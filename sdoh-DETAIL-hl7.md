# sdoh - Detailed Report (FHIR all)
Generated: 2026-09-04T19:59:24.936Z

Package: `hl7.fhir.us.sdoh-clinicalcare@2.3.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 20 | 20 | 100% |
| Random Validation Parity | 20 | 20 | 100% |
| Random Generation Validation + Parity | 18 | 20 | 90% |


---

## Empty Validation Parity Results

### ✅ Passing (20)
- ✅ SDOHCCConditionClass
- ✅ SDOHCCGoalClass
- ✅ SDOHCCLocationClass
- ✅ SDOHCCObservationAssessmentClass
- ✅ SDOHCCObservationEthnicityOMBClass
- ✅ SDOHCCObservationGenderIdentityClass
- ✅ SDOHCCObservationPersonalCharacteristicClass
- ✅ SDOHCCObservationPersonalPronounsClass
- ✅ SDOHCCObservationRaceOMBClass
- ✅ SDOHCCObservationRecordedSexGenderClass
- ✅ SDOHCCObservationScreeningResponseClass
- ✅ SDOHCCObservationSexualOrientationClass
- ✅ SDOHCCPractitionerRoleClass
- ✅ SDOHCCProcedureClass
- ✅ SDOHCCServiceRequestClass
- ✅ SDOHCCTaskForPatientClass
- ✅ SDOHCCConsentClass
- ✅ SDOHCCGroupClass
- ✅ SDOHCCHealthcareServiceClass
- ✅ SDOHCCTaskForReferralManagementClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (20)
- ✅ SDOHCCConditionClass
- ✅ SDOHCCGoalClass
- ✅ SDOHCCLocationClass
- ✅ SDOHCCObservationAssessmentClass
- ✅ SDOHCCObservationEthnicityOMBClass
- ✅ SDOHCCObservationGenderIdentityClass
- ✅ SDOHCCObservationPersonalCharacteristicClass
- ✅ SDOHCCObservationPersonalPronounsClass
- ✅ SDOHCCObservationRaceOMBClass
- ✅ SDOHCCObservationRecordedSexGenderClass
- ✅ SDOHCCObservationScreeningResponseClass
- ✅ SDOHCCObservationSexualOrientationClass
- ✅ SDOHCCPractitionerRoleClass
- ✅ SDOHCCProcedureClass
- ✅ SDOHCCServiceRequestClass
- ✅ SDOHCCTaskForPatientClass
- ✅ SDOHCCConsentClass
- ✅ SDOHCCGroupClass
- ✅ SDOHCCHealthcareServiceClass
- ✅ SDOHCCTaskForReferralManagementClass

### ❌ Failing (0)
_None_

---

## Random Generation Validation + Parity Results

### ✅ Passing (18)
- ✅ SDOHCCConditionClass
- ✅ SDOHCCGoalClass
- ✅ SDOHCCLocationClass
- ✅ SDOHCCObservationAssessmentClass
- ✅ SDOHCCObservationEthnicityOMBClass
- ✅ SDOHCCObservationGenderIdentityClass
- ✅ SDOHCCObservationPersonalCharacteristicClass
- ✅ SDOHCCObservationPersonalPronounsClass
- ✅ SDOHCCObservationRaceOMBClass
- ✅ SDOHCCObservationRecordedSexGenderClass
- ✅ SDOHCCObservationSexualOrientationClass
- ✅ SDOHCCPractitionerRoleClass
- ✅ SDOHCCProcedureClass
- ✅ SDOHCCServiceRequestClass
- ✅ SDOHCCTaskForPatientClass
- ✅ SDOHCCConsentClass
- ✅ SDOHCCGroupClass
- ✅ SDOHCCTaskForReferralManagementClass

### ❌ Failing (2)
- ❌ SDOHCCObservationScreeningResponseClass (1 errors)
    - None of the codings provided are in the value set 'US Core Survey Codes' (http://hl7.org/fhir/us/core/ValueSet/us-core-survey-codes|7.0.0), and a coding from this value set is required) (codes = http://loinc.org#26436-6)
- ❌ SDOHCCHealthcareServiceClass (5 errors)
    - Object must have some content
    - Must have either extensions or value[x], not both
    - Extension.url is required in order to identify, use and validate the extension
    - Extension.url: minimum required = 1, but only found 0
    - Slice 'HealthcareService.telecom:AppointmentContact': a matching slice is required, but not found

---

[← Back to Summary](./pipeline-parity-summary.md)
