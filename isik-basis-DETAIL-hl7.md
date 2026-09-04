# isik-basis - Detailed Report (FHIR all)
Generated: 2026-08-29T11:15:18.060Z

Package: `de.gematik.isik-basismodul@4.0.3`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 25 | 25 | 100% |
| Random Validation Parity | 23 | 25 | 92% |
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
- ❌ ISiKAngehoerigerClass
  - Field-level comparison:
  Both validators: none
  Only HL7: constraint

- ❌ ISiKProzedurClass
  - Field-level comparison:
  Both validators: none
  Only HL7: unclassified


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
    - The code system 'http://fhir.de/CodeSystem/bfarm/ops' version '*' in the ValueSet include is different to the one in the value ('2026')

---

[← Back to Summary](./pipeline-parity-summary.md)
