---
url: /parity-report/docs/limitations.md
description: >-
  Known limitations of BabelFHIR-TS including unsupported FHIR profiling
  patterns, random() edge cases, FHIRPath coverage gaps, and how to report
  issues.
---

# Limitations

BabelFHIR-TS is a code generation tool that parses FHIR StructureDefinitions and produces TypeScript interfaces and validators. While it handles many common FHIR profiling patterns, there are important limitations to be aware of.

## FHIR Version Support

* **R4, R4B, and R5** are supported. The FHIR version is auto-detected from the package or can be set with `--fhir-version`.
* **Dependencies** — generated code depends on `@types/fhir` (R4/R4B/R5 definitions) and `fhirpath` (peer dependency for validators).
* **`@types/fhir` gaps** — `@types/fhir` does not export `SimpleQuantity` or `MoneyQuantity` (FHIR constraint profiles on `Quantity`). BabelFHIR-TS ships its own type aliases to fill this gap. See [DefinitelyTyped#74830](https://github.com/DefinitelyTyped/DefinitelyTyped/issues/74830).

## Profile Mapping Accuracy

* **Not guaranteed for all IGs** — the generator uses heuristics to interpret StructureDefinition constraints, slicing rules, and extensions. Complex or unusual profiling patterns may not map correctly to TypeScript.
* **Test before production** — always validate the generated code against your specific Implementation Guide's examples and test cases. We recommend running the official FHIR validator alongside BabelFHIR-TS in your QA pipeline.
* **Edge cases** — rare profiling constructs (deeply nested slicing, conditional constraints, complex discriminators) may generate suboptimal or incomplete types.

## TypeScript Limitations

* **Runtime type checking is limited** — TypeScript types are erased at compile time. The generated interfaces provide compile-time safety but cannot enforce constraints at runtime without the validator functions.
* **Extension slicing** — while the generator creates typed extension interfaces, TypeScript cannot enforce that extension arrays contain exactly the required slices at compile time (this is validated at runtime).
* **Choice types** — FHIR's `[x]` choice types (e.g., `value[x]`) are represented as union types in TypeScript, which may require runtime type narrowing.

## `random()` Method

The generated `.random()` methods create test data that satisfies TypeScript types and basic cardinality, but **do not guarantee** fully valid FHIR resources. Random data may violate:

* Complex FHIRPath invariants
* ValueSet bindings (codes are randomly chosen from required bindings but not guaranteed to be semantically correct)
* Profile-specific business rules
* Reference integrity constraints

Use `random()` for development, testing, and prototyping, but always validate production data on the FHIR server side.

## `validate()` Method

The generated validation methods execute FHIRPath expressions and check constraints from StructureDefinitions. They are tested against the HL7 Java Validator and the Firely SDK Validator for the Implementation Guides listed in the [Validation](./validation) page.

Edge cases, complex slicing patterns, or profiles not in the CI pipeline may produce different results. For production conformance testing, use the official [HL7 FHIR Validator](https://confluence.hl7.org/display/FHIR/Using+the+FHIR+Validator) as the source of truth.

## Reporting Issues

If you encounter an Implementation Guide that doesn't generate correctly, please [open an issue](https://github.com/babelfhir-ts/BabelFHIR-TS/issues) with:

* The package name and version
* The specific StructureDefinition URL
* Expected vs. actual generated output
* Any validation errors or type mismatches
