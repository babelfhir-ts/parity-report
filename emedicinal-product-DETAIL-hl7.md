# emedicinal-product - Detailed Report (FHIR all)
Generated: 2026-08-29T11:15:02.458Z

Package: `hl7.fhir.uv.emedicinal-product-info@1.0.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 15 | 15 | 100% |
| Random Validation Parity | 15 | 15 | 100% |
| Random Generation Validation + Parity | 11 | 15 | 73% |


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

## Random Generation Validation + Parity Results

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
- ❌ BundleUvEpiClass (4 errors)
    - The property identifier must be a JSON Array, not an Object (at Bundle.entry[0].resource)
    - The property subject must be a JSON Array, not an Object (at Bundle.entry[0].resource)
    - Invalid Resource target type. Found Patient, but expected one of ([MedicinalProductDefinition])
    - Invalid Resource target type. Found Practitioner, but expected one of ([Organization])
- ❌ ClinicalUseDefinitionContraindicationUvEpiClass (1 errors)
    - Object must have some content
- ❌ CompositionUvEpiClass (2 errors)
    - The property subject must be a JSON Array, not an Object (at Composition)
    - A section must contain at least one of text, entries, or sub-sections
- ❌ IngredientUvEpiClass (2 errors)
    - Object must have some content
    - Object must have some content

---

[← Back to Summary](./pipeline-parity-summary.md)
