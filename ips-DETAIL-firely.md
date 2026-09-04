# ips - Detailed Report (FHIR all)
Generated: 2026-08-29T11:15:07.432Z

Package: `hl7.fhir.uv.ips@2.0.1`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 25 | 25 | 100% |
| Random Validation Parity | 24 | 25 | 96% |
| Random Generation Validation + Parity | 24 | 25 | 96% |


---

## Empty Validation Parity Results

### ✅ Passing (25)
- ✅ AllergyIntoleranceUvIpsClass
- ✅ ConditionUvIpsClass
- ✅ ImmunizationUvIpsClass
- ✅ MedicationIPSClass
- ✅ MedicationRequestIPSClass
- ✅ MedicationStatementIPSClass
- ✅ ObservationAlcoholUseUvIpsClass
- ✅ ObservationPregnancyEddUvIpsClass
- ✅ ObservationPregnancyOutcomeUvIpsClass
- ✅ ObservationPregnancyStatusUvIpsClass
- ✅ ObservationResultsLaboratoryPathologyUvIpsClass
- ✅ ObservationResultsRadiologyUvIpsClass
- ✅ ObservationTobaccoUseUvIpsClass
- ✅ OrganizationUvIpsClass
- ✅ PatientUvIpsClass
- ✅ PractitionerRoleUvIpsClass
- ✅ PractitionerUvIpsClass
- ✅ ProcedureUvIpsClass
- ✅ SpecimenUvIpsClass
- ✅ BundleUvIpsClass
- ✅ DeviceObserverUvIpsClass
- ✅ DeviceUseStatementUvIpsClass
- ✅ DeviceUvIpsClass
- ✅ FlagAlertUvIpsClass
- ✅ ImagingStudyUvIpsClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (24)
- ✅ AllergyIntoleranceUvIpsClass
- ✅ ConditionUvIpsClass
- ✅ ImmunizationUvIpsClass
- ✅ MedicationIPSClass
- ✅ MedicationRequestIPSClass
- ✅ MedicationStatementIPSClass
- ✅ ObservationAlcoholUseUvIpsClass
- ✅ ObservationPregnancyEddUvIpsClass
- ✅ ObservationPregnancyOutcomeUvIpsClass
- ✅ ObservationPregnancyStatusUvIpsClass
- ✅ ObservationResultsLaboratoryPathologyUvIpsClass
- ✅ ObservationResultsRadiologyUvIpsClass
- ✅ ObservationTobaccoUseUvIpsClass
- ✅ OrganizationUvIpsClass
- ✅ PatientUvIpsClass
- ✅ PractitionerRoleUvIpsClass
- ✅ PractitionerUvIpsClass
- ✅ ProcedureUvIpsClass
- ✅ SpecimenUvIpsClass
- ✅ DeviceObserverUvIpsClass
- ✅ DeviceUseStatementUvIpsClass
- ✅ DeviceUvIpsClass
- ✅ FlagAlertUvIpsClass
- ✅ ImagingStudyUvIpsClass

### ❌ Failing (1)
- ❌ BundleUvIpsClass
  - Field-level comparison:
  Both validators: none
  Only Firely: entry


---

## Random Generation Validation + Parity Results

### ✅ Passing (24)
- ✅ AllergyIntoleranceUvIpsClass
- ✅ ConditionUvIpsClass
- ✅ ImmunizationUvIpsClass
- ✅ MedicationIPSClass
- ✅ MedicationRequestIPSClass
- ✅ MedicationStatementIPSClass
- ✅ ObservationAlcoholUseUvIpsClass
- ✅ ObservationPregnancyEddUvIpsClass
- ✅ ObservationPregnancyOutcomeUvIpsClass
- ✅ ObservationPregnancyStatusUvIpsClass
- ✅ ObservationResultsLaboratoryPathologyUvIpsClass
- ✅ ObservationResultsRadiologyUvIpsClass
- ✅ ObservationTobaccoUseUvIpsClass
- ✅ OrganizationUvIpsClass
- ✅ PatientUvIpsClass
- ✅ PractitionerRoleUvIpsClass
- ✅ PractitionerUvIpsClass
- ✅ ProcedureUvIpsClass
- ✅ SpecimenUvIpsClass
- ✅ DeviceObserverUvIpsClass
- ✅ DeviceUseStatementUvIpsClass
- ✅ DeviceUvIpsClass
- ✅ FlagAlertUvIpsClass
- ✅ ImagingStudyUvIpsClass

### ❌ Failing (1)
- ❌ BundleUvIpsClass (2 errors)
    - Unable to resolve reference to profile 'http://hl7.org/fhir/uv/ips/StructureDefinition/Composition-uv-ips|2.0.1'. Details: Encountered an error while loading schema 'http://hl7.org/fhir/uv/ips/StructureDefinition/Composition-uv-ips|2.0.1': Failed to convert ElementDefinition at Composition.section:sectionMedications.entry:medicationStatementOrRequest in profile http://hl7.org/fhir/uv/ips/StructureDefinition/Composition-uv-ips: The discriminator path 'resolve()' at http://hl7.org/fhir/uv/ips/StructureDefinition/Composition-uv-ips#Composition.section.entry (Composition.section:sectionMedications.entry:medicationStatementOrRequest) leads to multiple ElementDefinitions, which is not allowed.
    - No elements matched required slice: 'entry:composition'

---

[← Back to Summary](./pipeline-parity-summary.md)
