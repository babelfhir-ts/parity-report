# davinci-cdex - Detailed Report (FHIR all)
Generated: 2026-09-04T19:55:27.361Z

Package: `hl7.fhir.us.davinci-cdex@2.1.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 7 | 7 | 100% |
| Random Validation Parity | 7 | 7 | 100% |
| Random Generation Validation + Parity | 1 | 7 | 14% |


---

## Empty Validation Parity Results

### ✅ Passing (7)
- ✅ CDexPatientDemographicsClass
- ✅ CDexPractitionerRoleClass
- ✅ CDEXSDCQuestionnaireResponseClass
- ✅ CDexParametersSubmitAttachmentClass
- ✅ CDexSignatureBundleClass
- ✅ CDexTaskAttachmentRequestClass
- ✅ CDexTaskDataRequestClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (7)
- ✅ CDexPatientDemographicsClass
- ✅ CDexPractitionerRoleClass
- ✅ CDEXSDCQuestionnaireResponseClass
- ✅ CDexParametersSubmitAttachmentClass
- ✅ CDexSignatureBundleClass
- ✅ CDexTaskAttachmentRequestClass
- ✅ CDexTaskDataRequestClass

### ❌ Failing (0)
_None_

---

## Random Generation Validation + Parity Results

### ✅ Passing (1)
- ✅ CDEXSDCQuestionnaireResponseClass

### ❌ Failing (6)
- ❌ CDexPatientDemographicsClass (1 errors)
    - Value 'id-40mg49ud' is not exactly equal to fixed value 'patient'
- ❌ CDexPractitionerRoleClass (1 errors)
    - Value 'id-414j234d' is not exactly equal to fixed value 'practitionerrole'
- ❌ CDexParametersSubmitAttachmentClass (1 errors)
    - Cannot generate factory method for type Hl7.Fhir.Model.Resource: there is no default constructor.
- ❌ CDexSignatureBundleClass (2 errors)
    - Missing required member: 'data'
    - No elements matched required slice: 'type:verify'
- ❌ CDexTaskAttachmentRequestClass (2 errors)
    - Resource has no 'resourceType' property. At line 17, position 6.
    - Resource has no 'resourceType' property. At line 23, position 6.
- ❌ CDexTaskDataRequestClass (1 errors)
    - Instance failed constraint cdex-7 "If code = "data-request-code", must have one "code" input."

---

[← Back to Summary](./pipeline-parity-summary.md)
