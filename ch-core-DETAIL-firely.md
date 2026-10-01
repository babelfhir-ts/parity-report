# ch-core - Detailed Report (FHIR all)
Generated: 2026-09-05T11:32:27.235Z

Package: `ch.fhir.ig.ch-core@6.0.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 29 | 29 | 100% |
| Random Validation Parity | 27 | 29 | 93% |
| Random Generation Validation + Parity | 22 | 29 | 76% |


---

## Empty Validation Parity Results

### ✅ Passing (29)
- ✅ CHCoreAllergyIntoleranceClass
- ✅ CHCoreConditionClass
- ✅ CHCoreCoverageClass
- ✅ CHCoreDocumentReferenceClass
- ✅ CHCoreEncounterClass
- ✅ CHCoreImmunizationClass
- ✅ CHCoreImmunizationRecommendationClass
- ✅ CHCoreLocationClass
- ✅ CHCoreMedicationAdministrationClass
- ✅ CHCoreMedicationClass
- ✅ CHCoreMedicationDispenseClass
- ✅ CHCoreMedicationRequestClass
- ✅ CHCoreMedicationStatementClass
- ✅ CHCoreOrganizationClass
- ✅ CHCoreOrganizationEPRClass
- ✅ CHCorePatientClass
- ✅ CHCorePatientEPRClass
- ✅ CHCorePractitionerClass
- ✅ CHCorePractitionerEPRClass
- ✅ CHCorePractitionerRoleClass
- ✅ CHCorePractitionerRoleEprClass
- ✅ CHCoreServiceRequestClass
- ✅ CHCoreClaimClass
- ✅ CHCoreCompositionClass
- ✅ CHCoreCompositionEPRClass
- ✅ CHCoreDocumentClass
- ✅ CHCoreDocumentEPRClass
- ✅ CHCoreEPRConsentClass
- ✅ CHCoreRelatedPersonClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (27)
- ✅ CHCoreAllergyIntoleranceClass
- ✅ CHCoreConditionClass
- ✅ CHCoreCoverageClass
- ✅ CHCoreDocumentReferenceClass
- ✅ CHCoreEncounterClass
- ✅ CHCoreImmunizationClass
- ✅ CHCoreImmunizationRecommendationClass
- ✅ CHCoreLocationClass
- ✅ CHCoreMedicationAdministrationClass
- ✅ CHCoreMedicationClass
- ✅ CHCoreMedicationDispenseClass
- ✅ CHCoreMedicationRequestClass
- ✅ CHCoreMedicationStatementClass
- ✅ CHCoreOrganizationClass
- ✅ CHCoreOrganizationEPRClass
- ✅ CHCorePatientClass
- ✅ CHCorePatientEPRClass
- ✅ CHCorePractitionerClass
- ✅ CHCorePractitionerEPRClass
- ✅ CHCorePractitionerRoleClass
- ✅ CHCorePractitionerRoleEprClass
- ✅ CHCoreServiceRequestClass
- ✅ CHCoreClaimClass
- ✅ CHCoreCompositionClass
- ✅ CHCoreCompositionEPRClass
- ✅ CHCoreEPRConsentClass
- ✅ CHCoreRelatedPersonClass

### ❌ Failing (2)
- ❌ CHCoreDocumentClass
  - Field-level comparison:
  Both validators: none
  Only Firely: entry

- ❌ CHCoreDocumentEPRClass
  - Field-level comparison:
  Both validators: none
  Only Firely: entry


---

## Random Generation Validation + Parity Results

### ✅ Passing (22)
- ✅ CHCoreAllergyIntoleranceClass
- ✅ CHCoreConditionClass
- ✅ CHCoreCoverageClass
- ✅ CHCoreDocumentReferenceClass
- ✅ CHCoreEncounterClass
- ✅ CHCoreImmunizationClass
- ✅ CHCoreImmunizationRecommendationClass
- ✅ CHCoreLocationClass
- ✅ CHCoreMedicationAdministrationClass
- ✅ CHCoreMedicationClass
- ✅ CHCoreMedicationDispenseClass
- ✅ CHCoreMedicationRequestClass
- ✅ CHCoreMedicationStatementClass
- ✅ CHCoreOrganizationClass
- ✅ CHCoreOrganizationEPRClass
- ✅ CHCorePractitionerRoleClass
- ✅ CHCorePractitionerRoleEprClass
- ✅ CHCoreServiceRequestClass
- ✅ CHCoreClaimClass
- ✅ CHCoreCompositionClass
- ✅ CHCoreCompositionEPRClass
- ✅ CHCoreEPRConsentClass

### ❌ Failing (7)
- ❌ CHCorePatientClass (1 errors)
    - Unable to resolve reference to profile 'http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address'. Details: Encountered an error while loading schema 'http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address': Failed to convert ElementDefinition at Address.line.extension:streetName in profile http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address: The value discriminator should have a 'fixed[x]', 'pattern[x]' or binding element set on 'Extension.value[x]'.
- ❌ CHCorePatientEPRClass (1 errors)
    - Unable to resolve reference to profile 'http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address'. Details: Encountered an error while loading schema 'http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address': Failed to convert ElementDefinition at Address.line.extension:streetName in profile http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address: The value discriminator should have a 'fixed[x]', 'pattern[x]' or binding element set on 'Extension.value[x]'.
- ❌ CHCorePractitionerClass (1 errors)
    - Unable to resolve reference to profile 'http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address'. Details: Encountered an error while loading schema 'http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address': Failed to convert ElementDefinition at Address.line.extension:streetName in profile http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address: The value discriminator should have a 'fixed[x]', 'pattern[x]' or binding element set on 'Extension.value[x]'.
- ❌ CHCorePractitionerEPRClass (1 errors)
    - Unable to resolve reference to profile 'http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address'. Details: Encountered an error while loading schema 'http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address': Failed to convert ElementDefinition at Address.line.extension:streetName in profile http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address: The value discriminator should have a 'fixed[x]', 'pattern[x]' or binding element set on 'Extension.value[x]'.
- ❌ CHCoreDocumentClass (3 errors)
    - Unable to resolve reference to profile 'http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address'. Details: Encountered an error while loading schema 'http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address': Failed to convert ElementDefinition at Address.line.extension:streetName in profile http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address: The value discriminator should have a 'fixed[x]', 'pattern[x]' or binding element set on 'Extension.value[x]'.
    - Unable to resolve reference to profile 'http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address'. Details: Encountered an error while loading schema 'http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address': Failed to convert ElementDefinition at Address.line.extension:streetName in profile http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address: The value discriminator should have a 'fixed[x]', 'pattern[x]' or binding element set on 'Extension.value[x]'. (for slice forPractitioner)
    - No elements matched required slice: 'entry:Composition'
- ❌ CHCoreDocumentEPRClass (3 errors)
    - Unable to resolve reference to profile 'http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address'. Details: Encountered an error while loading schema 'http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address': Failed to convert ElementDefinition at Address.line.extension:streetName in profile http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address: The value discriminator should have a 'fixed[x]', 'pattern[x]' or binding element set on 'Extension.value[x]'.
    - Unable to resolve reference to profile 'http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address'. Details: Encountered an error while loading schema 'http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address': Failed to convert ElementDefinition at Address.line.extension:streetName in profile http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address: The value discriminator should have a 'fixed[x]', 'pattern[x]' or binding element set on 'Extension.value[x]'. (for slice forPractitioner)
    - No elements matched required slice: 'entry:Composition'
- ❌ CHCoreRelatedPersonClass (1 errors)
    - Unable to resolve reference to profile 'http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address'. Details: Encountered an error while loading schema 'http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address': Failed to convert ElementDefinition at Address.line.extension:streetName in profile http://fhir.ch/ig/ch-core/StructureDefinition/ch-core-address: The value discriminator should have a 'fixed[x]', 'pattern[x]' or binding element set on 'Extension.value[x]'.

---

[← Back to Summary](./pipeline-parity-summary.md)
