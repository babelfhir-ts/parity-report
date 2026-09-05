# au-core - Detailed Report (FHIR all)
Generated: 2026-09-05T11:32:27.112Z

Package: `hl7.fhir.au.core@2.0.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 13 | 13 | 100% |
| Random Validation Parity | 20 | 20 | 100% |
| Random Generation Validation + Parity | 16 | 20 | 80% |


---

## Empty Validation Parity Results

### ✅ Passing (13)
- ✅ AUCoreAllergyIntoleranceClass
- ✅ AUCoreEncounterClass
- ✅ AUCoreImmunizationClass
- ✅ AUCoreLocationClass
- ✅ AUCoreMedicationStatementClass
- ✅ AUCoreOrganizationClass
- ✅ AUCorePatientClass
- ✅ AUCorePractitionerClass
- ✅ AUCorePractitionerRoleClass
- ✅ AUCoreDiagnosticResultClass
- ✅ AUCoreHealthcareServiceClass
- ✅ AUCorePathologyResultClass
- ✅ AUCoreRelatedPersonClass

### ❌ Failing (0)
_None_

### ⚠️ Excluded - External Issues (7)
- ⚠️ AUCoreBloodPressureClass (excluded - Validator bug)
- ⚠️ AUCoreBodyHeightClass (excluded - Validator bug)
- ⚠️ AUCoreBodyTemperatureClass (excluded - Validator bug)
- ⚠️ AUCoreBodyWeightClass (excluded - Validator bug)
- ⚠️ AUCoreHeartRateClass (excluded - Validator bug)
- ⚠️ AUCoreRespirationRateClass (excluded - Validator bug)
- ⚠️ AUCoreWaistCircumferenceClass (excluded - Validator bug)

---

## Random Validation Parity Results

### ✅ Passing (20)
- ✅ AUCoreAllergyIntoleranceClass
- ✅ AUCoreEncounterClass
- ✅ AUCoreImmunizationClass
- ✅ AUCoreLocationClass
- ✅ AUCoreMedicationStatementClass
- ✅ AUCoreOrganizationClass
- ✅ AUCorePatientClass
- ✅ AUCorePractitionerClass
- ✅ AUCorePractitionerRoleClass
- ✅ AUCoreBloodPressureClass
- ✅ AUCoreBodyHeightClass
- ✅ AUCoreBodyTemperatureClass
- ✅ AUCoreBodyWeightClass
- ✅ AUCoreDiagnosticResultClass
- ✅ AUCoreHealthcareServiceClass
- ✅ AUCoreHeartRateClass
- ✅ AUCorePathologyResultClass
- ✅ AUCoreRelatedPersonClass
- ✅ AUCoreRespirationRateClass
- ✅ AUCoreWaistCircumferenceClass

### ❌ Failing (0)
_None_

---

## Random Generation Validation + Parity Results

### ✅ Passing (16)
- ✅ AUCoreAllergyIntoleranceClass
- ✅ AUCoreEncounterClass
- ✅ AUCoreImmunizationClass
- ✅ AUCoreOrganizationClass
- ✅ AUCorePractitionerClass
- ✅ AUCorePractitionerRoleClass
- ✅ AUCoreBodyHeightClass
- ✅ AUCoreBodyTemperatureClass
- ✅ AUCoreBodyWeightClass
- ✅ AUCoreDiagnosticResultClass
- ✅ AUCoreHealthcareServiceClass
- ✅ AUCoreHeartRateClass
- ✅ AUCorePathologyResultClass
- ✅ AUCoreRelatedPersonClass
- ✅ AUCoreRespirationRateClass
- ✅ AUCoreWaistCircumferenceClass

### ❌ Failing (4)
- ❌ AUCoreLocationClass (1 errors)
    - The location shall at least have a valid identifier or address or type
- ❌ AUCoreMedicationStatementClass (1 errors)
    - Error from https://tx.fhir.org/r4: Error: The filter "concept in 929360061000036106" is not understood or supported
- ❌ AUCorePatientClass (3 errors)
    - IHI shall be an exactly 16 digit number
    - IHI prefix is 800360
    - IHI shall pass the Luhn algorithm check
- ❌ AUCoreBloodPressureClass (4 errors)
    - Slice 'Observation.component:SystolicBP': a matching slice is required, but not found
    - Slice 'Observation.component:DiastolicBP': a matching slice is required, but not found
    - Slice 'Observation.component:SystolicBP': a matching slice is required, but not found
    - Slice 'Observation.component:DiastolicBP': a matching slice is required, but not found

---

[← Back to Summary](./pipeline-parity-summary.md)
