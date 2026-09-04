# physical-activity - Detailed Report (FHIR all)
Generated: 2026-09-04T19:55:36.575Z

Package: `hl7.fhir.us.physical-activity@1.0.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 12 | 12 | 100% |
| Random Validation Parity | 12 | 12 | 100% |
| Random Generation Validation + Parity | 11 | 12 | 92% |


---

## Empty Validation Parity Results

### ✅ Passing (12)
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

### ✅ Passing (12)
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

### ✅ Passing (11)
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

### ❌ Failing (1)
- ❌ PAServiceRequestClass (1 errors)
    - Instance failed constraint pa-sr-1 "At least one of reasonCode or reasonReference must be provided"

---

[← Back to Summary](./pipeline-parity-summary.md)
