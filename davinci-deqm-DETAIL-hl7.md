# davinci-deqm - Detailed Report (FHIR all)
Generated: 2026-09-05T11:26:57.063Z

Package: `hl7.fhir.us.davinci-deqm@5.0.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 11 | 11 | 100% |
| Random Validation Parity | 11 | 11 | 100% |
| Random Generation Validation + Parity | 5 | 11 | 45% |


---

## Empty Validation Parity Results

### ✅ Passing (11)
- ✅ DEQMDataExchangeMeasureReportProfileClass
- ✅ DEQMGapsInCareCompositionProfileClass
- ✅ DEQMGapsInCareDetectedIssueProfileClass
- ✅ DEQMGapsInCareGroupProfileClass
- ✅ DEQMIndividualMeasureReportProfileClass
- ✅ DEQMSummaryMeasureReportProfileClass
- ✅ DEQMGapsInCareBundleClass
- ✅ DEQMIndividualMeasureReportListClass
- ✅ DEQMSubjectListMeasureReportClass
- ✅ DetailedCareGapGuidanceResponseClass
- ✅ ParametersCareGapRemarkPatchClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (11)
- ✅ DEQMDataExchangeMeasureReportProfileClass
- ✅ DEQMGapsInCareCompositionProfileClass
- ✅ DEQMGapsInCareDetectedIssueProfileClass
- ✅ DEQMGapsInCareGroupProfileClass
- ✅ DEQMIndividualMeasureReportProfileClass
- ✅ DEQMSummaryMeasureReportProfileClass
- ✅ DEQMGapsInCareBundleClass
- ✅ DEQMIndividualMeasureReportListClass
- ✅ DEQMSubjectListMeasureReportClass
- ✅ DetailedCareGapGuidanceResponseClass
- ✅ ParametersCareGapRemarkPatchClass

### ❌ Failing (0)
_None_

---

## Random Generation Validation + Parity Results

### ✅ Passing (5)
- ✅ DEQMGapsInCareCompositionProfileClass
- ✅ DEQMGapsInCareDetectedIssueProfileClass
- ✅ DEQMIndividualMeasureReportListClass
- ✅ DetailedCareGapGuidanceResponseClass
- ✅ ParametersCareGapRemarkPatchClass

### ❌ Failing (6)
- ❌ DEQMDataExchangeMeasureReportProfileClass (3 errors)
    - The System URI could not be determined for the code 'code' in the ValueSet 'http://hl7.org/fhir/us/davinci-deqm/ValueSet/update-type|5.0.0'
    - The value provided ('code') was not found in the value set 'DEQM Update Type Value Set' (http://hl7.org/fhir/us/davinci-deqm/ValueSet/update-type|5.0.0), and a code is required from this value set  (error message = The System URI could not be determined for the code 'code' in the ValueSet 'http://hl7.org/fhir/us/davinci-deqm/ValueSet/update-type|5.0.0'; The provided code '#code' was not found in the value set 'http://hl7.org/fhir/us/davinci-deqm/ValueSet/update-type|5.0.0')
    - If present, start SHALL have a lower value than end
- ❌ DEQMGapsInCareGroupProfileClass (1 errors)
    - Can only have members if group is "actual"
- ❌ DEQMIndividualMeasureReportProfileClass (2 errors)
    - Canonical URL SHALL contain a version.
    - If the scoring, at either the root level or the group level, is other than composite then the group.population cardinality is >=1
- ❌ DEQMSummaryMeasureReportProfileClass (3 errors)
    - Canonical URL SHALL contain a version.
    - The population must either have a count (integer) or a countQuantity (quantity), but not both.
    - Measure scoring is required. It must be specified on the root only, or on every group, and it cannot be on both.
- ❌ DEQMGapsInCareBundleClass (3 errors)
    - The property resource must be an Object, not a Primitive property (at Bundle.entry[0].resource)
    - entry.request mandatory for batch/transaction/history, otherwise prohibited
    - Except for transactions and batches, each entry in a Bundle must have a fullUrl which is the identity of the resource in the entry
- ❌ DEQMSubjectListMeasureReportClass (3 errors)
    - Canonical URL SHALL contain a version.
    - The population must either have a count (integer) or a countQuantity (quantity), but not both.
    - Measure scoring is required. It must be specified on the root only, or on every group, and it cannot be on both.

---

[← Back to Summary](./pipeline-parity-summary.md)
