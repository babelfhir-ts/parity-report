# sdoh - Detailed Report (FHIR all)
Generated: 2026-08-29T11:15:22.965Z

Package: `hl7.fhir.us.sdoh-clinicalcare@2.3.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 16 | 16 | 100% |
| Random Validation Parity | 15 | 16 | 94% |
| Random Generation Validation + Parity | 12 | 16 | 75% |


---

## Empty Validation Parity Results

### ✅ Passing (16)
- ✅ SDOHCCGoalClass
- ✅ SDOHCCLocationClass
- ✅ SDOHCCObservationAssessmentClass
- ✅ SDOHCCObservationGenderIdentityClass
- ✅ SDOHCCObservationPersonalCharacteristicClass
- ✅ SDOHCCObservationPersonalPronounsClass
- ✅ SDOHCCObservationRecordedSexGenderClass
- ✅ SDOHCCObservationScreeningResponseClass
- ✅ SDOHCCObservationSexualOrientationClass
- ✅ SDOHCCPractitionerRoleClass
- ✅ SDOHCCProcedureClass
- ✅ SDOHCCServiceRequestClass
- ✅ SDOHCCConsentClass
- ✅ SDOHCCGroupClass
- ✅ SDOHCCHealthcareServiceClass
- ✅ SDOHCCTaskForReferralManagementClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (15)
- ✅ SDOHCCGoalClass
- ✅ SDOHCCLocationClass
- ✅ SDOHCCObservationAssessmentClass
- ✅ SDOHCCObservationGenderIdentityClass
- ✅ SDOHCCObservationPersonalCharacteristicClass
- ✅ SDOHCCObservationPersonalPronounsClass
- ✅ SDOHCCObservationRecordedSexGenderClass
- ✅ SDOHCCObservationScreeningResponseClass
- ✅ SDOHCCObservationSexualOrientationClass
- ✅ SDOHCCPractitionerRoleClass
- ✅ SDOHCCProcedureClass
- ✅ SDOHCCServiceRequestClass
- ✅ SDOHCCConsentClass
- ✅ SDOHCCGroupClass
- ✅ SDOHCCTaskForReferralManagementClass

### ❌ Failing (1)
- ❌ SDOHCCHealthcareServiceClass
  - Field-level comparison:
  Both validators: url, extension
  Only Internal: telecom


---

## Random Generation Validation + Parity Results

### ✅ Passing (12)
- ✅ SDOHCCLocationClass
- ✅ SDOHCCObservationAssessmentClass
- ✅ SDOHCCObservationGenderIdentityClass
- ✅ SDOHCCObservationPersonalCharacteristicClass
- ✅ SDOHCCObservationPersonalPronounsClass
- ✅ SDOHCCObservationRecordedSexGenderClass
- ✅ SDOHCCObservationScreeningResponseClass
- ✅ SDOHCCObservationSexualOrientationClass
- ✅ SDOHCCPractitionerRoleClass
- ✅ SDOHCCConsentClass
- ✅ SDOHCCGroupClass
- ✅ SDOHCCTaskForReferralManagementClass

### ❌ Failing (4)
- ❌ SDOHCCGoalClass (1 errors)
    - Unable to resolve reference to profile 'http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-Goal'. Details: Encountered an error while loading schema 'http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-Goal': Failed to convert ElementDefinition at Goal.addresses:SupportedAddresses in profile http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-Goal: The discriminator path 'resolve()' at http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-Goal#Goal.addresses (Goal.addresses:SupportedAddresses) leads to multiple ElementDefinitions, which is not allowed.
- ❌ SDOHCCProcedureClass (1 errors)
    - Unable to resolve reference to profile 'http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-Procedure'. Details: Encountered an error while loading schema 'http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-Procedure': Failed to convert ElementDefinition at Procedure.basedOn:SupportedBasedOn in profile http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-Procedure: The discriminator path 'resolve()' at http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-Procedure#Procedure.basedOn (Procedure.basedOn:SupportedBasedOn) leads to multiple ElementDefinitions, which is not allowed.
- ❌ SDOHCCServiceRequestClass (1 errors)
    - Unable to resolve reference to profile 'http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-ServiceRequest'. Details: Encountered an error while loading schema 'http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-ServiceRequest': Failed to convert ElementDefinition at ServiceRequest.orderDetail:SubjectContactDetail in profile http://hl7.org/fhir/us/sdoh-clinicalcare/StructureDefinition/SDOHCC-ServiceRequest: The value discriminator should have a 'fixed[x]', 'pattern[x]' or binding element set on 'CodeableConcept.coding'.
- ❌ SDOHCCHealthcareServiceClass (1 errors)
    - One or more errors occurred. (An object needs to have at least one property. At HealthcareService.telecom[0].extension[0], line 20, position 8.)

---

[← Back to Summary](./pipeline-parity-summary.md)
