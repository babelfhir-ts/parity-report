# carin-bb - Detailed Report (FHIR all)
Generated: 2026-09-04T20:02:41.206Z

Package: `hl7.fhir.us.carin-bb@2.2.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 16 | 16 | 100% |
| Random Validation Parity | 16 | 16 | 100% |
| Random Generation Validation + Parity | 6 | 16 | 38% |


---

## Empty Validation Parity Results

### ✅ Passing (16)
- ✅ C4BBCoverageClass
- ✅ C4BBExplanationOfBenefitInpatientInstitutionalBasisClass
- ✅ C4BBExplanationOfBenefitInpatientInstitutionalClass
- ✅ C4BBExplanationOfBenefitOutpatientInstitutionalBasisClass
- ✅ C4BBExplanationOfBenefitOutpatientInstitutionalClass
- ✅ C4BBOrganizationClass
- ✅ C4BBPatientClass
- ✅ C4BBPractitionerClass
- ✅ C4BBExplanationOfBenefitClass
- ✅ C4BBExplanationOfBenefitOralBasisClass
- ✅ C4BBExplanationOfBenefitOralClass
- ✅ C4BBExplanationOfBenefitPharmacyBasisClass
- ✅ C4BBExplanationOfBenefitPharmacyClass
- ✅ C4BBExplanationOfBenefitProfessionalNonClinicianBasisClass
- ✅ C4BBExplanationOfBenefitProfessionalNonClinicianClass
- ✅ C4BBRelatedPersonClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (16)
- ✅ C4BBCoverageClass
- ✅ C4BBExplanationOfBenefitInpatientInstitutionalBasisClass
- ✅ C4BBExplanationOfBenefitInpatientInstitutionalClass
- ✅ C4BBExplanationOfBenefitOutpatientInstitutionalBasisClass
- ✅ C4BBExplanationOfBenefitOutpatientInstitutionalClass
- ✅ C4BBOrganizationClass
- ✅ C4BBPatientClass
- ✅ C4BBPractitionerClass
- ✅ C4BBExplanationOfBenefitClass
- ✅ C4BBExplanationOfBenefitOralBasisClass
- ✅ C4BBExplanationOfBenefitOralClass
- ✅ C4BBExplanationOfBenefitPharmacyBasisClass
- ✅ C4BBExplanationOfBenefitPharmacyClass
- ✅ C4BBExplanationOfBenefitProfessionalNonClinicianBasisClass
- ✅ C4BBExplanationOfBenefitProfessionalNonClinicianClass
- ✅ C4BBRelatedPersonClass

### ❌ Failing (0)
_None_

---

## Random Generation Validation + Parity Results

### ✅ Passing (6)
- ✅ C4BBCoverageClass
- ✅ C4BBOrganizationClass
- ✅ C4BBPatientClass
- ✅ C4BBPractitionerClass
- ✅ C4BBExplanationOfBenefitClass
- ✅ C4BBRelatedPersonClass

### ❌ Failing (10)
- ❌ C4BBExplanationOfBenefitInpatientInstitutionalBasisClass (2 errors)
    - The pattern [system http://terminology.hl7.org/CodeSystem/claim-type, code institutional, and display 'null'] defined in the profile http://hl7.org/fhir/us/carin-bb/StructureDefinition/C4BB-ExplanationOfBenefit-Inpatient-Institutional-Basis|2.2.0 not found. Issues: [ValidationMessage[level=ERROR,type=VALUE,location=ExplanationOfBenefit.type.coding.version,message=Missing element 'version' - required by fixed value assigned in profile http://hl7.org/fhir/us/carin-bb/StructureDefinition/C4BB-ExplanationOfBenefit-Inpatient-Institutional-Basis|2.2.0]]
    - None of the codings provided are in the value set 'NUBC Revenue Codes Value Set' (http://hl7.org/fhir/us/carin-bb/ValueSet/AHANUBCRevenueCodes|2.2.0), and a coding from this value set is required) (codes = http://terminology.hl7.org/CodeSystem/data-absent-reason#unknown)
- ❌ C4BBExplanationOfBenefitInpatientInstitutionalClass (4 errors)
    - The pattern [system http://terminology.hl7.org/CodeSystem/claim-type, code institutional, and display 'null'] defined in the profile http://hl7.org/fhir/us/carin-bb/StructureDefinition/C4BB-ExplanationOfBenefit-Inpatient-Institutional|2.2.0 not found. Issues: [ValidationMessage[level=ERROR,type=VALUE,location=ExplanationOfBenefit.type.coding.version,message=Missing element 'version' - required by fixed value assigned in profile http://hl7.org/fhir/us/carin-bb/StructureDefinition/C4BB-ExplanationOfBenefit-Inpatient-Institutional|2.2.0]]
    - If Adjudication is present, it must have at least one adjudicationamounttype slice
    - None of the codings provided are in the value set 'NUBC Revenue Codes Value Set' (http://hl7.org/fhir/us/carin-bb/ValueSet/AHANUBCRevenueCodes|2.2.0), and a coding from this value set is required) (codes = http://terminology.hl7.org/CodeSystem/data-absent-reason#unknown)
    - Institutional EOB:  Should have adjudication with adjudicationamounttype slice at the item or header level, but not both
- ❌ C4BBExplanationOfBenefitOutpatientInstitutionalBasisClass (1 errors)
    - The pattern [system http://terminology.hl7.org/CodeSystem/claim-type, code institutional, and display 'null'] defined in the profile http://hl7.org/fhir/us/carin-bb/StructureDefinition/C4BB-ExplanationOfBenefit-Outpatient-Institutional-Basis|2.2.0 not found. Issues: [ValidationMessage[level=ERROR,type=VALUE,location=ExplanationOfBenefit.type.coding.version,message=Missing element 'version' - required by fixed value assigned in profile http://hl7.org/fhir/us/carin-bb/StructureDefinition/C4BB-ExplanationOfBenefit-Outpatient-Institutional-Basis|2.2.0]]
- ❌ C4BBExplanationOfBenefitOutpatientInstitutionalClass (3 errors)
    - The pattern [system http://terminology.hl7.org/CodeSystem/claim-type, code institutional, and display 'null'] defined in the profile http://hl7.org/fhir/us/carin-bb/StructureDefinition/C4BB-ExplanationOfBenefit-Outpatient-Institutional|2.2.0 not found. Issues: [ValidationMessage[level=ERROR,type=VALUE,location=ExplanationOfBenefit.type.coding.version,message=Missing element 'version' - required by fixed value assigned in profile http://hl7.org/fhir/us/carin-bb/StructureDefinition/C4BB-ExplanationOfBenefit-Outpatient-Institutional|2.2.0]]
    - If Adjudication is present, it must have at least one adjudicationamounttype slice
    - Institutional EOB:  Should have adjudication with adjudicationamounttype slice at the item or header level, but not both
- ❌ C4BBExplanationOfBenefitOralBasisClass (2 errors)
    - The pattern [system http://terminology.hl7.org/CodeSystem/claim-type, code oral, and display 'null'] defined in the profile http://hl7.org/fhir/us/carin-bb/StructureDefinition/C4BB-ExplanationOfBenefit-Oral-Basis|2.2.0 not found. Issues: [ValidationMessage[level=ERROR,type=VALUE,location=ExplanationOfBenefit.type.coding.version,message=Missing element 'version' - required by fixed value assigned in profile http://hl7.org/fhir/us/carin-bb/StructureDefinition/C4BB-ExplanationOfBenefit-Oral-Basis|2.2.0]]
    - Slice 'ExplanationOfBenefit.item.adjudication:benefitpaymentstatus': a matching slice is required, but not found
- ❌ C4BBExplanationOfBenefitOralClass (4 errors)
    - The pattern [system http://terminology.hl7.org/CodeSystem/claim-type, code oral, and display 'null'] defined in the profile http://hl7.org/fhir/us/carin-bb/StructureDefinition/C4BB-ExplanationOfBenefit-Oral|2.2.0 not found. Issues: [ValidationMessage[level=ERROR,type=VALUE,location=ExplanationOfBenefit.type.coding.version,message=Missing element 'version' - required by fixed value assigned in profile http://hl7.org/fhir/us/carin-bb/StructureDefinition/C4BB-ExplanationOfBenefit-Oral|2.2.0]]
    - ExplanationOfBenefit.item.adjudication: minimum required = 2, but only found 1
    - Slice 'ExplanationOfBenefit.item.adjudication:benefitpaymentstatus': a matching slice is required, but not found
    - Slice 'ExplanationOfBenefit.item.adjudication:adjudicationamounttype': a matching slice is required, but not found
- ❌ C4BBExplanationOfBenefitPharmacyBasisClass (4 errors)
    - The pattern [system http://terminology.hl7.org/CodeSystem/claim-type, code pharmacy, and display 'null'] defined in the profile http://hl7.org/fhir/us/carin-bb/StructureDefinition/C4BB-ExplanationOfBenefit-Pharmacy-Basis|2.2.0 not found. Issues: [ValidationMessage[level=ERROR,type=VALUE,location=ExplanationOfBenefit.type.coding.version,message=Missing element 'version' - required by fixed value assigned in profile http://hl7.org/fhir/us/carin-bb/StructureDefinition/C4BB-ExplanationOfBenefit-Pharmacy-Basis|2.2.0]]
    - None of the codings provided are in the value set 'NCPDP Dispense As Written (DAW)/Product Selection Code Value Set' (http://hl7.org/fhir/us/carin-bb/ValueSet/NCPDPDispensedAsWrittenOrProductSelectionCode|2.2.0), and a coding from this value set is required) (codes = http://terminology.hl7.org/CodeSystem/v3-NullFlavor#UNK)
    - None of the codings provided are in the value set 'NCPDP Reject Code Value Set' (http://hl7.org/fhir/us/carin-bb/ValueSet/NCPDPRejectCode|2.2.0), and a coding from this value set is required) (codes = http://terminology.hl7.org/CodeSystem/data-absent-reason#unknown)
    - None of the codings provided are in the value set 'National Drug Code (NDC) Value Set' (http://hl7.org/fhir/us/carin-bb/ValueSet/FDANationalDrugCode|2.2.0), and a coding from this value set is required) (codes = http://terminology.hl7.org/CodeSystem/data-absent-reason#unknown)
- ❌ C4BBExplanationOfBenefitPharmacyClass (5 errors)
    - The pattern [system http://terminology.hl7.org/CodeSystem/claim-type, code pharmacy, and display 'null'] defined in the profile http://hl7.org/fhir/us/carin-bb/StructureDefinition/C4BB-ExplanationOfBenefit-Pharmacy|2.2.0 not found. Issues: [ValidationMessage[level=ERROR,type=VALUE,location=ExplanationOfBenefit.type.coding.version,message=Missing element 'version' - required by fixed value assigned in profile http://hl7.org/fhir/us/carin-bb/StructureDefinition/C4BB-ExplanationOfBenefit-Pharmacy|2.2.0]]
    - None of the codings provided are in the value set 'NCPDP Dispense As Written (DAW)/Product Selection Code Value Set' (http://hl7.org/fhir/us/carin-bb/ValueSet/NCPDPDispensedAsWrittenOrProductSelectionCode|2.2.0), and a coding from this value set is required) (codes = http://terminology.hl7.org/CodeSystem/v3-NullFlavor#UNK)
    - Slice 'ExplanationOfBenefit.item.adjudication:adjudicationamounttype': a matching slice is required, but not found
    - None of the codings provided are in the value set 'NCPDP Reject Code Value Set' (http://hl7.org/fhir/us/carin-bb/ValueSet/NCPDPRejectCode|2.2.0), and a coding from this value set is required) (codes = http://terminology.hl7.org/CodeSystem/data-absent-reason#unknown)
    - None of the codings provided are in the value set 'National Drug Code (NDC) Value Set' (http://hl7.org/fhir/us/carin-bb/ValueSet/FDANationalDrugCode|2.2.0), and a coding from this value set is required) (codes = http://terminology.hl7.org/CodeSystem/data-absent-reason#unknown)
- ❌ C4BBExplanationOfBenefitProfessionalNonClinicianBasisClass (2 errors)
    - Slice 'ExplanationOfBenefit.item.adjudication:benefitpaymentstatus': a matching slice is required, but not found
    - Vision EOB: Item productOrService not required in item.productOrService if and only if type is vision.
- ❌ C4BBExplanationOfBenefitProfessionalNonClinicianClass (4 errors)
    - ExplanationOfBenefit.item.adjudication: minimum required = 2, but only found 1
    - Slice 'ExplanationOfBenefit.item.adjudication:benefitpaymentstatus': a matching slice is required, but not found
    - Slice 'ExplanationOfBenefit.item.adjudication:adjudicationamounttype': a matching slice is required, but not found
    - Vision EOB: Item productOrService not required in item.productOrService if and only if type is vision.

---

[← Back to Summary](./pipeline-parity-summary.md)
