# de-basisprofil - Detailed Report (FHIR all)
Generated: 2026-10-01T09:10:19.696Z

Package: `de.basisprofil.r4@1.6.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 9 | 9 | 100% |
| Random Validation Parity | 19 | 19 | 100% |
| Random Generation Validation + Parity | 8 | 19 | 42% |


---

## Empty Validation Parity Results

### ✅ Passing (9)
- ✅ CoverageDeBasisClass
- ✅ CoverageDeGkvClass
- ✅ CoverageDeSelClass
- ✅ ObservationDePflegegradClass
- ✅ ChargeItemEBMClass
- ✅ EkgDEClass
- ✅ GradDerBehinderungClass
- ✅ NamingsystemDeBasisClass
- ✅ ScoreDEGCSClass

### ❌ Failing (0)
_None_

### ⚠️ Excluded - External Issues (10)
- ⚠️ VitalSignDEArterielleSauerstoffsaettigungClass (excluded - Validator bug)
- ⚠️ VitalSignDEArterielleSauerstoffsaettigungPulsoximetrieClass (excluded - Validator bug)
- ⚠️ VitalSignDEAtemfrequenzClass (excluded - Validator bug)
- ⚠️ VitalSignDEBlutdruckClass (excluded - Validator bug)
- ⚠️ VitalSignDEClass (excluded - Validator bug)
- ⚠️ VitalSignDEHerzfrequenzClass (excluded - Validator bug)
- ⚠️ VitalSignDEKoerpergewichtClass (excluded - Validator bug)
- ⚠️ VitalSignDEKoerpergroesseClass (excluded - Validator bug)
- ⚠️ VitalSignDEKoerperkerntemperaturClass (excluded - Validator bug)
- ⚠️ VitalSignDEKopfumfangClass (excluded - Validator bug)

---

## Random Validation Parity Results

### ✅ Passing (19)
- ✅ CoverageDeBasisClass
- ✅ CoverageDeGkvClass
- ✅ CoverageDeSelClass
- ✅ ObservationDePflegegradClass
- ✅ ChargeItemEBMClass
- ✅ EkgDEClass
- ✅ GradDerBehinderungClass
- ✅ NamingsystemDeBasisClass
- ✅ ScoreDEGCSClass
- ✅ VitalSignDEArterielleSauerstoffsaettigungClass
- ✅ VitalSignDEArterielleSauerstoffsaettigungPulsoximetrieClass
- ✅ VitalSignDEAtemfrequenzClass
- ✅ VitalSignDEBlutdruckClass
- ✅ VitalSignDEClass
- ✅ VitalSignDEHerzfrequenzClass
- ✅ VitalSignDEKoerpergewichtClass
- ✅ VitalSignDEKoerpergroesseClass
- ✅ VitalSignDEKoerperkerntemperaturClass
- ✅ VitalSignDEKopfumfangClass

### ❌ Failing (0)
_None_

---

## Random Generation Validation + Parity Results

### ✅ Passing (8)
- ✅ CoverageDeBasisClass
- ✅ CoverageDeGkvClass
- ✅ CoverageDeSelClass
- ✅ ObservationDePflegegradClass
- ✅ EkgDEClass
- ✅ ScoreDEGCSClass
- ✅ VitalSignDEBlutdruckClass
- ✅ VitalSignDEClass

### ❌ Failing (11)
- ❌ ChargeItemEBMClass (1 errors)
    - Slice 'ChargeItem.code.coding:ebm': a matching slice is required, but not found
- ❌ GradDerBehinderungClass (1 errors)
    - Ergebnis muss eine durch 10 teilbare Zahl sein
- ❌ NamingsystemDeBasisClass (2 errors)
    - The System URI could not be determined for the code 'document' in the ValueSet 'http://hl7.org/fhir/ValueSet/namingsystem-identifier-type|4.0.1'
    - The value provided ('document') was not found in the value set 'NamingSystemIdentifierType' (http://hl7.org/fhir/ValueSet/namingsystem-identifier-type|4.0.1), and a code is required from this value set  (error message = The System URI could not be determined for the code 'document' in the ValueSet 'http://hl7.org/fhir/ValueSet/namingsystem-identifier-type|4.0.1'; The provided code '#document' was not found in the value set 'http://hl7.org/fhir/ValueSet/namingsystem-identifier-type|4.0.1')
- ❌ VitalSignDEArterielleSauerstoffsaettigungClass (5 errors)
    - Value is '/h' but is fixed to '%' in the profile http://hl7.org/fhir/StructureDefinition/oxygensat|4.0.1#Observation.value[x]:valueQuantity.code
    - Observation.code.coding:snomed.code: minimum required = 1, but only found 0
    - Observation.code.coding.code: minimum required = 1, but only found 0
    - Value is '/h' but is fixed to '%' in the profile http://fhir.de/StructureDefinition/observation-de-vitalsign-sauerstoffsaettigung|1.6.0#Observation
    - Value is '/h' but is fixed to '%' in the profile http://fhir.de/StructureDefinition/observation-de-vitalsign-sauerstoffsaettigung|1.6.0#Observation.value[x]:valueQuantity
- ❌ VitalSignDEArterielleSauerstoffsaettigungPulsoximetrieClass (5 errors)
    - Value is '/h' but is fixed to '%' in the profile http://hl7.org/fhir/StructureDefinition/oxygensat|4.0.1#Observation.value[x]:valueQuantity.code
    - Observation.code.coding:snomed.code: minimum required = 1, but only found 0
    - Observation.code.coding.code: minimum required = 1, but only found 0
    - Value is '/h' but is fixed to '%' in the profile http://fhir.de/StructureDefinition/observation-de-vitalsign-sauerstoffsaettigung-pulsoximetrie|1.6.0#Observation
    - Value is '/h' but is fixed to '%' in the profile http://fhir.de/StructureDefinition/observation-de-vitalsign-sauerstoffsaettigung-pulsoximetrie|1.6.0#Observation.value[x]:valueQuantity
- ❌ VitalSignDEAtemfrequenzClass (5 errors)
    - Value is '/h' but is fixed to '/min' in the profile http://hl7.org/fhir/StructureDefinition/resprate|4.0.1#Observation.value[x]:valueQuantity.code
    - Observation.code.coding:snomed.code: minimum required = 1, but only found 0
    - Observation.code.coding.code: minimum required = 1, but only found 0
    - Value is '/h' but is fixed to '/min' in the profile http://fhir.de/StructureDefinition/observation-de-vitalsign-atemfrequenz|1.6.0#Observation
    - Value is '/h' but is fixed to '/min' in the profile http://fhir.de/StructureDefinition/observation-de-vitalsign-atemfrequenz|1.6.0#Observation.value[x]:valueQuantity
- ❌ VitalSignDEHerzfrequenzClass (5 errors)
    - Value is '/h' but is fixed to '/min' in the profile http://hl7.org/fhir/StructureDefinition/heartrate|4.0.1#Observation.value[x]:valueQuantity.code
    - Observation.code.coding:snomed.code: minimum required = 1, but only found 0
    - Observation.code.coding.code: minimum required = 1, but only found 0
    - Value is '/h' but is fixed to '/min' in the profile http://fhir.de/StructureDefinition/observation-de-vitalsign-herzfrequenz|1.6.0#Observation
    - Value is '/h' but is fixed to '/min' in the profile http://fhir.de/StructureDefinition/observation-de-vitalsign-herzfrequenz|1.6.0#Observation.value[x]:valueQuantity
- ❌ VitalSignDEKoerpergewichtClass (5 errors)
    - The System URI could not be determined for the code '/h' in the ValueSet 'http://hl7.org/fhir/ValueSet/ucum-bodyweight|4.0.1'
    - The value provided ('/h') was not found in the value set 'Body Weight Units' (http://hl7.org/fhir/ValueSet/ucum-bodyweight|4.0.1), and a code is required from this value set  (error message = The System URI could not be determined for the code '/h' in the ValueSet 'http://hl7.org/fhir/ValueSet/ucum-bodyweight|4.0.1'; The provided code '#/h' was not found in the value set 'http://hl7.org/fhir/ValueSet/ucum-bodyweight|4.0.1')
    - Observation.code.coding:snomed.code: minimum required = 1, but only found 0
    - Observation.code.coding.code: minimum required = 1, but only found 0
    - The code provided (http://unitsofmeasure.org#/h) was not found in the value set 'VitalSignDE_Body_Weigth_UCUM' (http://fhir.de/ValueSet/VitalSignDE_Body_Weigth_UCUM|1.6.0), and a code from this value set is required: The provided code 'http://unitsofmeasure.org#/h' was not found in the value set 'http://fhir.de/ValueSet/VitalSignDE_Body_Weigth_UCUM|1.6.0'
- ❌ VitalSignDEKoerpergroesseClass (5 errors)
    - The System URI could not be determined for the code '/h' in the ValueSet 'http://hl7.org/fhir/ValueSet/ucum-bodylength|4.0.1'
    - The value provided ('/h') was not found in the value set 'Body Length Units' (http://hl7.org/fhir/ValueSet/ucum-bodylength|4.0.1), and a code is required from this value set  (error message = The System URI could not be determined for the code '/h' in the ValueSet 'http://hl7.org/fhir/ValueSet/ucum-bodylength|4.0.1'; The provided code '#/h' was not found in the value set 'http://hl7.org/fhir/ValueSet/ucum-bodylength|4.0.1')
    - Observation.code.coding:snomed.code: minimum required = 1, but only found 0
    - Observation.code.coding.code: minimum required = 1, but only found 0
    - The code provided (http://unitsofmeasure.org#/h) was not found in the value set 'VitalSignDE_Body_Length_UCUM' (http://fhir.de/ValueSet/VitalSignDE_Body_Length_UCUM|1.6.0), and a code from this value set is required: The provided code 'http://unitsofmeasure.org#/h' was not found in the value set 'http://fhir.de/ValueSet/VitalSignDE_Body_Length_UCUM|1.6.0'
- ❌ VitalSignDEKoerperkerntemperaturClass (6 errors)
    - The System URI could not be determined for the code '/h' in the ValueSet 'http://hl7.org/fhir/ValueSet/ucum-bodytemp|4.0.1'
    - The value provided ('/h') was not found in the value set 'Body Temperature Units' (http://hl7.org/fhir/ValueSet/ucum-bodytemp|4.0.1), and a code is required from this value set  (error message = The System URI could not be determined for the code '/h' in the ValueSet 'http://hl7.org/fhir/ValueSet/ucum-bodytemp|4.0.1'; The provided code '#/h' was not found in the value set 'http://hl7.org/fhir/ValueSet/ucum-bodytemp|4.0.1')
    - Observation.code.coding:snomed.code: minimum required = 1, but only found 0
    - Observation.code.coding.code: minimum required = 1, but only found 0
    - Value is '/h' but is fixed to 'Cel' in the profile http://fhir.de/StructureDefinition/observation-de-vitalsign-koerpertemperatur|1.6.0#Observation
- ❌ VitalSignDEKopfumfangClass (5 errors)
    - The System URI could not be determined for the code '/h' in the ValueSet 'http://hl7.org/fhir/ValueSet/ucum-bodylength|4.0.1'
    - The value provided ('/h') was not found in the value set 'Body Length Units' (http://hl7.org/fhir/ValueSet/ucum-bodylength|4.0.1), and a code is required from this value set  (error message = The System URI could not be determined for the code '/h' in the ValueSet 'http://hl7.org/fhir/ValueSet/ucum-bodylength|4.0.1'; The provided code '#/h' was not found in the value set 'http://hl7.org/fhir/ValueSet/ucum-bodylength|4.0.1')
    - Observation.code.coding:snomed.code: minimum required = 1, but only found 0
    - Observation.code.coding.code: minimum required = 1, but only found 0
    - The code provided (http://unitsofmeasure.org#/h) was not found in the value set 'VitalSignDE_Body_Length_UCUM' (http://fhir.de/ValueSet/VitalSignDE_Body_Length_UCUM|1.6.0), and a code from this value set is required: The provided code 'http://unitsofmeasure.org#/h' was not found in the value set 'http://fhir.de/ValueSet/VitalSignDE_Body_Length_UCUM|1.6.0'

---

[← Back to Summary](./pipeline-parity-summary.md)
