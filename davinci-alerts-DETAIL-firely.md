# davinci-alerts - Detailed Report (FHIR all)
Generated: 2026-08-29T11:16:20.773Z

Package: `hl7.fhir.us.davinci-alerts@1.1.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 3 | 3 | 100% |
| Random Validation Parity | 2 | 3 | 67% |
| Random Generation Validation + Parity | 1 | 3 | 33% |


---

## Empty Validation Parity Results

### ✅ Passing (3)
- ✅ ADTNotificationConditionProfileClass
- ✅ NotificationsBundleClass
- ✅ TransferNotificationMessageHeaderClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (2)
- ✅ ADTNotificationConditionProfileClass
- ✅ NotificationsBundleClass

### ❌ Failing (1)
- ❌ TransferNotificationMessageHeaderClass
  - Field-level comparison:
  Both validators: constraint
  Only Internal: focus


---

## Random Generation Validation + Parity Results

### ✅ Passing (1)
- ✅ NotificationsBundleClass

### ❌ Failing (2)
- ❌ ADTNotificationConditionProfileClass (1 errors)
    - Encountered a reference (Encounter/id-whbpk3gk) of kind 'Referenced', which is not one of the allowed kinds (Bundled).
- ❌ TransferNotificationMessageHeaderClass (2 errors)
    - Encountered a reference (SearchParameter/id-5xezw5uw) of kind 'Referenced', which is not one of the allowed kinds (Bundled).
    - Encountered a reference (SearchParameter/id-5xezw5uw) of kind 'Referenced', which is not one of the allowed kinds (Bundled). (for slice transfer-notification)

---

[← Back to Summary](./pipeline-parity-summary.md)
