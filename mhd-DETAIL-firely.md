# mhd - Detailed Report (FHIR all)
Generated: 2026-09-05T11:32:28.886Z

Package: `ihe.iti.mhd@4.2.4`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 30 | 30 | 100% |
| Random Validation Parity | 25 | 30 | 83% |
| Random Generation Validation + Parity | 10 | 30 | 33% |


---

## Empty Validation Parity Results

### ✅ Passing (30)
- ✅ AuditFindDocumentReferencesConsumerClass
- ✅ AuditFindDocumentReferencesResponderClass
- ✅ ComprehensiveDocumentReferenceClass
- ✅ FindDocumentReferencesComprehensiveResponseClass
- ✅ MinimalDocumentReferenceClass
- ✅ SimplifiedPublishDocumentReferenceClass
- ✅ UnContainedComprehensiveDocumentReferenceClass
- ✅ AuditFindDocumentListsConsumerClass
- ✅ AuditFindDocumentListsResponderClass
- ✅ AuditGenerateMetadataRecipientClass
- ✅ AuditGenerateMetadataSourceClass
- ✅ AuditProvideBundleRecipientClass
- ✅ AuditProvideBundleSourceClass
- ✅ AuditRetrieveDocumentConsumerClass
- ✅ AuditRetrieveDocumentResponderClass
- ✅ AuditSimplifiedPublishRecipientClass
- ✅ AuditSimplifiedPublishSourceClass
- ✅ ComprehensiveProvideDocumentBundleClass
- ✅ FindListsResponseClass
- ✅ FolderClass
- ✅ FolderComprehensiveClass
- ✅ MHDgenerateMetadataParametersInClass
- ✅ MhdListClass
- ✅ MinimalProvideDocumentBundleClass
- ✅ PatchParametersClass
- ✅ ProvideDocumentBundleResponseClass
- ✅ SubmissionSetClass
- ✅ SubmissionSetComprehensiveClass
- ✅ SubmissionSetComprehensiveUnContainedClass
- ✅ UnContainedComprehensiveProvideDocumentBundleClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (25)
- ✅ AuditFindDocumentReferencesConsumerClass
- ✅ AuditFindDocumentReferencesResponderClass
- ✅ ComprehensiveDocumentReferenceClass
- ✅ FindDocumentReferencesComprehensiveResponseClass
- ✅ MinimalDocumentReferenceClass
- ✅ SimplifiedPublishDocumentReferenceClass
- ✅ UnContainedComprehensiveDocumentReferenceClass
- ✅ AuditFindDocumentListsConsumerClass
- ✅ AuditFindDocumentListsResponderClass
- ✅ AuditGenerateMetadataRecipientClass
- ✅ AuditGenerateMetadataSourceClass
- ✅ AuditProvideBundleRecipientClass
- ✅ AuditProvideBundleSourceClass
- ✅ AuditRetrieveDocumentConsumerClass
- ✅ AuditRetrieveDocumentResponderClass
- ✅ AuditSimplifiedPublishRecipientClass
- ✅ AuditSimplifiedPublishSourceClass
- ✅ FindListsResponseClass
- ✅ FolderClass
- ✅ FolderComprehensiveClass
- ✅ MHDgenerateMetadataParametersInClass
- ✅ MhdListClass
- ✅ SubmissionSetClass
- ✅ SubmissionSetComprehensiveClass
- ✅ SubmissionSetComprehensiveUnContainedClass

### ❌ Failing (5)
- ❌ ComprehensiveProvideDocumentBundleClass
  - Field-level comparison:
  Both validators: extension, code
  Only Internal: constraint
  Only Firely: pattern, entry, unclassified

- ❌ MinimalProvideDocumentBundleClass
  - Field-level comparison:
  Both validators: extension, code
  Only Internal: constraint
  Only Firely: pattern, entry, unclassified

- ❌ PatchParametersClass
  - Field-level comparison:
  Both validators: none
  Only Firely: pattern

- ❌ ProvideDocumentBundleResponseClass
  - Field-level comparison:
  Both validators: none
  Only Internal: unclassified

- ❌ UnContainedComprehensiveProvideDocumentBundleClass
  - Field-level comparison:
  Both validators: extension, code
  Only Internal: constraint
  Only Firely: pattern, entry, unclassified


---

## Random Generation Validation + Parity Results

### ✅ Passing (10)
- ✅ FindDocumentReferencesComprehensiveResponseClass
- ✅ FindListsResponseClass
- ✅ FolderClass
- ✅ FolderComprehensiveClass
- ✅ MHDgenerateMetadataParametersInClass
- ✅ MhdListClass
- ✅ ProvideDocumentBundleResponseClass
- ✅ SubmissionSetClass
- ✅ SubmissionSetComprehensiveClass
- ✅ SubmissionSetComprehensiveUnContainedClass

### ❌ Failing (20)
- ❌ AuditFindDocumentReferencesConsumerClass (1 errors)
    - Instance failed constraint val-audit-source "The Audit Source is this agent too." (for slice client)
