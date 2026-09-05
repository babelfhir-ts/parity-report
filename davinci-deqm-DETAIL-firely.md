# davinci-deqm - Detailed Report (FHIR all)
Generated: 2026-09-05T11:32:29.361Z

Package: `hl7.fhir.us.davinci-deqm@5.0.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 11 | 11 | 100% |
| Random Validation Parity | 10 | 11 | 91% |
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

### ✅ Passing (10)
- ✅ DEQMDataExchangeMeasureReportProfileClass
- ✅ DEQMGapsInCareCompositionProfileClass
- ✅ DEQMGapsInCareDetectedIssueProfileClass
- ✅ DEQMGapsInCareGroupProfileClass
- ✅ DEQMIndividualMeasureReportProfileClass
- ✅ DEQMSummaryMeasureReportProfileClass
- ✅ DEQMIndividualMeasureReportListClass
- ✅ DEQMSubjectListMeasureReportClass
- ✅ DetailedCareGapGuidanceResponseClass
- ✅ ParametersCareGapRemarkPatchClass

### ❌ Failing (1)
- ❌ DEQMGapsInCareBundleClass
  - Field-level comparison:
  Both validators: unclassified
  Only Internal: resource
  Only Firely: entry


---

## Random Generation Validation + Parity Results

### ✅ Passing (5)
- ✅ DEQMGapsInCareCompositionProfileClass
- ✅ DEQMGapsInCareDetectedIssueProfileClass
- ✅ DEQMIndividualMeasureReportListClass
- ✅ DetailedCareGapGuidanceResponseClass
- ✅ ParametersCareGapRemarkPatchClass

### ❌ Failing (6)
- ❌ DEQMDataExchangeMeasureReportProfileClass (2 errors)
    - Code 'code' does not exist in the value set 'DEQM Update Type Value Set' (http://hl7.org/fhir/us/davinci-deqm/ValueSet/update-type), but the binding is of strength 'required' (for slice valueCode)
    - Instance failed constraint per-1 "If present, start SHALL have a lower value than end"
- ❌ DEQMGapsInCareGroupProfileClass (1 errors)
    - Instance failed constraint grp-1 "Can only have members if group is "actual""
- ❌ DEQMIndividualMeasureReportProfileClass (2 errors)
    - Instance failed constraint deqm-5 "If the scoring, at either the root level or the group level, is other than composite then the group.population cardinality is >=1"
    - Instance failed constraint deqm-0 "Canonical URL SHALL contain a version."
- ❌ DEQMSummaryMeasureReportProfileClass (3 errors)
    - Instance failed constraint deqm-3 "Measure scoring is required. It must be specified on the root only, or on every group, and it cannot be on both."
    - Instance failed constraint deqm-0 "Canonical URL SHALL contain a version."
    - Instance failed constraint deqm-8 "The population must either have a count (integer) or a countQuantity (quantity), but not both."
- ❌ DEQMGapsInCareBundleClass (2 errors)
    - Resource has no 'resourceType' property. At line 22, position 6.
    - Encountered a json primitive while expecting a json object for non-primitive element 'resource'. At Bundle.entry[0].resource, line 21, position 19.
- ❌ DEQMSubjectListMeasureReportClass (3 errors)
    - Instance failed constraint deqm-3 "Measure scoring is required. It must be specified on the root only, or on every group, and it cannot be on both."
    - Instance failed constraint deqm-0 "Canonical URL SHALL contain a version."
    - Instance failed constraint deqm-8 "The population must either have a count (integer) or a countQuantity (quantity), but not both."

---

[← Back to Summary](./pipeline-parity-summary.md)
