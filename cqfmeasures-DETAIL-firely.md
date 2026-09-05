# cqfmeasures - Detailed Report (FHIR all)
Generated: 2026-09-05T11:25:09.671Z

Package: `hl7.fhir.us.cqfmeasures@5.0.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 13 | 13 | 100% |
| Random Validation Parity | 11 | 13 | 85% |
| Random Generation Validation + Parity | 6 | 13 | 46% |


---

## Empty Validation Parity Results

### ✅ Passing (13)
- ✅ CQFMAttestationMeasureClass
- ✅ CQFMCohortMeasureClass
- ✅ CQFMCompositeMeasureClass
- ✅ CQFMComputableMeasureClass
- ✅ CQFMContinuousVariableMeasureClass
- ✅ CQFMCQLMeasureClass
- ✅ CQFMDeviceClass
- ✅ CQFMELMMeasureClass
- ✅ CQFMExecutableMeasureClass
- ✅ CQFMProportionMeasureClass
- ✅ CQFMPublishableMeasureClass
- ✅ CQFMRatioMeasureClass
- ✅ CQFMTestCaseClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (11)
- ✅ CQFMAttestationMeasureClass
- ✅ CQFMCohortMeasureClass
- ✅ CQFMCompositeMeasureClass
- ✅ CQFMComputableMeasureClass
- ✅ CQFMContinuousVariableMeasureClass
- ✅ CQFMCQLMeasureClass
- ✅ CQFMDeviceClass
- ✅ CQFMELMMeasureClass
- ✅ CQFMExecutableMeasureClass
- ✅ CQFMRatioMeasureClass
- ✅ CQFMTestCaseClass

### ❌ Failing (2)
- ❌ CQFMProportionMeasureClass
  - Field-level comparison:
  Both validators: unclassified, population
  Only Firely: extension

- ❌ CQFMPublishableMeasureClass
  - Field-level comparison:
  Both validators: none
  Only Firely: unclassified, extension, value


---

## Random Generation Validation + Parity Results

### ✅ Passing (6)
- ✅ CQFMAttestationMeasureClass
- ✅ CQFMCQLMeasureClass
- ✅ CQFMDeviceClass
- ✅ CQFMELMMeasureClass
- ✅ CQFMExecutableMeasureClass
- ✅ CQFMTestCaseClass

### ❌ Failing (7)
- ❌ CQFMCohortMeasureClass (3 errors)
    - Instance failed constraint cmp-1 "Population basis must be specified at the root, or on each group"
    - Instance failed constraint cmp-2 "Scoring must either be specified at the root, or on each group"
    - Instance failed constraint cmp-4 "Improvement notation must be specified for scoring types other than cohort"
- ❌ CQFMCompositeMeasureClass (2 errors)
    - Instance failed constraint cmp-2 "Scoring must either be specified at the root, or on each group"
    - Instance failed constraint cmp-4 "Improvement notation must be specified for scoring types other than cohort"
- ❌ CQFMComputableMeasureClass (2 errors)
    - Instance failed constraint cmp-2 "Scoring must either be specified at the root, or on each group"
    - Instance failed constraint cmp-4 "Improvement notation must be specified for scoring types other than cohort"
- ❌ CQFMContinuousVariableMeasureClass (1 errors)
    - One or more errors occurred. (An object needs to have at least one property. At Measure.group[0].population[0].extension[0], line 25, position 12.)
- ❌ CQFMProportionMeasureClass (8 errors)
    - Instance failed constraint cmp-1 "Population basis must be specified at the root, or on each group"
    - Instance failed constraint cmp-2 "Scoring must either be specified at the root, or on each group"
    - Instance failed constraint cmp-4 "Improvement notation must be specified for scoring types other than cohort"
    - Instance count at element 'population' is 1, which is not within the specified cardinality of 3..6
    - No elements matched required slice: 'population:initialPopulation'
- ❌ CQFMPublishableMeasureClass (8 errors)
    - Extension used outside of appropriate contexts. Expected context to be one of: {ELEMENT,Resource}
    - No elements matched required slice: 'extension:term'
    - No elements matched required slice: 'extension:definition'
    - Instance count at element 'value' is 1, which is not within the specified cardinality of 0..0
    - Extension used outside of appropriate contexts. Expected context to be one of: {ELEMENT,Resource} (for slice definitionTerm)
- ❌ CQFMRatioMeasureClass (1 errors)
    - One or more errors occurred. (An object needs to have at least one property. At Measure.group[0].population[0].extension[0], line 25, position 12.)

---

[← Back to Summary](./pipeline-parity-summary.md)
