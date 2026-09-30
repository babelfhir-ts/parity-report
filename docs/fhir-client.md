---
url: /parity-report/docs/fhir-client.md
description: >-
  Use the generated type-safe FHIR client to interact with FHIR servers using
  profile-specific methods, SMART on FHIR auth, and full R4/R4B/R5 base resource
  coverage.
---

# FHIR Client

BabelFHIR-TS generates a **type-safe FHIR client** that extends the version-matched base client ([`@babelfhir-ts/client-r4`](https://www.npmjs.com/package/@babelfhir-ts/client-r4), [`client-r4b`](https://www.npmjs.com/package/@babelfhir-ts/client-r4b), or [`client-r5`](https://www.npmjs.com/package/@babelfhir-ts/client-r5)) with profile-specific methods.

## Basic Usage

```ts
import { FhirClient } from "./output/fhir-client";

const client = new FhirClient("https://hapi.fhir.org/baseR4");
```

## Profile-Specific Methods

The generated client adds methods named after your IG's profiles:

```ts
// Read a US Core Patient by ID
const patient = await client.read().uSCorePatientProfile().read("123");

// Search for US Core Conditions
const bundle = await client.read().usCoreCondition().search({ patient: "123" });
```

## Base FHIR Resources

All base resource types for the selected FHIR version are available:

```ts
const appointment = await client.read().appointment().read("456");
const encounters = await client.read().encounter().search({ patient: "123" });
```

## Skipping Client Generation

If you don't need the FHIR client (e.g., you already use another HTTP client), pass `--no-client` to skip generating the `fhir-client/` module:

```bash
babelfhir-ts --package hl7.fhir.us.core@8.0.0 --no-client
```

## Base Client Package

The version-matched base client package (e.g., [`@babelfhir-ts/client-r4`](https://www.npmjs.com/package/@babelfhir-ts/client-r4)) is automatically included as a dependency of every generated package. It provides:

* CRUD operations for all R4 resource types
* Search with type-safe parameters
* Bundle handling
* Pagination support

The generated client extends this base with profile-specific accessor methods unique to your Implementation Guide.

## Using Multiple Packages

When your project depends on multiple generated IG packages (e.g., Da Vinci PAS **and** Da Vinci DTR), each package would generate its own `FhirClient` subclass — but you only need **one** client instance. The recommended pattern:

1. Install the base client directly:
   ```bash
   npm install @babelfhir-ts/client-r4
   ```

2. Install each IG package with `--no-client` to skip generating per-package clients:
   ```bash
   babelfhir-ts install hl7.fhir.us.davinci-pas@2.1.0 --no-client
   babelfhir-ts install hl7.fhir.us.davinci-dtr@2.1.0 --no-client
   ```

3. Use `forType<T>()` for profile-specific access from any package:

   ```ts
   import { FhirClient } from "@babelfhir-ts/client-r4";
   import type { PASClaim, PASCoverage } from "hl7.fhir.us.davinci-pas-generated";
   import type { DTRQuestionnaireResponse } from "hl7.fhir.us.davinci-dtr-generated";

   const client = new FhirClient("https://fhir.example.com", authFetch);

   // Base R4 types — named accessors (inherited from @babelfhir-ts/client-r4)
   const patient = await client.read().patient().read("123");

   // Profile types from any package — forType<T>()
   const claim = await client.read().forType<PASClaim>("Claim").search({ status: "active" });
   const coverage = await client.read().forType<PASCoverage>("Coverage").searchAll({
     patient: "Patient/123",
   });
   const qr = await client.read().forType<DTRQuestionnaireResponse>("QuestionnaireResponse").read("456");

   // Write operations work the same way
   await client.write().forType<PASClaim>("Claim").create(myClaim);
   ```

`forType<T>(resourceType)` is available on both `read()` and `write()` clients and returns a fully typed reader/writer for any FHIR resource type `T`. The `resourceType` string must be the base FHIR resource type name (e.g., `"Claim"`, not the profile name).

## SMART on FHIR Authentication

The base client package includes built-in SMART App Launch (v2) support with PKCE. This is provided via [`@babelfhir-ts/smart-auth`](https://www.npmjs.com/package/@babelfhir-ts/smart-auth), which is re-exported from the client package.

### SmartFhirClient

The easiest way to use SMART auth is through `SmartFhirClient`, which combines discovery, token management, and the typed FHIR client:

```ts
import { SmartFhirClient } from "@babelfhir-ts/client-r4";

const smart = new SmartFhirClient({
  clientId: "my-app",
  redirectUri: "http://localhost:3000/callback",
  fhirBaseUrl: "https://fhir.example.com/fhir",
  scopes: "openid fhirUser patient/*.read",
});

// On page load: check if this is an OAuth callback
if (smart.isCallback()) {
  const token = await smart.handleCallback();
  // token.patient, token.fhirUser available from context
} else if (!smart.isAuthenticated()) {
  await smart.authorize(); // redirects to IdP
  return;
}

// Authenticated requests — all headers injected automatically
const patient = await smart.read().patient().read("123");
```

### SmartAuth (Standalone)

For more control, use `SmartAuth` directly to manage the OAuth flow without coupling to the FHIR client:

```ts
import { SmartAuth } from "@babelfhir-ts/client-r4";

const auth = new SmartAuth({
  clientId: "my-app",
  redirectUri: "http://localhost:3000/callback",
  fhirBaseUrl: "https://fhir.example.com/fhir",
  scopes: "openid fhirUser patient/*.read",
});

// Handles both standalone and EHR launch automatically
await auth.authorize();

// After callback:
const token = await auth.handleCallback();
const authFetch = auth.createAuthenticatedFetch();
```

### Configuration

| Option | Type | Description |
|---|---|---|
| `clientId` | `string` | OAuth2 client\_id registered with the auth server |
| `redirectUri` | `string` | Redirect URI registered with the auth server |
| `fhirBaseUrl` | `string` | FHIR server base URL (used as `aud` parameter) |
| `scopes` | `string` | Space-separated OAuth2 scopes |
| `storage` | `Storage` | Optional storage backend (defaults to `sessionStorage`) |
| `storagePrefix` | `string` | Optional prefix for storage keys (defaults to `"smart_"`) |
| `postLogoutRedirectUri` | `string` | Where to redirect after IdP logout |

### Launch Modes

SMART supports two launch modes, auto-detected from URL parameters:

* **Standalone** — your app initiates the flow by redirecting to the authorization endpoint
* **EHR** — the EHR redirects to your app with `?launch=...&iss=...` parameters

`SmartFhirClient.authorize()` and `SmartAuth.authorize()` detect the mode automatically.

### Token Context

After a successful callback, the `SmartToken` object includes:

```ts
interface SmartToken {
  access_token: string;
  token_type: string;
  expires_in: number;
  scope: string;
  id_token?: string;
  refresh_token?: string;
  fhirUser?: string;   // e.g., "Practitioner/123"
  patient?: string;     // patient context from EHR launch
  encounter?: string;   // encounter context from EHR launch
}
```

### Endpoint Discovery

The library discovers OAuth endpoints automatically via:

1. `/.well-known/smart-configuration` (preferred)
2. `/metadata` CapabilityStatement fallback

You can also call `discoverEndpoints()` directly:

```ts
import { discoverEndpoints } from "@babelfhir-ts/client-r4";

const config = await discoverEndpoints("https://fhir.example.com/fhir");
// config.authorization_endpoint, config.token_endpoint, etc.
```
