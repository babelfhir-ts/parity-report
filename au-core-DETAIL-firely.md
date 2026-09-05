# au-core - Detailed Report (FHIR all)
Generated: 2026-09-05T11:25:16.317Z

Package: `hl7.fhir.au.core@2.0.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 20 | 20 | 100% |
| Random Validation Parity | 20 | 20 | 100% |
| Random Generation Validation + Parity | 16 | 20 | 80% |


---

## Empty Validation Parity Results

### ✅ Passing (20)
- ✅ AUCoreAllergyIntoleranceClass
- ✅ AUCoreConditionClass
- ✅ AUCoreEncounterClass
- ✅ AUCoreLocationClass
- ✅ AUCoreMedicationStatementClass
- ✅ AUCoreOrganizationClass
- ✅ AUCorePatientClass
- ✅ AUCorePractitionerClass
- ✅ AUCorePractitionerRoleClass
- ✅ AUCoreProcedureClass
- ✅ AUCoreBodyHeightClass
- ✅ AUCoreBodyTemperatureClass
- ✅ AUCoreBodyWeightClass
- ✅ AUCoreDiagnosticResultClass
- ✅ AUCoreHealthcareServiceClass
- ✅ AUCoreHeartRateClass
- ✅ AUCoreRelatedPersonClass
- ✅ AUCoreRespirationRateClass
- ✅ AUCoreSmokingStatusClass
- ✅ AUCoreWaistCircumferenceClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (20)
- ✅ AUCoreAllergyIntoleranceClass
- ✅ AUCoreConditionClass
- ✅ AUCoreEncounterClass
- ✅ AUCoreLocationClass
- ✅ AUCoreMedicationStatementClass
- ✅ AUCoreOrganizationClass
- ✅ AUCorePatientClass
- ✅ AUCorePractitionerClass
- ✅ AUCorePractitionerRoleClass
- ✅ AUCoreProcedureClass
- ✅ AUCoreBodyHeightClass
- ✅ AUCoreBodyTemperatureClass
- ✅ AUCoreBodyWeightClass
- ✅ AUCoreDiagnosticResultClass
- ✅ AUCoreHealthcareServiceClass
- ✅ AUCoreHeartRateClass
- ✅ AUCoreRelatedPersonClass
- ✅ AUCoreRespirationRateClass
- ✅ AUCoreSmokingStatusClass
- ✅ AUCoreWaistCircumferenceClass

### ❌ Failing (0)
_None_

---

## Random Generation Validation + Parity Results

### ✅ Passing (16)
- ✅ AUCoreAllergyIntoleranceClass
- ✅ AUCoreConditionClass
- ✅ AUCoreEncounterClass
- ✅ AUCoreMedicationStatementClass
- ✅ AUCoreOrganizationClass
- ✅ AUCoreProcedureClass
- ✅ AUCoreBodyHeightClass
- ✅ AUCoreBodyTemperatureClass
- ✅ AUCoreBodyWeightClass
- ✅ AUCoreDiagnosticResultClass
- ✅ AUCoreHealthcareServiceClass
- ✅ AUCoreHeartRateClass
- ✅ AUCoreRelatedPersonClass
- ✅ AUCoreRespirationRateClass
- ✅ AUCoreSmokingStatusClass
- ✅ AUCoreWaistCircumferenceClass

### ❌ Failing (4)
- ❌ AUCoreLocationClass (1 errors)
    - Instance failed constraint au-core-loc-01 "The location shall at least have a valid identifier or address or type"
- ❌ AUCorePatientClass (3 errors)
    - Instance failed constraint inv-ihi-value-0 "IHI shall be an exactly 16 digit number" (for slice ihi)
    - Instance failed constraint inv-ihi-value-1 "IHI prefix is 800360" (for slice ihi)
    - Instance failed constraint inv-ihi-value-2 "IHI shall pass the Luhn algorithm check" (for slice ihi)
- ❌ AUCorePractitionerClass (6 errors)
    - Instance failed constraint inv-hpii-0 "HPI-I shall be 16 digits" (for slice hpii)
    - Instance failed constraint inv-hpii-1 "HPI-I prefix shall be 800361" (for slice hpii)
    - Instance failed constraint inv-hpii-2 "HPI-I shall pass the Luhn algorithm check" (for slice hpii)
    - Missing required member: 'type' (for slice hpii)
    - Value 'urn:ietf:rfc:3986' is not exactly equal to fixed value 'http://ns.electronichealth.net.au/id/hi/hpii/1.0' (for slice hpii)
- ❌ AUCorePractitionerRoleClass (2 errors)
    - Missing required member: 'type' (for slice medicareProvider)
    - Value 'urn:ietf:rfc:3986' is not exactly equal to fixed value 'http://ns.electronichealth.net.au/id/medicare-provider-number' (for slice medicareProvider)

---

[← Back to Summary](./pipeline-parity-summary.md)
