# isik-basis - Detailed Report (FHIR all)
Generated: 2026-10-01T09:09:45.174Z

Package: `de.gematik.isik-basismodul@4.0.3`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 25 | 25 | 100% |
| Random Validation Parity | 24 | 25 | 96% |
| Random Generation Validation + Parity | 23 | 25 | 92% |


---

## Empty Validation Parity Results

### ✅ Passing (25)
- ✅ ISiKAbrechnungsfallClass
- ✅ ISiKAlkoholAbususClass
- ✅ ISiKAllergieUnvertraeglichkeitClass
- ✅ ISiKAngehoerigerClass
- ✅ ISiKBerichtBundleClass
- ✅ ISiKBerichtSubSystemeClass
- ✅ ISiKBinaryClass
- ✅ ISiKCodeSystemClass
- ✅ ISiKKontaktGesundheitseinrichtungClass
- ✅ ISiKLebensZustandClass
- ✅ ISiKOrganisationClass
- ✅ ISiKOrganisationFachabteilungClass
- ✅ ISiKPatientClass
- ✅ ISiKPatientMergeSubscriptionClass
- ✅ ISiKPersonImGesundheitsberufClass
- ✅ ISiKProzedurClass
- ✅ ISiKRaucherStatusClass
- ✅ ISiKSchwangerschaftErwarteterEntbindungsterminClass
- ✅ ISiKSchwangerschaftsstatusClass
- ✅ ISiKStandortBettenstellplatzClass
- ✅ ISiKStandortClass
- ✅ ISiKStandortRaumClass
- ✅ ISiKStillstatusClass
- ✅ ISiKValueSetClass
- ✅ PatientMergeSubscriptionClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (24)
- ✅ ISiKAbrechnungsfallClass
- ✅ ISiKAlkoholAbususClass
- ✅ ISiKAllergieUnvertraeglichkeitClass
- ✅ ISiKAngehoerigerClass
- ✅ ISiKBerichtBundleClass
- ✅ ISiKBerichtSubSystemeClass
- ✅ ISiKBinaryClass
- ✅ ISiKCodeSystemClass
- ✅ ISiKKontaktGesundheitseinrichtungClass
- ✅ ISiKLebensZustandClass
- ✅ ISiKOrganisationClass
- ✅ ISiKOrganisationFachabteilungClass
- ✅ ISiKPatientClass
- ✅ ISiKPatientMergeSubscriptionClass
- ✅ ISiKPersonImGesundheitsberufClass
- ✅ ISiKRaucherStatusClass
- ✅ ISiKSchwangerschaftErwarteterEntbindungsterminClass
- ✅ ISiKSchwangerschaftsstatusClass
- ✅ ISiKStandortBettenstellplatzClass
- ✅ ISiKStandortClass
- ✅ ISiKStandortRaumClass
- ✅ ISiKStillstatusClass
- ✅ ISiKValueSetClass
- ✅ PatientMergeSubscriptionClass

### ❌ Failing (1)
- ❌ ISiKProzedurClass
  - Field-level comparison:
  Both validators: none
  Only HL7: code


---

## Random Generation Validation + Parity Results

### ✅ Passing (23)
- ✅ ISiKAbrechnungsfallClass
- ✅ ISiKAlkoholAbususClass
- ✅ ISiKAllergieUnvertraeglichkeitClass
- ✅ ISiKBerichtBundleClass
- ✅ ISiKBerichtSubSystemeClass
- ✅ ISiKBinaryClass
- ✅ ISiKCodeSystemClass
- ✅ ISiKKontaktGesundheitseinrichtungClass
- ✅ ISiKLebensZustandClass
- ✅ ISiKOrganisationClass
- ✅ ISiKOrganisationFachabteilungClass
- ✅ ISiKPatientClass
- ✅ ISiKPatientMergeSubscriptionClass
- ✅ ISiKPersonImGesundheitsberufClass
- ✅ ISiKRaucherStatusClass
- ✅ ISiKSchwangerschaftErwarteterEntbindungsterminClass
- ✅ ISiKSchwangerschaftsstatusClass
- ✅ ISiKStandortBettenstellplatzClass
- ✅ ISiKStandortClass
- ✅ ISiKStandortRaumClass
- ✅ ISiKStillstatusClass
- ✅ ISiKValueSetClass
- ✅ PatientMergeSubscriptionClass

### ❌ Failing (2)
- ❌ ISiKAngehoerigerClass (1 errors)
    - Slicing cannot be evaluated: Could not match discriminator ($this) for slice RelatedPerson.name:Name in profile https://gematik.de/fhir/isik/StructureDefinition/ISiKAngehoeriger|4.0.3 - the discriminator [$this] does not have fixed value, binding or existence assertions
- ❌ ISiKProzedurClass (1 errors)
    - Unknown code 'code-id-7ye' in the CodeSystem 'http://fhir.de/CodeSystem/bfarm/ops' version '2026'

---

[← Back to Summary](./pipeline-parity-summary.md)
