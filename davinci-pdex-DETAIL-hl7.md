# davinci-pdex - Detailed Report (FHIR all)
Generated: 2026-09-05T11:38:42.638Z

Package: `hl7.fhir.us.davinci-pdex@2.1.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 13 | 13 | 100% |
| Random Validation Parity | 13 | 13 | 100% |
| Random Generation Validation + Parity | 10 | 13 | 77% |


---

## Empty Validation Parity Results

### ✅ Passing (13)
- ✅ MtlsOrganizationClass
- ✅ PdexMedicationDispenseClass
- ✅ ProvenanceExtensionClass
- ✅ MtlsBundleClass
- ✅ MtlsEndpointClass
- ✅ PdexDeviceClass
- ✅ PDexMemberMatchGroupClass
- ✅ PDexMemberNoMatchGroupClass
- ✅ PDexMultiMemberMatchRequestParametersClass
- ✅ PDexMultiMemberMatchResponseParametersClass
- ✅ PdexPriorAuthorizationClass
- ✅ PDexProviderGroupClass
- ✅ PDexProviderSharingConsentClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (13)
- ✅ MtlsOrganizationClass
- ✅ PdexMedicationDispenseClass
- ✅ ProvenanceExtensionClass
- ✅ MtlsBundleClass
- ✅ MtlsEndpointClass
- ✅ PdexDeviceClass
- ✅ PDexMemberMatchGroupClass
- ✅ PDexMemberNoMatchGroupClass
- ✅ PDexMultiMemberMatchRequestParametersClass
- ✅ PDexMultiMemberMatchResponseParametersClass
- ✅ PdexPriorAuthorizationClass
- ✅ PDexProviderGroupClass
- ✅ PDexProviderSharingConsentClass

### ❌ Failing (0)
_None_

---

## Random Generation Validation + Parity Results

### ✅ Passing (10)
- ✅ MtlsOrganizationClass
- ✅ MtlsBundleClass
- ✅ MtlsEndpointClass
- ✅ PdexDeviceClass
- ✅ PDexMemberMatchGroupClass
- ✅ PDexMemberNoMatchGroupClass
- ✅ PDexMultiMemberMatchResponseParametersClass
- ✅ PdexPriorAuthorizationClass
- ✅ PDexProviderGroupClass
- ✅ PDexProviderSharingConsentClass

### ❌ Failing (3)
- ❌ PdexMedicationDispenseClass (1 errors)
    - None of the codings provided are in the value set 'FDA National Drug Code (NDC)' (http://hl7.org/fhir/us/davinci-pdex/ValueSet/FDANationalDrugCode|2.1.0), and a coding from this value set is required) (codes = http://www.nlm.nih.gov/research/umls/rxnorm#1043449)
- ❌ ProvenanceExtensionClass (2 errors)
    - None of the codings provided are in the value set 'Provenance Agent Type' (http://hl7.org/fhir/us/davinci-pdex/ValueSet/ProvenanceAgentType|2.1.0), and a coding from this value set is required) (codes = http://terminology.hl7.org/CodeSystem/provenance-participant-type#author)
    - None of the codings provided are in the value set 'US Core Provenance Participant Type Codes' (http://hl7.org/fhir/us/core/ValueSet/us-core-provenance-participant-type|7.0.0), and a coding from this value set is required) (codes = http://terminology.hl7.org/CodeSystem/provenance-participant-type#author)
- ❌ PDexMultiMemberMatchRequestParametersClass (2 errors)
    - Example URLs are not allowed in this context (http://example.org/policy)
    - Slice 'Consent.policy:hrex': a matching slice is required, but not found

---

[← Back to Summary](./pipeline-parity-summary.md)
