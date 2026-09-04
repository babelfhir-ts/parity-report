# davinci-drug-formulary - Detailed Report (FHIR all)
Generated: 2026-08-29T11:16:22.016Z

Package: `hl7.fhir.us.davinci-drug-formulary@2.1.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 8 | 8 | 100% |
| Random Validation Parity | 8 | 8 | 100% |
| Random Generation Validation + Parity | 5 | 8 | 63% |


---

## Empty Validation Parity Results

### ✅ Passing (8)
- ✅ InsurancePlanCoverageExtensionClass
- ✅ InsurancePlanLocationClass
- ✅ FormularyBulkDataGraphDefinitionClass
- ✅ FormularyClass
- ✅ FormularyDrugClass
- ✅ FormularyItemClass
- ✅ PayerInsurancePlanBulkDataGraphDefinitionClass
- ✅ PayerInsurancePlanClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (8)
- ✅ InsurancePlanCoverageExtensionClass
- ✅ InsurancePlanLocationClass
- ✅ FormularyBulkDataGraphDefinitionClass
- ✅ FormularyClass
- ✅ FormularyDrugClass
- ✅ FormularyItemClass
- ✅ PayerInsurancePlanBulkDataGraphDefinitionClass
- ✅ PayerInsurancePlanClass

### ❌ Failing (0)
_None_

---

## Random Generation Validation + Parity Results

### ✅ Passing (5)
- ✅ InsurancePlanCoverageExtensionClass
- ✅ FormularyBulkDataGraphDefinitionClass
- ✅ FormularyClass
- ✅ FormularyItemClass
- ✅ PayerInsurancePlanBulkDataGraphDefinitionClass

### ❌ Failing (3)
- ❌ InsurancePlanLocationClass (1 errors)
    - Location contains an address, geolocation, or both
- ❌ FormularyDrugClass (1 errors)
    - Slice 'MedicationKnowledge.code.coding:semantic-drug': a matching slice is required, but not found
- ❌ PayerInsurancePlanClass (9 errors)
    - Object must have some content
    - Must have either extensions or value[x], not both
    - Extension.url is required in order to identify, use and validate the extension
    - Extension.url: minimum required = 1, but only found 0
    - InsurancePlan.plan.specificCost.category: minimum required = 1, but only found 0

---

[← Back to Summary](./pipeline-parity-summary.md)
