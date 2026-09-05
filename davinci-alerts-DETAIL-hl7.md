# davinci-alerts - Detailed Report (FHIR all)
Generated: 2026-09-04T20:53:08.903Z

Package: `hl7.fhir.us.davinci-alerts@1.1.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 8 | 8 | 100% |
| Random Validation Parity | 8 | 8 | 100% |
| Random Generation Validation + Parity | 1 | 8 | 13% |


---

## Empty Validation Parity Results

### ✅ Passing (8)
- ✅ ADTNotificationConditionProfileClass
- ✅ ADTNotificationCoverageProfileClass
- ✅ ADTNotificationEncounterProfileClass
- ✅ AdmitNotificationMessageHeaderClass
- ✅ DischargeNotificationMessageHeaderClass
- ✅ NotificationsBundleClass
- ✅ NotificationsMessageHeaderClass
- ✅ TransferNotificationMessageHeaderClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (8)
- ✅ ADTNotificationConditionProfileClass
- ✅ ADTNotificationCoverageProfileClass
- ✅ ADTNotificationEncounterProfileClass
- ✅ AdmitNotificationMessageHeaderClass
- ✅ DischargeNotificationMessageHeaderClass
- ✅ NotificationsBundleClass
- ✅ NotificationsMessageHeaderClass
- ✅ TransferNotificationMessageHeaderClass

### ❌ Failing (0)
_None_

---

## Random Generation Validation + Parity Results

### ✅ Passing (1)
- ✅ NotificationsBundleClass

### ❌ Failing (7)
- ❌ ADTNotificationConditionProfileClass (1 errors)
    - Bundled or contained reference not found within the bundle/resource Encounter/id-whbpk3gk
- ❌ ADTNotificationCoverageProfileClass (1 errors)
    - Bundled or contained reference not found within the bundle/resource Patient/id-endd7r6a
- ❌ ADTNotificationEncounterProfileClass (1 errors)
    - Bundled or contained reference not found within the bundle/resource Patient/id-wllqxho2
- ❌ AdmitNotificationMessageHeaderClass (2 errors)
    - Slice 'MessageHeader.focus:admit-notification': a matching slice is required, but not found
    - Bundled or contained reference not found within the bundle/resource SearchParameter/id-xxks7l4h
- ❌ DischargeNotificationMessageHeaderClass (2 errors)
    - Slice 'MessageHeader.focus:discharge-notification': a matching slice is required, but not found
    - Bundled or contained reference not found within the bundle/resource SearchParameter/id-1xhw1vhp
- ❌ NotificationsMessageHeaderClass (1 errors)
    - Bundled or contained reference not found within the bundle/resource Resource/id-dodpbbsq
- ❌ TransferNotificationMessageHeaderClass (2 errors)
    - Slice 'MessageHeader.focus:transfer-notification': a matching slice is required, but not found
    - Bundled or contained reference not found within the bundle/resource SearchParameter/id-5xezw5uw

---

[← Back to Summary](./pipeline-parity-summary.md)
