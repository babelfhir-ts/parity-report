---
url: /parity-report/docs/generated-code.md
description: >-
  Understand the TypeScript output produced by BabelFHIR-TS — module structure,
  interfaces, validators, classes, ValueSet helpers, and how to import generated
  code.
---

# Generated Code Guide

Generated profile packages installed via `babelfhir-ts install` are published as **compiled JavaScript with TypeScript declarations**:

* JavaScript for runtime: `index.js`, `*.js`
* Type declarations for IDE/TS: `index.d.ts`, `*.d.ts`

## Dependencies

* `@types/fhir` is included as a dependency of the generated package (no extra setup in your app)
* The version-matched base client (e.g., [`@babelfhir-ts/client-r4`](https://www.npmjs.com/package/@babelfhir-ts/client-r4)) is included as a dependency (base FHIR client that the generated client extends)
* `fhirpath` is a peer dependency (required only if you use the generated validators/classes)

Install `fhirpath` in your app if you plan to call `.validate()` or use the generated classes:

```bash
npm install fhirpath
```

## Module Resolution

Generated packages work with all modern TypeScript setups:

* **Node.js 18+** with `"type": "module"` in `package.json`
* **Bundlers** (Vite, esbuild, Webpack) with ESM output
* **TypeScript 5.0+** with any module resolution (`node16`, `nodenext`, or `bundler`)

## FHIR Type Imports

Generated code imports base FHIR types from the version-specific module (`fhir/r4`, `fhir/r4b`, or `fhir/r5`):

```ts
import { Appointment, Extension, CodeableConcept } from "fhir/r4";
```

Since `@types/fhir` doesn't provide a `package.json` `exports` field, BabelFHIR-TS includes a **version-specific ambient module declaration** (e.g., `fhir-r4.d.ts`, `fhir-r4b.d.ts`, or `fhir-r5.d.ts`) in every generated package. The generated `index.d.ts` references this file:

```ts
/// <reference path="./fhir-r4.d.ts" />
```

This ensures TypeScript can resolve `fhir/r4` (or `fhir/r4b`, `fhir/r5`) imports automatically without any configuration in your project's `tsconfig.json`.

## What Gets Generated

For each profile in an Implementation Guide, BabelFHIR-TS generates:

| File | Description |
|---|---|
| `<Profile>.ts` | TypeScript interface with all constraints, extensions, and slicing rules |
| `<Profile>Class.ts` | Helper class with `empty()`, `random()`, and `validate()` methods |
| `<Profile>Validator.ts` | Standalone validator function with FHIRPath constraint evaluation |
| `valuesets/` | ValueSet modules with typed code unions, random pickers, and registry (see [ValueSets](./valuesets)) |
| `fhir-client/` | Type-safe FHIR client with profile-specific methods (see [FHIR Client](./fhir-client)) |
| `dicomweb/` | DICOMweb helpers typed to ImagingStudy profiles (when `--dicomweb` is used, see [DICOMweb](./dicomweb)) |
| `<Profile>.zod.ts` | Zod schema (when `--schema zod` is used, see [Schema Generation](./schema-generation)) |
| `index.ts` | Barrel export of all generated types |
| `fhir-<version>.d.ts` | Ambient module declaration for `fhir/<version>` imports (r4/r4b/r5) |
| `ValidatorOptions.ts` | Shared runtime options type for all validators (see [Validation](./validation#runtime-validator-options)) |

### Interfaces

Generated interfaces merge profile constraints with base FHIR types:

```ts
import { Patient, Extension } from "fhir/r4";

export interface USCorePatientProfile extends Patient {
  identifier: USCorePatientProfile_Identifier[];
  name: USCorePatientProfile_Name[];
  // ... constrained fields with proper types
}
```

### Classes

Generated classes provide convenience methods:

```ts
const patient = USCorePatientProfileClass.empty();   // minimal valid resource
const random = USCorePatientProfileClass.random();   // populated with test data
const { errors, warnings } = await random.validate();
```

### Validators

Standalone validator functions can be used without the class wrapper:

```ts
import { validateUSCorePatientProfile } from "./output/USCorePatientProfile";

const result = await validateUSCorePatientProfile(myPatientResource);
```

## Package Exports

Generated packages use Node.js [subpath exports](https://nodejs.org/api/packages.html#subpath-exports) so consumers can import from well-defined entry points:

| Export Path | Description |
|---|---|
| `"."` | Main entry — all interfaces, classes, and validators |
| `"./fhir-client"` | Type-safe FHIR client (when client generation is enabled) |
| `"./valuesets/*"` | Individual ValueSet modules (when ValueSets are resolved) |
| `"./dicomweb"` | DICOMweb helpers (when `--dicomweb` is used) |
| `"./dicomweb/cornerstone"` | Cornerstone3D integration (when `--dicomweb` is used) |

```ts
// Main entry
import { USCorePatientProfile, USCorePatientProfileClass } from "hl7.fhir.us.core-generated";

// FHIR client
import { FhirClient } from "hl7.fhir.us.core-generated/fhir-client";

// Individual ValueSet
import { AdministrativeGenderCode } from "hl7.fhir.us.core-generated/valuesets/ValueSet-AdministrativeGender";
```

## Package Metadata

Generated packages include a `fhir` field in `package.json` that stores the generation settings. This metadata powers `babelfhir-ts update` — when you regenerate packages, the original flags are preserved automatically:

```json
{
  "fhir": {
    "ig": "hl7.fhir.us.core",
    "version": "8.0.0",
    "fhirVersion": "r4",
    "txServer": "https://tx.fhir.org/r4",
    "displayLanguage": "de,en",
    "maxCodes": 1000
  }
}
```

| Field | Description |
|---|---|
| `ig` | Source FHIR package name |
| `version` | Package version |
| `canonical` | IG canonical URL (if available) |
| `fhirVersions` | FHIR version list from the IG manifest |
| `fhirVersion` | Target FHIR version (r4/r4b/r5) |
| `txServer` | Terminology server URL used during generation |
| `displayLanguage` | Language(s) for display terms |
| `maxCodes` | Cap on concepts kept per expanded ValueSet |
| `dicomweb` | Whether DICOMweb helpers were generated |
| `noClient` | Whether client generation was skipped |
| `noClasses` | Whether class generation was skipped |
| `schema` | Schema format (e.g., `"zod"`) |
