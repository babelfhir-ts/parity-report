# davinci-pas - Detailed Report (FHIR all)
Generated: 2026-09-04T20:58:02.460Z

Package: `hl7.fhir.us.davinci-pas@2.2.1`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 29 | 29 | 100% |
| Random Validation Parity | 29 | 29 | 100% |
| Random Generation Validation + Parity | 20 | 29 | 69% |


---

## Empty Validation Parity Results

### ✅ Passing (29)
- ✅ PASCoverageClass
- ✅ PASDocumentReferenceClass
- ✅ PASEncounterClass
- ✅ PASLocationClass
- ✅ PASMedicationRequestClass
- ✅ PASOrganizationClass
- ✅ PASPractitionerClass
- ✅ PASPractitionerRoleClass
- ✅ PASServiceRequestClass
- ✅ PASBeneficiaryClass
- ✅ PASClaimBaseClass
- ✅ PASClaimClass
- ✅ PASClaimInquiryClass
- ✅ PASClaimInquiryResponseClass
- ✅ PASClaimResponseBaseClass
- ✅ PASClaimResponseClass
- ✅ PASClaimUpdateClass
- ✅ PASCommunicationRequestClass
- ✅ PASDeviceRequestClass
- ✅ PASInquiryRequestBundleClass
- ✅ PASInquiryResponseBundleClass
- ✅ PASInsurerClass
- ✅ PASNutritionOrderClass
- ✅ PASRequestBundleClass
- ✅ PASRequestorClass
- ✅ PASResponseBundleClass
- ✅ PASSubscriberClass
- ✅ PASSubscriptionClass
- ✅ PASTaskClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (29)
- ✅ PASCoverageClass
- ✅ PASDocumentReferenceClass
- ✅ PASEncounterClass
- ✅ PASLocationClass
- ✅ PASMedicationRequestClass
- ✅ PASOrganizationClass
- ✅ PASPractitionerClass
- ✅ PASPractitionerRoleClass
- ✅ PASServiceRequestClass
- ✅ PASBeneficiaryClass
- ✅ PASClaimBaseClass
- ✅ PASClaimClass
- ✅ PASClaimInquiryClass
- ✅ PASClaimInquiryResponseClass
- ✅ PASClaimResponseBaseClass
- ✅ PASClaimResponseClass
- ✅ PASClaimUpdateClass
- ✅ PASCommunicationRequestClass
- ✅ PASDeviceRequestClass
- ✅ PASInquiryRequestBundleClass
- ✅ PASInquiryResponseBundleClass
- ✅ PASInsurerClass
- ✅ PASNutritionOrderClass
- ✅ PASRequestBundleClass
- ✅ PASRequestorClass
- ✅ PASResponseBundleClass
- ✅ PASSubscriberClass
- ✅ PASSubscriptionClass
- ✅ PASTaskClass

### ❌ Failing (0)
_None_

---

## Random Generation Validation + Parity Results

### ✅ Passing (20)
- ✅ PASEncounterClass
- ✅ PASLocationClass
- ✅ PASMedicationRequestClass
- ✅ PASOrganizationClass
- ✅ PASPractitionerClass
- ✅ PASPractitionerRoleClass
- ✅ PASServiceRequestClass
- ✅ PASBeneficiaryClass
- ✅ PASClaimBaseClass
- ✅ PASClaimInquiryClass
- ✅ PASClaimInquiryResponseClass
- ✅ PASClaimResponseBaseClass
- ✅ PASClaimResponseClass
- ✅ PASDeviceRequestClass
- ✅ PASInquiryRequestBundleClass
- ✅ PASInsurerClass
- ✅ PASNutritionOrderClass
- ✅ PASRequestorClass
- ✅ PASSubscriberClass
- ✅ PASSubscriptionClass

### ❌ Failing (9)
- ❌ PASCoverageClass (1 errors)
    - If relationship does not equal 'self', then subscriber SHALL be present.
- ❌ PASDocumentReferenceClass (1 errors)
    - DocumentReference.content.attachment.url: max allowed = 0, but found 1
- ❌ PASClaimClass (3 errors)
    - Claim.item.extension: minimum required = 2, but only found 1
    - Slice 'Claim.item.extension:requestType' for extension 'http://hl7.org/fhir/us/davinci-pas/StructureDefinition/extension-serviceItemRequestType': a matching slice is required, but not found
    - Slice 'Claim.item.extension:certificationType' for extension 'http://hl7.org/fhir/us/davinci-pas/StructureDefinition/extension-certificationType': a matching slice is required, but not found
- ❌ PASClaimUpdateClass (3 errors)
    - Claim.item.extension: minimum required = 2, but only found 1
    - Slice 'Claim.item.extension:requestType' for extension 'http://hl7.org/fhir/us/davinci-pas/StructureDefinition/extension-serviceItemRequestType': a matching slice is required, but not found
    - Slice 'Claim.item.extension:certificationType' for extension 'http://hl7.org/fhir/us/davinci-pas/StructureDefinition/extension-certificationType': a matching slice is required, but not found
- ❌ PASCommunicationRequestClass (1 errors)
    - CommunicationRequest.identifier is required unless CommunicationRequest.medium is 'VO'.
- ❌ PASInquiryResponseBundleClass (1 errors)
    - A Prior Authorization Response Bundle must have the PAS Response as the first resource
- ❌ PASRequestBundleClass (16 errors)
    - Claim.related: minimum required = 1, but only found 0
    - Claim.item.extension: minimum required = 2, but only found 0
    - Slice 'Claim.item.extension:requestType' for extension 'http://hl7.org/fhir/us/davinci-pas/StructureDefinition/extension-serviceItemRequestType': a matching slice is required, but not found
    - Slice 'Claim.item.extension:certificationType' for extension 'http://hl7.org/fhir/us/davinci-pas/StructureDefinition/extension-certificationType': a matching slice is required, but not found
    - Claim.item.location[x]: minimum required = 1, but only found 0
- ❌ PASResponseBundleClass (1 errors)
    - ClaimResponse.request: minimum required = 1, but only found 0
- ❌ PASTaskClass (9 errors)
    - Object must have some content
    - The extension URL must not contain a version
    - The Extension 'http://hl7.org/fhir/us/davinci-pas/StructureDefinition/extension-serviceLineNumber|2.2.1' definition allows for the types [positiveInt] but found type integer
    - Value is 'http://hl7.org/fhir/us/davinci-pas/StructureDefinition/extension-serviceLineNumber|2.2.1' but is fixed to 'http://hl7.org/fhir/us/davinci-pas/StructureDefinition/extension-serviceLineNumber' in the profile http://hl7.org/fhir/us/davinci-pas/StructureDefinition/extension-serviceLineNumber|2.2.1#Extension.url
    - Must have either extensions or value[x], not both

---

[← Back to Summary](./pipeline-parity-summary.md)
