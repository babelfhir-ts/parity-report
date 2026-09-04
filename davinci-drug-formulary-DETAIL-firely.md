# davinci-drug-formulary - Detailed Report (FHIR all)
Generated: 2026-08-29T11:15:17.212Z

Package: `hl7.fhir.us.davinci-drug-formulary@2.1.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 7 | 7 | 100% |
| Random Validation Parity | 6 | 7 | 86% |
| Random Generation Validation + Parity | 5 | 7 | 71% |


---

## Empty Validation Parity Results

### ✅ Passing (7)
- ✅ InsurancePlanCoverageExtensionClass
- ✅ InsurancePlanLocationClass
- ✅ FormularyBulkDataGraphDefinitionClass
- ✅ FormularyClass
- ✅ FormularyItemClass
- ✅ PayerInsurancePlanBulkDataGraphDefinitionClass
- ✅ PayerInsurancePlanClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (6)
- ✅ InsurancePlanCoverageExtensionClass
- ✅ InsurancePlanLocationClass
- ✅ FormularyBulkDataGraphDefinitionClass
- ✅ FormularyClass
- ✅ FormularyItemClass
- ✅ PayerInsurancePlanBulkDataGraphDefinitionClass

### ❌ Failing (1)
- ❌ PayerInsurancePlanClass
  - Field-level comparison:
  Both validators: url, extension
  Only Internal: category, coverage, benefit


---

## Random Generation Validation + Parity Results

### ✅ Passing (5)
- ✅ InsurancePlanCoverageExtensionClass
- ✅ FormularyBulkDataGraphDefinitionClass
- ✅ FormularyClass
- ✅ FormularyItemClass
- ✅ PayerInsurancePlanBulkDataGraphDefinitionClass

### ❌ Failing (2)
- ❌ InsurancePlanLocationClass (1 errors)
    - Instance failed constraint Location-address-or-geolocation "Location contains an address, geolocation, or both"
- ❌ PayerInsurancePlanClass (1 errors)
    - One or more errors occurred. (An object needs to have at least one property. At InsurancePlan.coverage[0].extension[0], line 35, position 8.)

---

[← Back to Summary](./pipeline-parity-summary.md)
