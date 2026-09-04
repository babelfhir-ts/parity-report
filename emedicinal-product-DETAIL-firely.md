# emedicinal-product - Detailed Report (FHIR all)
Generated: 2026-09-04T19:59:27.128Z

Package: `hl7.fhir.uv.emedicinal-product-info@1.0.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 15 | 15 | 100% |
| Random Validation Parity | 11 | 15 | 73% |
| Random Generation Validation + Parity | 12 | 15 | 80% |


---

## Empty Validation Parity Results

### ✅ Passing (15)
- ✅ OrganizationUvEpiClass
- ✅ AdministrableProductDefinitionUvEpiClass
- ✅ BundleUvEpiClass
- ✅ ClinicalUseDefinitionContraindicationUvEpiClass
- ✅ ClinicalUseDefinitionIndicationUvEpiClass
- ✅ ClinicalUseDefinitionInteractionUvEpiClass
- ✅ ClinicalUseDefinitionUndesirableEffectUvEpiClass
- ✅ ClinicalUseDefinitionWarningUvEpiClass
- ✅ CompositionUvEpiClass
- ✅ IngredientUvEpiClass
- ✅ ManufacturedItemDefinitionUvEpiClass
- ✅ MedicinalProductDefinitionUvEpiClass
- ✅ PackagedProductDefinitionUvEpiClass
- ✅ RegulatedAuthorizationUvEpiClass
- ✅ SubstanceDefinitionUvEpiClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (11)
- ✅ OrganizationUvEpiClass
- ✅ AdministrableProductDefinitionUvEpiClass
- ✅ ClinicalUseDefinitionIndicationUvEpiClass
- ✅ ClinicalUseDefinitionInteractionUvEpiClass
- ✅ ClinicalUseDefinitionUndesirableEffectUvEpiClass
- ✅ ClinicalUseDefinitionWarningUvEpiClass
- ✅ ManufacturedItemDefinitionUvEpiClass
- ✅ MedicinalProductDefinitionUvEpiClass
- ✅ PackagedProductDefinitionUvEpiClass
- ✅ RegulatedAuthorizationUvEpiClass
- ✅ SubstanceDefinitionUvEpiClass

### ❌ Failing (4)
- ❌ BundleUvEpiClass
  - Field-level comparison:
  Both validators: constraint
  Only Internal: identifier, subject

- ❌ ClinicalUseDefinitionContraindicationUvEpiClass
  - Field-level comparison:
  Both validators: none
  Only Internal: extension
  Only Firely: treatment

- ❌ CompositionUvEpiClass
  - Field-level comparison:
  Both validators: none
  Only Internal: subject, constraint

- ❌ IngredientUvEpiClass
  - Field-level comparison:
  Both validators: none
  Only Internal: extension
  Only Firely: code, substance


---

## Random Generation Validation + Parity Results

### ✅ Passing (12)
- ✅ OrganizationUvEpiClass
- ✅ AdministrableProductDefinitionUvEpiClass
- ✅ ClinicalUseDefinitionIndicationUvEpiClass
- ✅ ClinicalUseDefinitionInteractionUvEpiClass
- ✅ ClinicalUseDefinitionUndesirableEffectUvEpiClass
- ✅ ClinicalUseDefinitionWarningUvEpiClass
- ✅ CompositionUvEpiClass
- ✅ ManufacturedItemDefinitionUvEpiClass
- ✅ MedicinalProductDefinitionUvEpiClass
- ✅ PackagedProductDefinitionUvEpiClass
- ✅ RegulatedAuthorizationUvEpiClass
- ✅ SubstanceDefinitionUvEpiClass

### ❌ Failing (3)
- ❌ BundleUvEpiClass (2 errors)
    - The declared type of the element (MedicinalProductDefinition) is incompatible with that of the instance (Patient).
    - The declared type of the element (Organization) is incompatible with that of the instance (Practitioner).
- ❌ ClinicalUseDefinitionContraindicationUvEpiClass (1 errors)
    - One or more errors occurred. (An object needs to have at least one property. At ClinicalUseDefinition.contraindication.otherTherapy[0].treatment, line 42, position 8.)
- ❌ IngredientUvEpiClass (2 errors)
    - An object needs to have at least one property. At Ingredient.substance.code, line 26, position 16.
    - An object needs to have at least one property. At Ingredient.substance.strength[0].referenceStrength[0].substance, line 31, position 29.

---

[← Back to Summary](./pipeline-parity-summary.md)
