# ndh - Detailed Report (FHIR all)
Generated: 2026-09-04T19:53:55.981Z

Package: `hl7.fhir.us.ndh@1.0.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 28 | 28 | 100% |
| Random Validation Parity | 28 | 28 | 100% |
| Random Generation Validation + Parity | 21 | 28 | 75% |


---

## Empty Validation Parity Results

### ✅ Passing (28)
- ✅ NdhCareTeamClass
- ✅ NdhLocationClass
- ✅ NdhNdApiCareTeamClass
- ✅ NdhNdApiLocationClass
- ✅ NdhNdApiOrganizationAffiliationClass
- ✅ NdhNdApiOrganizationClass
- ✅ NdhNdApiPractitionerRoleClass
- ✅ NdhOrganizationAffiliationClass
- ✅ NdhOrganizationClass
- ✅ NdhPnLdApiLocationClass
- ✅ NdhPnLdApiOrganizationAffiliationClass
- ✅ NdhPnLdApiOrganizationClass
- ✅ NdhPnLdApiPractitionerRoleClass
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

### ✅ Passing (28)
- ✅ NdhCareTeamClass
- ✅ NdhLocationClass
- ✅ NdhNdApiCareTeamClass
- ✅ NdhNdApiLocationClass
- ✅ NdhNdApiOrganizationAffiliationClass
- ✅ NdhNdApiOrganizationClass
- ✅ NdhNdApiPractitionerRoleClass
- ✅ NdhOrganizationAffiliationClass
- ✅ NdhOrganizationClass
- ✅ NdhPnLdApiLocationClass
- ✅ NdhPnLdApiOrganizationAffiliationClass
- ✅ NdhPnLdApiOrganizationClass
- ✅ NdhPnLdApiPractitionerRoleClass
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

### ✅ Passing (21)
- ✅ NdhCareTeamClass
- ✅ NdhLocationClass
- ✅ NdhNdApiCareTeamClass
- ✅ NdhNdApiLocationClass
- ✅ NdhNdApiOrganizationClass
- ✅ NdhOrganizationClass
- ✅ NdhPnLdApiLocationClass
- ✅ NdhPnLdApiOrganizationClass
- ✅ NdhPnLdApiPractitionerRoleClass
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

### ❌ Failing (7)
- ❌ NdhNdApiOrganizationAffiliationClass (1 errors)
    - Instance failed constraint organization-or-participatingOrganization "NdhOrganizationAffiliation.organization or  NdhOrganizationAffiliation.participatingOrganization"
- ❌ NdhNdApiPractitionerRoleClass (4 errors)
    - Code 'Example' does not exist in the value set 'Identifier Status Value Set' (http://hl7.org/fhir/us/ndh/ValueSet/IdentifierStatusVS), but the binding is of strength 'required'
    - The declared type of the element (code) is incompatible with that of the instance (string).
    - Code 'Example' does not exist in the value set 'Identifier Status Value Set' (http://hl7.org/fhir/us/ndh/ValueSet/IdentifierStatusVS), but the binding is of strength 'required' (for slice identifier-status)
    - The declared type of the element (code) is incompatible with that of the instance (string). (for slice identifier-status)
- ❌ NdhOrganizationAffiliationClass (1 errors)
    - Instance failed constraint organization-or-participatingOrganization "NdhOrganizationAffiliation.organization or  NdhOrganizationAffiliation.participatingOrganization"
- ❌ NdhPnLdApiOrganizationAffiliationClass (1 errors)
    - Instance failed constraint organization-or-participatingOrganization "NdhOrganizationAffiliation.organization or  NdhOrganizationAffiliation.participatingOrganization"
- ❌ NdhInsurancePlanClass (2 errors)
    - Instance failed constraint ipn-1 "The organization SHALL at least have a name or an idendtifier, and possibly more than one"
    - Instance failed constraint network-or-NatlDirwork "If an insuranceplan does not define a network, then each plan must define one"
- ❌ NdhNdApiInsurancePlanClass (2 errors)
    - Instance failed constraint ipn-1 "The organization SHALL at least have a name or an idendtifier, and possibly more than one"
    - Instance failed constraint network-or-NatlDirwork "If an insuranceplan does not define a network, then each plan must define one"
- ❌ NdhPnLdApiInsurancePlanClass (2 errors)
    - Instance failed constraint ipn-1 "The organization SHALL at least have a name or an idendtifier, and possibly more than one"
    - Instance failed constraint network-or-NatlDirwork "If an insuranceplan does not define a network, then each plan must define one"

---

[← Back to Summary](./pipeline-parity-summary.md)
