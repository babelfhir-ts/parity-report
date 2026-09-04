# vitals - Detailed Report (FHIR all)
Generated: 2026-08-29T11:15:04.115Z

Package: `hl7.fhir.us.vitals@1.0.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 15 | 15 | 100% |
| Random Validation Parity | 12 | 15 | 80% |
| Random Generation Validation + Parity | 13 | 15 | 87% |


---

## Empty Validation Parity Results

### ✅ Passing (15)
- ✅ AverageBloodPressureClass
- ✅ BloodPressureDeviceClass
- ✅ BloodPressurePanelClass
- ✅ BodyLengthClass
- ✅ BodyMassIndexClass
- ✅ BodyTemperatureClass
- ✅ BodyWeightClass
- ✅ HeadOccipitalFrontalCircumferenceClass
- ✅ HeartRateClass
- ✅ HeightClass
- ✅ OxygenSaturationArterialBloodClass
- ✅ OxygenSaturationArterialBloodPulseOxClass
- ✅ ResiratoryRateClass
- ✅ TwentyFourHourBloodPressureClass
- ✅ VitalSignsPanelClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (12)
- ✅ BloodPressureDeviceClass
- ✅ BloodPressurePanelClass
- ✅ BodyLengthClass
- ✅ BodyMassIndexClass
- ✅ BodyTemperatureClass
- ✅ BodyWeightClass
- ✅ HeadOccipitalFrontalCircumferenceClass
- ✅ HeartRateClass
- ✅ HeightClass
- ✅ OxygenSaturationArterialBloodClass
- ✅ OxygenSaturationArterialBloodPulseOxClass
- ✅ ResiratoryRateClass

### ❌ Failing (3)
- ❌ AverageBloodPressureClass
  - Field-level comparison:
  Both validators: none
  Only Firely: pattern

- ❌ TwentyFourHourBloodPressureClass
  - Field-level comparison:
  Both validators: none
  Only Internal: unclassified
  Only Firely: pattern

- ❌ VitalSignsPanelClass
  - Field-level comparison:
  Both validators: none
  Only Internal: entry


---

## Random Generation Validation + Parity Results

### ✅ Passing (13)
- ✅ BloodPressureDeviceClass
- ✅ BloodPressurePanelClass
- ✅ BodyLengthClass
- ✅ BodyMassIndexClass
- ✅ BodyTemperatureClass
- ✅ BodyWeightClass
- ✅ HeadOccipitalFrontalCircumferenceClass
- ✅ HeartRateClass
- ✅ HeightClass
- ✅ OxygenSaturationArterialBloodClass
- ✅ OxygenSaturationArterialBloodPulseOxClass
- ✅ ResiratoryRateClass
- ✅ VitalSignsPanelClass

### ❌ Failing (2)
- ❌ AverageBloodPressureClass (1 errors)
    - Value '/min' is not exactly equal to fixed value 'mm[Hg]' (for slice valueQuantity)
- ❌ TwentyFourHourBloodPressureClass (1 errors)
    - Value '/min' is not exactly equal to fixed value 'mm[Hg]' (for slice valueQuantity)

---

[← Back to Summary](./pipeline-parity-summary.md)
