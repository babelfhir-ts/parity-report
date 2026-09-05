# kbv-erp - Detailed Report (FHIR all)
Generated: 2026-09-05T11:32:19.297Z

Package: `kbv.ita.erp@1.4.4`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 7 | 7 | 100% |
| Random Validation Parity | 6 | 7 | 86% |
| Random Generation Validation + Parity | 0 | 7 | 0% |


---

## Empty Validation Parity Results

### ✅ Passing (7)
- ✅ KBVPRERPMedicationCompoundingClass
- ✅ KBVPRERPMedicationFreeTextClass
- ✅ KBVPRERPMedicationIngredientClass
- ✅ KBVPRERPMedicationPZNClass
- ✅ KBVPRERPCompositionClass
- ✅ KBVPRERPPracticeSupplyClass
- ✅ KBVPRERPPrescriptionClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (6)
- ✅ KBVPRERPMedicationCompoundingClass
- ✅ KBVPRERPMedicationFreeTextClass
- ✅ KBVPRERPMedicationPZNClass
- ✅ KBVPRERPCompositionClass
- ✅ KBVPRERPPracticeSupplyClass
- ✅ KBVPRERPPrescriptionClass

### ❌ Failing (1)
- ❌ KBVPRERPMedicationIngredientClass
  - Field-level comparison:
  Both validators: unclassified, constraint, text, code, profile
  Only Internal: extension
  Only HL7: entry


---

## Random Generation Validation + Parity Results

### ✅ Passing (0)
_None_

### ❌ Failing (7)
- ❌ KBVPRERPMedicationCompoundingClass (18 errors)
    - The property extension must be an Array, not a Primitive property (at Medication.amount.numerator.extension[0])
    - Error parsing JSON: the primitive value must be a number
    - Extension.url is required in order to identify, use and validate the extension
    - Extension.url: minimum required = 1, but only found 0
    - Unknown code 'code-id-dod' in the CodeSystem 'https://fhir.kbv.de/CodeSystem/KBV_CS_ERP_Medication_Type' version '1.4.4'
- ❌ KBVPRERPMedicationFreeTextClass (3 errors)
    - Unknown code 'code-id-2br' in the CodeSystem 'https://fhir.kbv.de/CodeSystem/KBV_CS_ERP_Medication_Type' version '1.4.4'
    - Slice 'Medication.meta.profile:erpProfile': a matching slice is required, but not found
    - Value is 'code-id-2br' but is fixed to 'freitext' in the profile https://fhir.kbv.de/StructureDefinition/KBV_PR_ERP_Medication_FreeText|1.4.4#Medication.code.coding:verordnungskategorieCode.code
- ❌ KBVPRERPMedicationIngredientClass (12 errors)
    - Error parsing JSON: the primitive value must be a number
    - Error parsing JSON: the primitive value must be a number
    - Unknown code 'code-id-qz5' in the CodeSystem 'https://fhir.kbv.de/CodeSystem/KBV_CS_ERP_Medication_Type' version '1.4.4'
    - All FHIR elements must have a @value or children
    - The value 'Example value' is not a valid decimal
- ❌ KBVPRERPMedicationPZNClass (14 errors)
    - Error parsing JSON: the primitive value must be a number
    - Error parsing JSON: the primitive value must be a number
    - Extension.url is required in order to identify, use and validate the extension
    - Extension.url: minimum required = 1, but only found 0
    - All FHIR elements must have a @value or children
- ❌ KBVPRERPCompositionClass (2 errors)
    - Slice 'Composition.meta.profile:erpProfile': a matching slice is required, but not found
    - Composition.author:Arzt.identifier: max allowed = 0, but found 1
- ❌ KBVPRERPPracticeSupplyClass (3 errors)
    - The Coding provided (http://terminology.hl7.org/CodeSystem/v3-NullFlavor#UNK) was not found in the value set 'KBV_VS_FOR_Payor_type' (https://fhir.kbv.de/ValueSet/KBV_VS_FOR_Payor_type|1.3.1), and a code is required from this value set.  (error message = The provided code 'http://terminology.hl7.org/CodeSystem/v3-NullFlavor#UNK' was not found in the value set 'https://fhir.kbv.de/ValueSet/KBV_VS_FOR_Payor_type|1.3.1')
    - Slice 'SupplyRequest.meta.profile:erpProfile': a matching slice is required, but not found
    - Begrenzung der Datumsangabe auf 10 Zeichen JJJJ-MM-TT
- ❌ KBVPRERPPrescriptionClass (7 errors)
    - Mehrfachverordnung: Wenn das Kennzeichen gleich true ist, muss eine Nummerierung (Zaehler und Nenner) angegeben werden.
    - Mehrfachverordnung: Wenn das Kennzeichen gleich true ist, muss ein Zeitraum (mindestens Beginn der Einlösefrist) angegeben werden.
    - Mehrfachverordnung: Wenn das Kennzeichen gleich true ist, muss eine ID angegeben werden.
    - Slice 'MedicationRequest.meta.profile:erpProfile': a matching slice is required, but not found
    - MedicationRequest.dispenseRequest.quantity.system: max allowed = 0, but found 1

---

[← Back to Summary](./pipeline-parity-summary.md)
