---
url: /parity-report/docs/valuesets.md
description: >-
  Generated typed ValueSet modules provide code unions, runtime validators,
  random pickers, and a central registry for every ValueSet binding in your FHIR
  Implementation Guide.
---

# ValueSets

BabelFHIR-TS generates typed ValueSet modules for every ValueSet binding resolved from the StructureDefinitions in your Implementation Guide. These modules provide code unions, runtime validators, random pickers, and a central registry.

## Generated Files

ValueSet files are emitted in a `valuesets/` directory:

```
valuesets/
  ValueSet-AdministrativeGender.ts
  ValueSet-ConditionClinicalStatusCodes.ts
  ValueSet-USCoreRace.ts
  ...
  ValueSetRegistry.ts
```

## Per-ValueSet Module

Each `ValueSet-<Name>.ts` file exports:

### Code Union Type

A string literal union of all valid codes:

```ts
export type AdministrativeGenderCode = "male" | "female" | "other" | "unknown";
```

### Concept Array

An array of concept objects with code, system, and display:

```ts
export interface AdministrativeGenderConcept {
  code: string;
  system: string;
  display?: string;
}

export const AdministrativeGenderConcepts: AdministrativeGenderConcept[] = [
  { code: "male", system: "http://hl7.org/fhir/administrative-gender", display: "Male" },
  { code: "female", system: "http://hl7.org/fhir/administrative-gender", display: "Female" },
  // ...
];
```

### Codes Array

A convenience array of just the code strings:

```ts
export const AdministrativeGenderCodes = AdministrativeGenderConcepts.map(c => c.code);
```

### Validation Helper

Check if a string is a valid code:

```ts
export function isValidAdministrativeGenderCode(code: string): code is AdministrativeGenderCode {
  return AdministrativeGenderConcepts.some(c => c.code === code);
}
```

### Concept Lookup

Get concept details (system + display) by code:

```ts
export function getAdministrativeGenderConcept(code: string): AdministrativeGenderConcept | undefined {
  return AdministrativeGenderConcepts.find(c => c.code === code);
}
```

### Random Pickers

For test data generation:

```ts
export function randomAdministrativeGenderCode(): AdministrativeGenderCode {
  return AdministrativeGenderCodes[Math.floor(Math.random() * AdministrativeGenderCodes.length)];
}

export function randomAdministrativeGenderConcept(): AdministrativeGenderConcept {
  return AdministrativeGenderConcepts[Math.floor(Math.random() * AdministrativeGenderConcepts.length)];
}
```

## ValueSet Registry

The `ValueSetRegistry.ts` file provides a central entry point for all resolved ValueSets:

### Registry Object

```ts
import { getValueSet, ValueSetUrlMap, getRandomCodeByUrl, getRandomConceptByUrl } from "./valuesets/ValueSetRegistry";
```

### Lookup by Name

```ts
import { getValueSet } from "./valuesets/ValueSetRegistry";

const vs = getValueSet("AdministrativeGender");
// Access all exports from ValueSet-AdministrativeGender.ts
```

### Lookup by URL

```ts
import { ValueSetUrlMap, getRandomCodeByUrl, getRandomConceptByUrl } from "./valuesets/ValueSetRegistry";

// Map from canonical URL to registry name
const name = ValueSetUrlMap["http://hl7.org/fhir/ValueSet/administrative-gender"];
// "AdministrativeGender"

// Get a random code from a ValueSet by its canonical URL
const code = getRandomCodeByUrl("http://hl7.org/fhir/ValueSet/administrative-gender");
// e.g., "female"

// Get a random concept (code + system + display) by URL
const concept = getRandomConceptByUrl("http://hl7.org/fhir/ValueSet/administrative-gender|4.0.1");
// { code: "male", system: "http://hl7.org/fhir/administrative-gender", display: "Male" }
```

The URL lookup automatically strips version suffixes (e.g., `|4.0.1`) for matching.

## Multi-Language Display

When `--display-language` is used with multiple languages, ValueSet modules include additional display map exports. See [Multi-Language Display Terms](./i18n) for details.

## Empty ValueSets

ValueSets that have no explicitly enumerated codes (e.g., defined by filters or external terminology) are noted in a comment but don't generate code arrays or helpers. Runtime validation for these ValueSets requires a terminology server (see [Validator Runtime Options](./validation#runtime-validator-options)).

## Package Export

The `valuesets/` directory is exposed via a subpath export:

```ts
// Import a specific ValueSet
import { AdministrativeGenderCode } from "my-ig-generated/valuesets/ValueSet-AdministrativeGender";

// Import the registry
import { getRandomCodeByUrl } from "my-ig-generated/valuesets/ValueSetRegistry";
```