- ❌ AuditFindDocumentReferencesResponderClass (1 errors)
    - Instance failed constraint val-audit-source "The Audit Source is this agent too." (for slice server)
- ❌ ComprehensiveDocumentReferenceClass (3 errors)
    - Missing required member: 'type'
    - Instance count at element 'data' is 1, which is not within the specified cardinality of 0..0
    - Encountered a reference (Resource/id-ylsl7qo4) of kind 'Referenced', which is not one of the allowed kinds (Contained).
- ❌ MinimalDocumentReferenceClass (2 errors)
    - Missing required member: 'type'
    - Instance count at element 'data' is 1, which is not within the specified cardinality of 0..0
- ❌ SimplifiedPublishDocumentReferenceClass (1 errors)
    - Instance count at element 'url' is 1, which is not within the specified cardinality of 0..0
- ❌ UnContainedComprehensiveDocumentReferenceClass (2 errors)
    - Missing required member: 'type'
    - Instance count at element 'data' is 1, which is not within the specified cardinality of 0..0
- ❌ AuditFindDocumentListsConsumerClass (1 errors)
    - Instance failed constraint val-audit-source "The Audit Source is this agent too." (for slice client)
- ❌ AuditFindDocumentListsResponderClass (1 errors)
    - Instance failed constraint val-audit-source "The Audit Source is this agent too." (for slice server)
- ❌ AuditGenerateMetadataRecipientClass (1 errors)
    - Instance failed constraint val-audit-source "The Audit Source is this agent too." (for slice server)
- ❌ AuditGenerateMetadataSourceClass (1 errors)
    - Instance failed constraint val-audit-source "The Audit Source is this agent too." (for slice client)
- ❌ AuditProvideBundleRecipientClass (1 errors)
    - Instance failed constraint val-audit-source "The Audit Source is this agent too." (for slice documentRecipient)
- ❌ AuditProvideBundleSourceClass (1 errors)
    - Instance failed constraint val-audit-source "The Audit Source is this agent too." (for slice documentSource)
- ❌ AuditRetrieveDocumentConsumerClass (1 errors)
    - Instance failed constraint val-audit-source "The Audit Source is this agent too." (for slice client)
- ❌ AuditRetrieveDocumentResponderClass (1 errors)
    - Instance failed constraint val-audit-source "The Audit Source is this agent too." (for slice server)
- ❌ AuditSimplifiedPublishRecipientClass (1 errors)
    - Instance failed constraint val-audit-source "The Audit Source is this agent too." (for slice server)
- ❌ AuditSimplifiedPublishSourceClass (1 errors)
    - Instance failed constraint val-audit-source "The Audit Source is this agent too." (for slice client)
- ❌ ComprehensiveProvideDocumentBundleClass (7 errors)
    - Missing required member: 'extension'
    - No elements matched required slice: 'extension:designationType'
    - No elements matched required slice: 'extension:sourceId'
    - Value '{"coding":[{"system":"http://loinc.org","code":"57024-2"}]}' does not match pattern '{"coding":[{"system":"https://profiles.ihe.net/ITI/MHD/CodeSystem/MHDlistTypes","code":"submissionset"}]}'
    - Code '57024-2' from system 'http://loinc.org' does not exist in the value set 'MHD List Types ValueSet' (https://profiles.ihe.net/ITI/MHD/ValueSet/MHDlistTypesVS), but the binding is of strength 'required'
- ❌ MinimalProvideDocumentBundleClass (6 errors)
    - Missing required member: 'extension'
    - No elements matched required slice: 'extension:sourceId'
    - Value '{"coding":[{"system":"http://loinc.org","code":"57024-2"}]}' does not match pattern '{"coding":[{"system":"https://profiles.ihe.net/ITI/MHD/CodeSystem/MHDlistTypes","code":"submissionset"}]}'
    - Code '57024-2' from system 'http://loinc.org' does not exist in the value set 'MHD List Types ValueSet' (https://profiles.ihe.net/ITI/MHD/ValueSet/MHDlistTypesVS), but the binding is of strength 'required'
    - No elements matched required slice: 'entry:SubmissionSet'
- ❌ PatchParametersClass (1 errors)
    - Value 'placeholder' does not match pattern 'DocumentReference.status' (for slice valueString)
- ❌ UnContainedComprehensiveProvideDocumentBundleClass (7 errors)
    - Missing required member: 'extension'
    - No elements matched required slice: 'extension:designationType'
    - No elements matched required slice: 'extension:sourceId'
    - Value '{"coding":[{"system":"http://loinc.org","code":"57024-2"}]}' does not match pattern '{"coding":[{"system":"https://profiles.ihe.net/ITI/MHD/CodeSystem/MHDlistTypes","code":"submissionset"}]}'
    - Code '57024-2' from system 'http://loinc.org' does not exist in the value set 'MHD List Types ValueSet' (https://profiles.ihe.net/ITI/MHD/ValueSet/MHDlistTypesVS), but the binding is of strength 'required'

---

[← Back to Summary](./pipeline-parity-summary.md)
