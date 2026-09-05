# mhd - Detailed Report (FHIR all)
Generated: 2026-09-05T11:27:10.448Z

Package: `ihe.iti.mhd@4.2.4`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 31 | 31 | 100% |
| Random Validation Parity | 31 | 31 | 100% |
| Random Generation Validation + Parity | 11 | 31 | 35% |


---

## Empty Validation Parity Results

### ✅ Passing (31)
- ✅ AuditFindDocumentReferencesConsumerClass
- ✅ AuditFindDocumentReferencesResponderClass
- ✅ ComprehensiveDocumentReferenceClass
- ✅ FindDocumentReferencesComprehensiveResponseClass
- ✅ FindDocumentReferencesResponseClass
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

### ✅ Passing (31)
- ✅ AuditFindDocumentReferencesConsumerClass
- ✅ AuditFindDocumentReferencesResponderClass
- ✅ ComprehensiveDocumentReferenceClass
- ✅ FindDocumentReferencesComprehensiveResponseClass
- ✅ FindDocumentReferencesResponseClass
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

## Random Generation Validation + Parity Results

### ✅ Passing (11)
- ✅ FindDocumentReferencesComprehensiveResponseClass
- ✅ FindDocumentReferencesResponseClass
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
    - The Audit Source is this agent too.
- ❌ AuditFindDocumentReferencesResponderClass (1 errors)
    - The Audit Source is this agent too.
- ❌ ComprehensiveDocumentReferenceClass (3 errors)
    - Identifier.type: minimum required = 1, but only found 0
    - DocumentReference.content.attachment.data: max allowed = 0, but found 1
    - Bundled or contained reference not found within the bundle/resource Resource/id-ylsl7qo4
- ❌ MinimalDocumentReferenceClass (2 errors)
    - Identifier.type: minimum required = 1, but only found 0
    - DocumentReference.content.attachment.data: max allowed = 0, but found 1
- ❌ SimplifiedPublishDocumentReferenceClass (1 errors)
    - DocumentReference.content.attachment.url: max allowed = 0, but found 1
- ❌ UnContainedComprehensiveDocumentReferenceClass (2 errors)
    - Identifier.type: minimum required = 1, but only found 0
    - DocumentReference.content.attachment.data: max allowed = 0, but found 1
- ❌ AuditFindDocumentListsConsumerClass (1 errors)
    - The Audit Source is this agent too.
- ❌ AuditFindDocumentListsResponderClass (1 errors)
    - The Audit Source is this agent too.
- ❌ AuditGenerateMetadataRecipientClass (1 errors)
    - The Audit Source is this agent too.
- ❌ AuditGenerateMetadataSourceClass (1 errors)
    - The Audit Source is this agent too.
- ❌ AuditProvideBundleRecipientClass (1 errors)
    - The Audit Source is this agent too.
- ❌ AuditProvideBundleSourceClass (1 errors)
    - The Audit Source is this agent too.
- ❌ AuditRetrieveDocumentConsumerClass (1 errors)
    - The Audit Source is this agent too.
- ❌ AuditRetrieveDocumentResponderClass (1 errors)
    - The Audit Source is this agent too.
- ❌ AuditSimplifiedPublishRecipientClass (1 errors)
    - The Audit Source is this agent too.
- ❌ AuditSimplifiedPublishSourceClass (1 errors)
    - The Audit Source is this agent too.
