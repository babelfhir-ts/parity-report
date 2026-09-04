# ndh - Detailed Report (FHIR all)
Generated: 2026-09-04T19:59:38.190Z

Package: `hl7.fhir.us.ndh@1.0.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 31 | 31 | 100% |
| Random Validation Parity | 31 | 31 | 100% |
| Random Generation Validation + Parity | 23 | 31 | 74% |


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

## Random Generation Validation + Parity Results

### ✅ Passing (23)
- ✅ NdhCareTeamClass
- ✅ NdhLocationClass
- ✅ NdhNdApiCareTeamClass
- ✅ NdhNdApiLocationClass
- ✅ NdhNdApiOrganizationClass
- ✅ NdhOrganizationClass
- ✅ NdhPnLdApiLocationClass
- ✅ NdhPnLdApiOrganizationClass
- ✅ NdhPnLdApiPractitionerClass
- ✅ NdhPnLdApiPractitionerRoleClass
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

---

[← Back to Summary](./pipeline-parity-summary.md)
