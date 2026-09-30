---
url: /parity-report/docs/schema-generation.md
description: >-
  Generate Zod schemas alongside TypeScript output for runtime type validation
  with choice type expansion, FHIR constraint refinements, and profile-aware
  validation.
---

# Schema Generation (Zod)

BabelFHIR-TS can generate [Zod](https://zod.dev/) schemas alongside its standard TypeScript output. Zod schemas provide runtime type validation that complements the FHIRPath-based validators.

## Enabling Zod Schemas

Pass `--schema zod` during generation:

```bash
babelfhir-ts install hl7.fhir.us.core@8.0.0 --schema zod
babelfhir-ts --package hl7.fhir.us.core@8.0.0 --schema zod
```

## What Gets Generated

For each profile, a `<Profile>.zod.ts` file is generated containing:

* A Zod object schema with all profiled fields
* An inferred TypeScript type
* Constraint tracking metadata (for parity testing)

```ts
// USCorePatientProfile.zod.ts
import { z } from "zod";
import { PatientSchema } from "@babelfhir-ts/zod/r4";

export const USCorePatientProfileSchema = z.looseObject({
  resourceType: z.literal("Patient").optional(),
  identifier: z.array(IdentifierSchema).min(1),
  name: z.array(HumanNameSchema).min(1),
  gender: z.enum(["male", "female", "other", "unknown"]),
  // ...
})
.refine(/* pattern constraints */)
.refine(/* choice type requirements */);

export type USCorePatientProfile = z.infer<typeof USCorePatientProfileSchema>;
```

## Key Features

### Choice Type Expansion

FHIR `[x]` choice types (e.g., `value[x]`) are expanded into individual typed properties:

```ts
// value[x] becomes:
{
  valueString: z.string().optional(),
  valueQuantity: QuantitySchema.optional(),
  valueBoolean: z.boolean().optional(),
  // ...
}
```

Required choice fields generate a refinement that ensures at least one variant is present:

```ts
.refine(d => d.valueString !== undefined || d.valueQuantity !== undefined || ..., {
  message: "value must be present",
})
```

### Primitive Underscore Companions

For primitive choice variants, FHIR's `_field` companion elements (containing `id` and `extension`) are automatically emitted:

```ts
{
  valueString: z.string().optional(),
  _valueString: ElementSchema.optional(),  // id + extension
}
```

### resourceType Literal

Resource profiles include a `resourceType` literal field for discriminated unions:

```ts
{
  resourceType: z.literal("Patient").optional(),
  // ...
}
```

### ValueSet Bindings

When a field has a required binding with resolved codes (up to 50 values), the schema uses `z.enum()`:

```ts
{
  gender: z.enum(["male", "female", "other", "unknown"]),
  status: z.literal("active"),  // single-code ValueSets become literals
}
```

### BackboneElement Inlining

Nested BackboneElement fields are inlined as nested Zod object schemas:

```ts
{
  contact: z.array(z.looseObject({
    name: HumanNameSchema.optional(),
    telecom: z.array(ContactPointSchema).optional(),
  })).optional(),
}
```

### Refinements

Profile constraints are expressed as Zod refinements:

* **Pattern constraints** (e.g., `patternCodeableConcept`)
* **Slice cardinality** (minimum element counts for required slices)
* **Meta sub-fields** (e.g., `meta.profile` must contain the profile URL)

### Constraint Metadata

Each schema exports tracking arrays for parity testing:

```ts
/** FHIRPath constraints not yet expressible in Zod */
export const _unsupportedConstraints: string[] = ["dom-6", "..."];

/** FHIRPath constraints translatable to JS */
export const _supportedConstraints: string[] = ["ele-1", "..."];
```

## Dependencies

When `--schema zod` is used:

* `zod` (v4+) is added as a **peer dependency** of the generated package
* `@babelfhir-ts/zod` is added as a **dependency** (provides base FHIR type schemas like `PatientSchema`, `QuantitySchema`, etc.)

Install Zod in your project:

```bash
npm install zod
```

## Usage

```ts
import { USCorePatientProfileSchema } from "hl7.fhir.us.core-generated/USCorePatientProfile.zod";

// Parse and validate unknown data
const result = USCorePatientProfileSchema.safeParse(unknownData);
if (result.success) {
  const patient = result.data; // typed as USCorePatientProfile
} else {
  console.error(result.error.issues);
}
```

::: tip Zod vs FHIRPath Validators
Zod schemas validate structural types and cardinality synchronously. The FHIRPath-based `validate()` methods additionally evaluate complex FHIR invariants and can check terminology bindings asynchronously. Use Zod for fast input parsing and `validate()` for full conformance checking.
:::
