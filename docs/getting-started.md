---
url: /parity-report/docs/getting-started.md
description: >-
  Install BabelFHIR-TS, run your first code generation from a FHIR
  Implementation Guide, and start using the generated TypeScript interfaces,
  validators, and FHIR client.
---

# Getting Started

## Installation

Install globally (recommended when using the CLI frequently):

```bash
npm install -g @babelfhir-ts/codegen
```

Or invoke on-demand without a global install:

```bash
npx babelfhir-ts --help
```

::: info Requirements
Node.js 18+ (ESM support) and an internet connection when downloading packages from remote registries.
:::

## Quick Start

Generate code from a local folder that contains FHIR packages:

```bash
babelfhir-ts input/ output/
```

Process a single package archive and write the generated interfaces back into a new `.tgz` file:

```bash
babelfhir-ts hl7.fhir.us.core-8.0.0.tgz us-core-generated.tgz
```

Download and process a package directly from a registry (defaults to `https://packages.simplifier.net`):

```bash
babelfhir-ts --package hl7.fhir.us.core@8.0.0
```

Download, process, and install a processed package into your current project:

```bash
babelfhir-ts install hl7.fhir.us.core@8.0.0
```

## Using the Generated Code

After generation you can import the emitted classes:

```ts
import { USCorePatientProfileClass } from "./output/USCorePatientProfileClass";

const patient = USCorePatientProfileClass.random();
const { errors, warnings } = await patient.validate();
```

Or use the generated FHIR client to interact with a FHIR server:

```ts
import { FhirClient } from "./output/fhir-client";

const client = new FhirClient("https://hapi.fhir.org/baseR4");

// Profile-specific methods generated from your IG
const patient = await client.read().uSCorePatientProfile().read("123");
const bundle = await client.read().usCoreCondition().search({ patient: "123" });

// All base resource types for the selected FHIR version are available
const appointment = await client.read().appointment().read("456");
```

## Next Steps

* [CLI Reference](./cli-reference) — full list of commands and options
* [Generated Code Guide](./generated-code) — understanding the output
* [ValueSets](./valuesets) — generated ValueSet helpers and registry
* [FHIR Client](./fhir-client) — type-safe server interactions with SMART auth
* [Schema Generation](./schema-generation) — Zod schema output
* [DICOMweb](./dicomweb) — FHIR ImagingStudy to DICOMweb/Cornerstone3D
* [Multi-Language](./i18n) — localized display terms
* [Validation](./validation) — what the validators check and don't check
