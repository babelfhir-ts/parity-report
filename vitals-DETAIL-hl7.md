# vitals - Detailed Report (FHIR all)
Generated: 2026-09-05T11:33:18.975Z

Package: `hl7.fhir.us.vitals@1.0.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 1 | 1 | 100% |
| Random Validation Parity | 15 | 15 | 100% |
| Random Generation Validation + Parity | 9 | 15 | 60% |


---

## Empty Validation Parity Results

### ✅ Passing (1)
- ✅ BloodPressureDeviceClass

### ❌ Failing (0)
_None_

### ⚠️ Excluded - External Issues (14)
- ⚠️ AverageBloodPressureClass (excluded - Validator bug)
- ⚠️ BloodPressurePanelClass (excluded - Validator bug)
- ⚠️ BodyLengthClass (excluded - Validator bug)
- ⚠️ BodyMassIndexClass (excluded - Validator bug)
- ⚠️ BodyTemperatureClass (excluded - Validator bug)
- ⚠️ BodyWeightClass (excluded - Validator bug)
- ⚠️ HeadOccipitalFrontalCircumferenceClass (excluded - Validator bug)
- ⚠️ HeartRateClass (excluded - Validator bug)
- ⚠️ HeightClass (excluded - Validator bug)
- ⚠️ OxygenSaturationArterialBloodClass (excluded - Validator bug)
- ⚠️ OxygenSaturationArterialBloodPulseOxClass (excluded - Validator bug)
- ⚠️ ResiratoryRateClass (excluded - Validator bug)
- ⚠️ TwentyFourHourBloodPressureClass (excluded - Validator bug)
- ⚠️ VitalSignsPanelClass (excluded - Validator bug)

---

## Random Validation Parity Results

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

## Random Generation Validation + Parity Results

### ✅ Passing (9)
- ✅ BloodPressureDeviceClass
- ✅ BodyMassIndexClass
- ✅ BodyTemperatureClass
- ✅ BodyWeightClass
- ✅ HeartRateClass
- ✅ HeightClass
- ✅ OxygenSaturationArterialBloodClass
- ✅ OxygenSaturationArterialBloodPulseOxClass
- ✅ ResiratoryRateClass

### ❌ Failing (6)
- ❌ AverageBloodPressureClass (1 errors)
    - Value is '/min' but is fixed to 'mm[Hg]' in the profile http://hl7.org/fhir/us/vitals/StructureDefinition/average-blood-pressure|1.0.0#Observation.component:SystolicBP.value[x]:valueQuantity.code
- ❌ BloodPressurePanelClass (2 errors)
    - Observation.component: minimum required = 2, but only found 1
    - Slice 'Observation.component:DiastolicBP': a matching slice is required, but not found
- ❌ BodyLengthClass (1 errors)
    - BodyHeightCode: magic LOINC code 8302-2 required, but not found
- ❌ HeadOccipitalFrontalCircumferenceClass (1 errors)
    - HeadCircumCode: magic LOINC code 9843-4 required, but not found
- ❌ TwentyFourHourBloodPressureClass (2 errors)
    - if Observation.effective[x] is dateTime and has a value then that value shall be precise to the day
    - Value is '/min' but is fixed to 'mm[Hg]' in the profile http://hl7.org/fhir/us/vitals/StructureDefinition/twenty-four-hour-blood-pressure|1.0.0#Observation.component:SystolicBP24HMean.value[x]:valueQuantity.code
- ❌ VitalSignsPanelClass (1 errors)
    - This element does not match any known slice defined in the profile http://hl7.org/fhir/us/vitals/StructureDefinition/vital-signs-panel|1.0.0 and slicing is CLOSED: Observation.hasMember[0]: Does not match slice 'OxygenSaturationArterialBloodPulseOx' (discriminator: resolve().conformsTo('http://hl7.org/fhir/us/vitals/StructureDefinition/oxygen-saturation-arterial-blood-pulseOx')), Observation.hasMember[0]: Does not match slice 'BodyWeight' (discriminator: resolve().conformsTo('http://hl7.org/fhir/us/vitals/StructureDefinition/body-weight')), Observation.hasMember[0]: Does not match slice 'HeadOccipitalFrontalCircumference' (discriminator: resolve().conformsTo('http://hl7.org/fhir/us/vitals/StructureDefinition/head-occipital-frontal-circumference')), Observation.hasMember[0]: Does not match slice 'Height' (discriminator: resolve().conformsTo('http://hl7.org/fhir/us/vitals/StructureDefinition/height')), Observation.hasMember[0]: Does not match slice 'BodyLength' (discriminator: resolve().conformsTo('http://hl7.org/fhir/us/vitals/StructureDefinition/body-length')), Observation.hasMember[0]: Does not match slice 'BodyTemperature' (discriminator: resolve().conformsTo('http://hl7.org/fhir/us/vitals/StructureDefinition/body-temperature')), Observation.hasMember[0]: Does not match slice 'BloodPressurePanel' (discriminator: resolve().conformsTo('http://hl7.org/fhir/us/vitals/StructureDefinition/blood-pressure-panel')), Observation.hasMember[0]: Does not match slice 'HeartRate' (discriminator: resolve().conformsTo('http://hl7.org/fhir/us/vitals/StructureDefinition/heart-rate')), Observation.hasMember[0]: Does not match slice 'RespiratoryRate' (discriminator: resolve().conformsTo('http://hl7.org/fhir/us/vitals/StructureDefinition/respiratory-rate')), Observation.hasMember[0]: Does not match slice 'BodyMassIndex' (discriminator: resolve().conformsTo('http://hl7.org/fhir/us/vitals/StructureDefinition/body-mass-index'))

---

[← Back to Summary](./pipeline-parity-summary.md)
