# davinci-cdex - Detailed Report (FHIR all)
Generated: 2026-09-04T20:54:15.834Z

Package: `hl7.fhir.us.davinci-cdex@2.1.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 7 | 7 | 100% |
| Random Validation Parity | 7 | 7 | 100% |
| Random Generation Validation + Parity | 2 | 7 | 29% |


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

### ✅ Passing (2)
- ✅ CDEXSDCQuestionnaireResponseClass
- ✅ CDexParametersSubmitAttachmentClass

### ❌ Failing (5)
- ❌ CDexPatientDemographicsClass (1 errors)
    - Value is 'id-40mg49ud' but is fixed to 'patient' in the profile http://hl7.org/fhir/us/davinci-cdex/StructureDefinition/cdex-patient-demographics|2.1.0#Patient.id
- ❌ CDexPractitionerRoleClass (1 errors)
    - Value is 'id-414j234d' but is fixed to 'practitionerrole' in the profile http://hl7.org/fhir/us/davinci-cdex/StructureDefinition/cdex-practitionerrole|2.1.0#PractitionerRole.id
- ❌ CDexSignatureBundleClass (2 errors)
    - Slice 'Signature.type:verify': a matching slice is required, but not found
    - Signature.data: minimum required = 1, but only found 0
- ❌ CDexTaskAttachmentRequestClass (15 errors)
    - Unable to find resourceType property
    - Unable to find resourceType property
    - Resource requires an id, but none is present
    - Resource requires an id, but none is present
    - Slice 'Task.contained:practitionerrole': a matching slice is required, but not found
- ❌ CDexTaskDataRequestClass (1 errors)
    - If code = "data-request-code", must have one "code" input.

---

[← Back to Summary](./pipeline-parity-summary.md)
