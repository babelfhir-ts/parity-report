# ndh - Detailed Report (FHIR all)
Generated: 2026-10-01T11:38:31.682Z

Package: `hl7.fhir.us.ndh@1.0.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 31 | 31 | 100% |
| Random Validation Parity | 30 | 30 | 100% |
| Random Generation Validation + Parity | 22 | 30 | 73% |
| Excluded (external issues) | 1 | - | - |

---

## Empty Validation Parity Results

### ✅ Passing (31)
- ✅ NdhCareTeamClass
- ✅ NdhLocationClass
- ✅ NdhNdApiCareTeamClass
- ✅ NdhNdApiLocationClass
- ✅ NdhNdApiOrganizationAffiliationClass
- ✅ NdhNdApiOrganizationClass
- ✅ NdhNdApiPractitionerClass
- ✅ NdhNdApiPractitionerRoleClass
- ✅ NdhOrganizationAffiliationClass
- ✅ NdhOrganizationClass
- ✅ NdhPnLdApiLocationClass
- ✅ NdhPnLdApiOrganizationAffiliationClass
- ✅ NdhPnLdApiOrganizationClass
- ✅ NdhPnLdApiPractitionerClass
- ✅ NdhPnLdApiPractitionerRoleClass
- ✅ NdhPractitionerClass
- ✅ NdhPractitionerRoleClass
- ✅ NdhEndpointClass
- ✅ NdhHealthcareServiceClass
- ✅ NdhInsurancePlanClass
- ✅ NdhNdApiEndpointClass
- ✅ NdhNdApiHealthcareServiceClass
- ✅ NdhNdApiInsurancePlanClass
- ✅ NdhNdApiNetworkClass
- ✅ NdhNetworkClass
- ✅ NdhPnLdApiEndpointClass
- ✅ NdhPnLdApiHealthcareServiceClass
- ✅ NdhPnLdApiInsurancePlanClass
- ✅ NdhPnLdApiNetworkClass
- ✅ NdhRestrictionClass
- ✅ NdhVerificationClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (30)
- ✅ NdhCareTeamClass
- ✅ NdhLocationClass
- ✅ NdhNdApiCareTeamClass
- ✅ NdhNdApiLocationClass
- ✅ NdhNdApiOrganizationAffiliationClass
- ✅ NdhNdApiOrganizationClass
- ✅ NdhNdApiPractitionerClass
- ✅ NdhNdApiPractitionerRoleClass
- ✅ NdhOrganizationAffiliationClass
- ✅ NdhOrganizationClass
- ✅ NdhPnLdApiLocationClass
- ✅ NdhPnLdApiOrganizationAffiliationClass
- ✅ NdhPnLdApiOrganizationClass
- ✅ NdhPnLdApiPractitionerClass
- ✅ NdhPractitionerClass
- ✅ NdhPractitionerRoleClass
- ✅ NdhEndpointClass
- ✅ NdhHealthcareServiceClass
- ✅ NdhInsurancePlanClass
- ✅ NdhNdApiEndpointClass
- ✅ NdhNdApiHealthcareServiceClass
- ✅ NdhNdApiInsurancePlanClass
- ✅ NdhNdApiNetworkClass
- ✅ NdhNetworkClass
- ✅ NdhPnLdApiEndpointClass
- ✅ NdhPnLdApiHealthcareServiceClass
- ✅ NdhPnLdApiInsurancePlanClass
- ✅ NdhPnLdApiNetworkClass
- ✅ NdhRestrictionClass
- ✅ NdhVerificationClass

### ❌ Failing (0)
_None_

### ⚠️ Excluded - External Issues (1)
- ⚠️ NdhPnLdApiPractitionerRoleClass (excluded - Terminology limitation)

---

## Random Generation Validation + Parity Results

### ✅ Passing (22)
- ✅ NdhCareTeamClass
- ✅ NdhLocationClass
- ✅ NdhNdApiCareTeamClass
- ✅ NdhNdApiLocationClass
- ✅ NdhNdApiOrganizationClass
- ✅ NdhOrganizationClass
- ✅ NdhPnLdApiLocationClass
- ✅ NdhPnLdApiOrganizationClass
- ✅ NdhPnLdApiPractitionerClass
- ✅ NdhPractitionerClass
- ✅ NdhPractitionerRoleClass
- ✅ NdhEndpointClass
- ✅ NdhHealthcareServiceClass
- ✅ NdhNdApiEndpointClass
- ✅ NdhNdApiHealthcareServiceClass
- ✅ NdhNdApiNetworkClass
- ✅ NdhNetworkClass
- ✅ NdhPnLdApiEndpointClass
- ✅ NdhPnLdApiHealthcareServiceClass
- ✅ NdhPnLdApiNetworkClass
- ✅ NdhRestrictionClass
- ✅ NdhVerificationClass

### ❌ Failing (8)
- ❌ NdhNdApiOrganizationAffiliationClass (1 errors)
    - NdhOrganizationAffiliation.organization or  NdhOrganizationAffiliation.participatingOrganization
- ❌ NdhNdApiPractitionerClass (3 errors)
    - The Extension 'http://hl7.org/fhir/us/ndh/StructureDefinition/base-ext-identifier-status' definition allows for the types [code] but found type string
    - The System URI could not be determined for the code 'Example' in the ValueSet 'http://hl7.org/fhir/us/ndh/ValueSet/IdentifierStatusVS|1.0.0'
    - The value provided ('Example') was not found in the value set 'Identifier Status Value Set' (http://hl7.org/fhir/us/ndh/ValueSet/IdentifierStatusVS|1.0.0), and a code is required from this value set  (error message = The System URI could not be determined for the code 'Example' in the ValueSet 'http://hl7.org/fhir/us/ndh/ValueSet/IdentifierStatusVS|1.0.0'; The provided code '#Example' was not found in the value set 'http://hl7.org/fhir/us/ndh/ValueSet/IdentifierStatusVS|1.0.0')
- ❌ NdhNdApiPractitionerRoleClass (3 errors)
    - The Extension 'http://hl7.org/fhir/us/ndh/StructureDefinition/base-ext-identifier-status' definition allows for the types [code] but found type string
    - The System URI could not be determined for the code 'Example' in the ValueSet 'http://hl7.org/fhir/us/ndh/ValueSet/IdentifierStatusVS|1.0.0'
    - The value provided ('Example') was not found in the value set 'Identifier Status Value Set' (http://hl7.org/fhir/us/ndh/ValueSet/IdentifierStatusVS|1.0.0), and a code is required from this value set  (error message = The System URI could not be determined for the code 'Example' in the ValueSet 'http://hl7.org/fhir/us/ndh/ValueSet/IdentifierStatusVS|1.0.0'; The provided code '#Example' was not found in the value set 'http://hl7.org/fhir/us/ndh/ValueSet/IdentifierStatusVS|1.0.0')
- ❌ NdhOrganizationAffiliationClass (1 errors)
    - NdhOrganizationAffiliation.organization or  NdhOrganizationAffiliation.participatingOrganization
- ❌ NdhPnLdApiOrganizationAffiliationClass (1 errors)
    - NdhOrganizationAffiliation.organization or  NdhOrganizationAffiliation.participatingOrganization
- ❌ NdhInsurancePlanClass (2 errors)
    - The organization SHALL at least have a name or an idendtifier, and possibly more than one
    - If an insuranceplan does not define a network, then each plan must define one
- ❌ NdhNdApiInsurancePlanClass (2 errors)
    - The organization SHALL at least have a name or an idendtifier, and possibly more than one
    - If an insuranceplan does not define a network, then each plan must define one
- ❌ NdhPnLdApiInsurancePlanClass (2 errors)
    - The organization SHALL at least have a name or an idendtifier, and possibly more than one
    - If an insuranceplan does not define a network, then each plan must define one

### ⚠️ Excluded - External Issues (1)
- ⚠️ NdhPnLdApiPractitionerRoleClass (excluded - Terminology limitation)
    - Unknown code '453231000124104' in the CodeSystem 'http://snomed.info/sct' version 'http://snomed.info/sct/900000000000207008/version/20250201' (International Edition)

---

[← Back to Summary](./pipeline-parity-summary.md)
