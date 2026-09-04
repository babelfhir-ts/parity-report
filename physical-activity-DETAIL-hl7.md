# physical-activity - Detailed Report (FHIR all)
Generated: 2026-08-29T11:16:09.820Z

Package: `hl7.fhir.us.physical-activity@1.0.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 16 | 16 | 100% |
| Random Validation Parity | 16 | 16 | 100% |
| Random Generation Validation + Parity | 14 | 16 | 88% |


---

## Empty Validation Parity Results

### ✅ Passing (16)
- ✅ PACarePlanClass
- ✅ PAConditionLowPAClass
- ✅ PADiagnosticReportClass
- ✅ PAGoalClass
- ✅ PAObservationActivityGroupClass
- ✅ PAObservationActivityMeasureClass
- ✅ PAObservationBaseClass
- ✅ PAObservationEVSClass
- ✅ PAObservationEVSDaysPerWeekClass
- ✅ PAObservationEVSMinutesPerDayClass
- ✅ PAObservationEVSMinutesPerWeekClass
- ✅ PAObservationStrengthDaysPerWeekClass
- ✅ PAObservationTimeMeasureClass
- ✅ PAServiceRequestClass
- ✅ PARelatedPersonClass
- ✅ PATaskForReferralManagementClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (16)
- ✅ PACarePlanClass
- ✅ PAConditionLowPAClass
- ✅ PADiagnosticReportClass
- ✅ PAGoalClass
- ✅ PAObservationActivityGroupClass
- ✅ PAObservationActivityMeasureClass
- ✅ PAObservationBaseClass
- ✅ PAObservationEVSClass
- ✅ PAObservationEVSDaysPerWeekClass
- ✅ PAObservationEVSMinutesPerDayClass
- ✅ PAObservationEVSMinutesPerWeekClass
- ✅ PAObservationStrengthDaysPerWeekClass
- ✅ PAObservationTimeMeasureClass
- ✅ PAServiceRequestClass
- ✅ PARelatedPersonClass
- ✅ PATaskForReferralManagementClass

### ❌ Failing (0)
_None_

---

## Random Generation Validation + Parity Results

### ✅ Passing (14)
- ✅ PACarePlanClass
- ✅ PADiagnosticReportClass
- ✅ PAGoalClass
- ✅ PAObservationActivityGroupClass
- ✅ PAObservationActivityMeasureClass
- ✅ PAObservationBaseClass
- ✅ PAObservationEVSClass
- ✅ PAObservationEVSDaysPerWeekClass
- ✅ PAObservationEVSMinutesPerDayClass
- ✅ PAObservationEVSMinutesPerWeekClass
- ✅ PAObservationStrengthDaysPerWeekClass
- ✅ PAObservationTimeMeasureClass
- ✅ PARelatedPersonClass
- ✅ PATaskForReferralManagementClass

### ❌ Failing (2)
- ❌ PAConditionLowPAClass (1 errors)
    - Condition.category: minimum required = 2, but only found 1
- ❌ PAServiceRequestClass (1 errors)
    - At least one of reasonCode or reasonReference must be provided

---

[← Back to Summary](./pipeline-parity-summary.md)
