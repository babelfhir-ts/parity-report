# cqfmeasures - Detailed Report (FHIR all)
Generated: 2026-09-04T19:59:36.649Z

Package: `hl7.fhir.us.cqfmeasures@5.0.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 12 | 12 | 100% |
| Random Validation Parity | 12 | 12 | 100% |
| Random Generation Validation + Parity | 6 | 12 | 50% |


---

## Empty Validation Parity Results

### ✅ Passing (12)
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
- ✅ CQFMRatioMeasureClass
- ✅ CQFMTestCaseClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (12)
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
- ✅ CQFMRatioMeasureClass
- ✅ CQFMTestCaseClass

### ❌ Failing (0)
_None_

---

## Random Generation Validation + Parity Results

### ✅ Passing (6)
- ✅ CQFMAttestationMeasureClass
- ✅ CQFMCQLMeasureClass
- ✅ CQFMDeviceClass
- ✅ CQFMELMMeasureClass
- ✅ CQFMExecutableMeasureClass
- ✅ CQFMTestCaseClass

### ❌ Failing (6)
- ❌ CQFMCohortMeasureClass (3 errors)
    - Population basis must be specified at the root, or on each group
    - Scoring must either be specified at the root, or on each group
    - Improvement notation must be specified for scoring types other than cohort
- ❌ CQFMCompositeMeasureClass (2 errors)
    - Scoring must either be specified at the root, or on each group
    - Improvement notation must be specified for scoring types other than cohort
- ❌ CQFMComputableMeasureClass (2 errors)
    - Scoring must either be specified at the root, or on each group
    - Improvement notation must be specified for scoring types other than cohort
- ❌ CQFMContinuousVariableMeasureClass (13 errors)
    - Object must have some content
    - Must have either extensions or value[x], not both
    - Extension.url is required in order to identify, use and validate the extension
    - Extension.url: minimum required = 1, but only found 0
    - Measure.group.population: minimum required = 3, but only found 1
- ❌ CQFMProportionMeasureClass (7 errors)
    - Measure.group.population: minimum required = 3, but only found 1
    - Slice 'Measure.group.population:initialPopulation': a matching slice is required, but not found
    - Slice 'Measure.group.population:denominator': a matching slice is required, but not found
    - Slice 'Measure.group.population:numerator': a matching slice is required, but not found
    - Population basis must be specified at the root, or on each group
- ❌ CQFMRatioMeasureClass (12 errors)
    - Object must have some content
    - Must have either extensions or value[x], not both
    - Extension.url is required in order to identify, use and validate the extension
    - Extension.url: minimum required = 1, but only found 0
    - Measure.group.population: minimum required = 4, but only found 1

---

[← Back to Summary](./pipeline-parity-summary.md)
