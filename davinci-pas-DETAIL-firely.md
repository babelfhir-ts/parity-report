# davinci-pas - Detailed Report (FHIR all)
Generated: 2026-08-29T11:15:31.235Z

Package: `hl7.fhir.us.davinci-pas@2.2.1`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 22 | 22 | 100% |
| Random Validation Parity | 21 | 22 | 95% |
| Random Generation Validation + Parity | 15 | 22 | 68% |


---

## Empty Validation Parity Results

### ✅ Passing (22)
- ✅ PASCoverageClass
- ✅ PASDocumentReferenceClass
- ✅ PASLocationClass
- ✅ PASMedicationRequestClass
- ✅ PASOrganizationClass
- ✅ PASPractitionerClass
- ✅ PASPractitionerRoleClass
- ✅ PASServiceRequestClass
- ✅ PASBeneficiaryClass
- ✅ PASClaimInquiryResponseClass
- ✅ PASClaimResponseBaseClass
- ✅ PASClaimResponseClass
- ✅ PASCommunicationRequestClass
- ✅ PASInquiryRequestBundleClass
- ✅ PASInquiryResponseBundleClass
- ✅ PASInsurerClass
- ✅ PASNutritionOrderClass
- ✅ PASRequestBundleClass
- ✅ PASRequestorClass
- ✅ PASResponseBundleClass
- ✅ PASSubscriberClass
- ✅ PASSubscriptionClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (21)
- ✅ PASCoverageClass
- ✅ PASDocumentReferenceClass
- ✅ PASLocationClass
- ✅ PASMedicationRequestClass
- ✅ PASOrganizationClass
- ✅ PASPractitionerClass
- ✅ PASPractitionerRoleClass
- ✅ PASServiceRequestClass
- ✅ PASBeneficiaryClass
- ✅ PASClaimInquiryResponseClass
- ✅ PASClaimResponseBaseClass
- ✅ PASClaimResponseClass
- ✅ PASCommunicationRequestClass
- ✅ PASInquiryRequestBundleClass
- ✅ PASInquiryResponseBundleClass
- ✅ PASInsurerClass
- ✅ PASNutritionOrderClass
- ✅ PASRequestorClass
- ✅ PASResponseBundleClass
- ✅ PASSubscriberClass
- ✅ PASSubscriptionClass

### ❌ Failing (1)
- ❌ PASRequestBundleClass
  - Field-level comparison:
  Both validators: unclassified
  Only Internal: constraint, related, extension


---

## Random Generation Validation + Parity Results

### ✅ Passing (15)
- ✅ PASLocationClass
- ✅ PASMedicationRequestClass
- ✅ PASOrganizationClass
- ✅ PASPractitionerClass
- ✅ PASPractitionerRoleClass
- ✅ PASServiceRequestClass
- ✅ PASBeneficiaryClass
- ✅ PASClaimInquiryResponseClass
- ✅ PASClaimResponseBaseClass
- ✅ PASClaimResponseClass
- ✅ PASInsurerClass
- ✅ PASNutritionOrderClass
- ✅ PASRequestorClass
- ✅ PASSubscriberClass
- ✅ PASSubscriptionClass

### ❌ Failing (7)
- ❌ PASCoverageClass (1 errors)
    - Instance failed constraint self-beneficiary "If relationship does not equal 'self', then subscriber SHALL be present."
- ❌ PASDocumentReferenceClass (1 errors)
    - Instance count at element 'url' is 1, which is not within the specified cardinality of 0..0
- ❌ PASCommunicationRequestClass (1 errors)
    - Instance failed constraint IdentifierUnlessVO "CommunicationRequest.identifier is required unless CommunicationRequest.medium is 'VO'."
- ❌ PASInquiryRequestBundleClass (2 errors)
    - Unable to resolve reference to profile 'http://hl7.org/fhir/us/davinci-pas/StructureDefinition/profile-claim-inquiry|2.2.1'. Details: Encountered an error while loading schema 'http://hl7.org/fhir/us/davinci-pas/StructureDefinition/profile-claim-inquiry|2.2.1': Failed to convert ElementDefinition at Claim.careTeam:OverallClaimMember in profile http://hl7.org/fhir/us/davinci-pas/StructureDefinition/profile-claim-inquiry: The value discriminator should have a 'fixed[x]', 'pattern[x]' or binding element set on 'boolean'.
    - Unable to resolve reference to profile 'http://hl7.org/fhir/us/davinci-pas/StructureDefinition/profile-claim-inquiry|2.2.1'. Details: Encountered an error while loading schema 'http://hl7.org/fhir/us/davinci-pas/StructureDefinition/profile-claim-inquiry|2.2.1': Failed to convert ElementDefinition at Claim.careTeam:OverallClaimMember in profile http://hl7.org/fhir/us/davinci-pas/StructureDefinition/profile-claim-inquiry: The value discriminator should have a 'fixed[x]', 'pattern[x]' or binding element set on 'boolean'. (for slice Claim)
- ❌ PASInquiryResponseBundleClass (1 errors)
    - Instance failed constraint ClaimResponseFirst "A Prior Authorization Response Bundle must have the PAS Response as the first resource"
- ❌ PASRequestBundleClass (4 errors)
    - Unable to resolve reference to profile 'http://hl7.org/fhir/us/davinci-pas/StructureDefinition/profile-claim-update|2.2.1'. Details: Encountered an error while loading schema 'http://hl7.org/fhir/us/davinci-pas/StructureDefinition/profile-claim-update|2.2.1': Failed to convert ElementDefinition at Claim.careTeam:OverallClaimMember in profile http://hl7.org/fhir/us/davinci-pas/StructureDefinition/profile-claim-update: The value discriminator should have a 'fixed[x]', 'pattern[x]' or binding element set on 'boolean'.
    - Element does not validate against any of the expected profiles (http://hl7.org/fhir/us/davinci-pas/StructureDefinition/profile-claim-update|2.2.1, http://hl7.org/fhir/us/davinci-pas/StructureDefinition/profile-claim|2.2.1). (for slice Claim)
    - Unable to resolve reference to profile 'http://hl7.org/fhir/us/davinci-pas/StructureDefinition/profile-claim-update|2.2.1'. Details: Encountered an error while loading schema 'http://hl7.org/fhir/us/davinci-pas/StructureDefinition/profile-claim-update|2.2.1': Failed to convert ElementDefinition at Claim.careTeam:OverallClaimMember in profile http://hl7.org/fhir/us/davinci-pas/StructureDefinition/profile-claim-update: The value discriminator should have a 'fixed[x]', 'pattern[x]' or binding element set on 'boolean'. (for slice Claim)
    - Unable to resolve reference to profile 'http://hl7.org/fhir/us/davinci-pas/StructureDefinition/profile-claim|2.2.1'. Details: Encountered an error while loading schema 'http://hl7.org/fhir/us/davinci-pas/StructureDefinition/profile-claim|2.2.1': Failed to convert ElementDefinition at Claim.careTeam:OverallClaimMember in profile http://hl7.org/fhir/us/davinci-pas/StructureDefinition/profile-claim: The value discriminator should have a 'fixed[x]', 'pattern[x]' or binding element set on 'boolean'. (for slice Claim)
- ❌ PASResponseBundleClass (1 errors)
    - Missing required member: 'request'

---

[← Back to Summary](./pipeline-parity-summary.md)