- ❌ ComprehensiveProvideDocumentBundleClass (7 errors)
    - List.extension: minimum required = 2, but only found 0
    - Slice 'List.extension:designationType' for extension 'https://profiles.ihe.net/ITI/MHD/StructureDefinition/ihe-designationType': a matching slice is required, but not found
    - Slice 'List.extension:sourceId' for extension 'https://profiles.ihe.net/ITI/MHD/StructureDefinition/ihe-sourceId': a matching slice is required, but not found
    - The pattern [system https://profiles.ihe.net/ITI/MHD/CodeSystem/MHDlistTypes, code submissionset, and display 'null'] defined in the profile https://profiles.ihe.net/ITI/MHD/StructureDefinition/IHE.MHD.Comprehensive.SubmissionSet|4.2.4 not found. Issues: [ValidationMessage[level=ERROR,type=VALUE,location=Bundle.entry[0].resource/*List/id-1fb44nv1*/.code.coding.system,message=Value is 'http://loinc.org' but is fixed to 'https://profiles.ihe.net/ITI/MHD/CodeSystem/MHDlistTypes' in the profile https://profiles.ihe.net/ITI/MHD/StructureDefinition/IHE.MHD.Comprehensive.SubmissionSet|4.2.4#List], ValidationMessage[level=ERROR,type=VALUE,location=Bundle.entry[0].resource/*List/id-1fb44nv1*/.code.coding.code,message=Value is '57024-2' but is fixed to 'submissionset' in the profile https://profiles.ihe.net/ITI/MHD/StructureDefinition/IHE.MHD.Comprehensive.SubmissionSet|4.2.4#List]]
    - None of the codings provided are in the value set 'MHD List Types ValueSet' (https://profiles.ihe.net/ITI/MHD/ValueSet/MHDlistTypesVS|4.2.4), and a coding from this value set is required) (codes = http://loinc.org#57024-2)
- ❌ MinimalProvideDocumentBundleClass (6 errors)
    - List.extension: minimum required = 1, but only found 0
    - Slice 'List.extension:sourceId' for extension 'https://profiles.ihe.net/ITI/MHD/StructureDefinition/ihe-sourceId': a matching slice is required, but not found
    - The pattern [system https://profiles.ihe.net/ITI/MHD/CodeSystem/MHDlistTypes, code submissionset, and display 'null'] defined in the profile https://profiles.ihe.net/ITI/MHD/StructureDefinition/IHE.MHD.Minimal.SubmissionSet|4.2.4 not found. Issues: [ValidationMessage[level=ERROR,type=VALUE,location=Bundle.entry[0].resource/*List/id-y2tv2y0r*/.code.coding.system,message=Value is 'http://loinc.org' but is fixed to 'https://profiles.ihe.net/ITI/MHD/CodeSystem/MHDlistTypes' in the profile https://profiles.ihe.net/ITI/MHD/StructureDefinition/IHE.MHD.Minimal.SubmissionSet|4.2.4#List], ValidationMessage[level=ERROR,type=VALUE,location=Bundle.entry[0].resource/*List/id-y2tv2y0r*/.code.coding.code,message=Value is '57024-2' but is fixed to 'submissionset' in the profile https://profiles.ihe.net/ITI/MHD/StructureDefinition/IHE.MHD.Minimal.SubmissionSet|4.2.4#List]]
    - None of the codings provided are in the value set 'MHD List Types ValueSet' (https://profiles.ihe.net/ITI/MHD/ValueSet/MHDlistTypesVS|4.2.4), and a coding from this value set is required) (codes = http://loinc.org#57024-2)
    - This element does not match any known slice defined in the profile https://profiles.ihe.net/ITI/MHD/StructureDefinition/IHE.MHD.Minimal.ProvideBundle|4.2.4 and slicing is CLOSED: Bundle.entry[0]: Does not match slice 'SubmissionSet' (discriminator: resource.conformsTo('https://profiles.ihe.net/ITI/MHD/StructureDefinition/IHE.MHD.Minimal.SubmissionSet') and request.method.where(value = 'POST').exists()), Bundle.entry[0]: Details for Bundle matching against profile https://profiles.ihe.net/ITI/MHD/StructureDefinition/IHE.MHD.Minimal.SubmissionSet|4.2.4, Bundle.entry[0]: Does not match slice 'DocumentRefs' (discriminator: resource.conformsTo('https://profiles.ihe.net/ITI/MHD/StructureDefinition/IHE.MHD.Minimal.DocumentReference') and request.method.where(value = 'POST').exists()), Bundle.entry[0]: Details for Bundle matching against profile https://profiles.ihe.net/ITI/MHD/StructureDefinition/IHE.MHD.Minimal.DocumentReference|4.2.4, Bundle.entry[0]: Does not match slice 'UpdateDocumentRefs' (discriminator: resource.conformsTo('https://profiles.ihe.net/ITI/MHD/StructureDefinition/IHE.MHD.Patch.Parameters') and request.method.where(value = 'PATCH').exists()), Bundle.entry[0]: Details for Bundle matching against profile https://profiles.ihe.net/ITI/MHD/StructureDefinition/IHE.MHD.Patch.Parameters|4.2.4, Bundle.entry[0]: Does not match slice 'Documents' (discriminator: resource.conformsTo('http://hl7.org/fhir/StructureDefinition/Binary') and (request.method memberOf 'http://hl7.org/fhir/ValueSet/http-verb|4.0.1')), Bundle.entry[0]: Details for Bundle matching against profile http://hl7.org/fhir/StructureDefinition/Binary|4.0.1, Bundle.entry[0]: Does not match slice 'FhirDocuments' (discriminator: resource.conformsTo('http://hl7.org/fhir/StructureDefinition/Bundle') and request.method.where(value = 'POST').exists()), Bundle.entry[0]: Details for Bundle matching against profile http://hl7.org/fhir/StructureDefinition/Bundle|4.0.1, Bundle.entry[0]: Does not match slice 'Folders' (discriminator: resource.conformsTo('https://profiles.ihe.net/ITI/MHD/StructureDefinition/IHE.MHD.Minimal.Folder') and (request.method memberOf 'https://profiles.ihe.net/ITI/MHD/ValueSet/MHDprovideFolderActions')), Bundle.entry[0]: Details for Bundle matching against profile https://profiles.ihe.net/ITI/MHD/StructureDefinition/IHE.MHD.Minimal.Folder|4.2.4, Bundle.entry[0]: Does not match slice 'Patient' (discriminator: resource.conformsTo('http://hl7.org/fhir/StructureDefinition/Patient') and (request.method memberOf 'https://profiles.ihe.net/ITI/MHD/ValueSet/MHDprovidePatientActions')), Bundle.entry[0]: Details for Bundle matching against profile http://hl7.org/fhir/StructureDefinition/Patient|4.0.1
- ❌ PatchParametersClass (1 errors)
    - Value is 'placeholder' but is fixed to 'DocumentReference.status' in the profile https://profiles.ihe.net/ITI/MHD/StructureDefinition/IHE.MHD.Patch.Parameters|4.2.4#Parameters.parameter:operation.part:path.value[x]:valueString
- ❌ UnContainedComprehensiveProvideDocumentBundleClass (7 errors)
    - List.extension: minimum required = 2, but only found 0
    - Slice 'List.extension:designationType' for extension 'https://profiles.ihe.net/ITI/MHD/StructureDefinition/ihe-designationType': a matching slice is required, but not found
    - Slice 'List.extension:sourceId' for extension 'https://profiles.ihe.net/ITI/MHD/StructureDefinition/ihe-sourceId': a matching slice is required, but not found
    - The pattern [system https://profiles.ihe.net/ITI/MHD/CodeSystem/MHDlistTypes, code submissionset, and display 'null'] defined in the profile https://profiles.ihe.net/ITI/MHD/StructureDefinition/IHE.MHD.UnContained.Comprehensive.SubmissionSet|4.2.4 not found. Issues: [ValidationMessage[level=ERROR,type=VALUE,location=Bundle.entry[0].resource/*List/id-o78v1kjr*/.code.coding.system,message=Value is 'http://loinc.org' but is fixed to 'https://profiles.ihe.net/ITI/MHD/CodeSystem/MHDlistTypes' in the profile https://profiles.ihe.net/ITI/MHD/StructureDefinition/IHE.MHD.UnContained.Comprehensive.SubmissionSet|4.2.4#List], ValidationMessage[level=ERROR,type=VALUE,location=Bundle.entry[0].resource/*List/id-o78v1kjr*/.code.coding.code,message=Value is '57024-2' but is fixed to 'submissionset' in the profile https://profiles.ihe.net/ITI/MHD/StructureDefinition/IHE.MHD.UnContained.Comprehensive.SubmissionSet|4.2.4#List]]
    - None of the codings provided are in the value set 'MHD List Types ValueSet' (https://profiles.ihe.net/ITI/MHD/ValueSet/MHDlistTypesVS|4.2.4), and a coding from this value set is required) (codes = http://loinc.org#57024-2)

---

[← Back to Summary](./pipeline-parity-summary.md)
