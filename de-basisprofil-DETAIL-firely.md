# de-basisprofil - Detailed Report (FHIR all)
Generated: 2026-09-05T11:25:10.824Z

Package: `de.basisprofil.r4@1.6.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 19 | 19 | 100% |
| Random Validation Parity | 14 | 19 | 74% |
| Random Generation Validation + Parity | 8 | 19 | 42% |


---

## Empty Validation Parity Results

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

## Random Validation Parity Results

### ✅ Passing (14)
- ✅ CoverageDeBasisClass
- ✅ CoverageDeGkvClass
- ✅ CoverageDeSelClass
- ✅ ObservationDePflegegradClass
- ✅ ChargeItemEBMClass
- ✅ EkgDEClass
- ✅ GradDerBehinderungClass
- ✅ NamingsystemDeBasisClass
- ✅ ScoreDEGCSClass
- ✅ VitalSignDEBlutdruckClass
- ✅ VitalSignDEClass
- ✅ VitalSignDEKoerpergewichtClass
- ✅ VitalSignDEKoerpergroesseClass
- ✅ VitalSignDEKopfumfangClass

### ❌ Failing (5)
- ❌ VitalSignDEArterielleSauerstoffsaettigungClass
  - Field-level comparison:
  Both validators: code
  Only Firely: pattern

- ❌ VitalSignDEArterielleSauerstoffsaettigungPulsoximetrieClass
  - Field-level comparison:
  Both validators: code
  Only Firely: pattern

- ❌ VitalSignDEAtemfrequenzClass
  - Field-level comparison:
  Both validators: code
  Only Firely: pattern

- ❌ VitalSignDEHerzfrequenzClass
  - Field-level comparison:
  Both validators: code
  Only Firely: pattern

- ❌ VitalSignDEKoerperkerntemperaturClass
  - Field-level comparison:
  Both validators: code
  Only Firely: pattern


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
    - No elements matched required slice: 'coding:ebm'
- ❌ GradDerBehinderungClass (1 errors)
    - Instance failed constraint value-only-tenth "Ergebnis muss eine durch 10 teilbare Zahl sein"
- ❌ NamingsystemDeBasisClass (1 errors)
    - Code 'document' does not exist in the value set 'NamingSystemIdentifierType' (http://hl7.org/fhir/ValueSet/namingsystem-identifier-type), but the binding is of strength 'required'
- ❌ VitalSignDEArterielleSauerstoffsaettigungClass (2 errors)
    - Missing required member: 'code'
    - Value '{"value":72,"comparator":">","unit":"1","system":"http://unitsofmeasure.org","code":"/h"}' does not match pattern '{"system":"http://unitsofmeasure.org","code":"%"}' (for slice valueQuantity)
- ❌ VitalSignDEArterielleSauerstoffsaettigungPulsoximetrieClass (2 errors)
    - Missing required member: 'code'
    - Value '{"value":72,"comparator":">","unit":"1","system":"http://unitsofmeasure.org","code":"/h"}' does not match pattern '{"system":"http://unitsofmeasure.org","code":"%"}' (for slice valueQuantity)
- ❌ VitalSignDEAtemfrequenzClass (2 errors)
    - Missing required member: 'code'
    - Value '{"value":72,"comparator":">","unit":"1","system":"http://unitsofmeasure.org","code":"/h"}' does not match pattern '{"system":"http://unitsofmeasure.org","code":"/min"}' (for slice valueQuantity)
- ❌ VitalSignDEHerzfrequenzClass (2 errors)
    - Missing required member: 'code'
    - Value '{"value":72,"comparator":">","unit":"1","system":"http://unitsofmeasure.org","code":"/h"}' does not match pattern '{"system":"http://unitsofmeasure.org","code":"/min"}' (for slice valueQuantity)
- ❌ VitalSignDEKoerpergewichtClass (2 errors)
    - Missing required member: 'code'
    - Code '/h' from system 'http://unitsofmeasure.org' does not exist in the value set 'VitalSignDE_Body_Weigth_UCUM' (http://fhir.de/ValueSet/VitalSignDE_Body_Weigth_UCUM), but the binding is of strength 'required' (for slice valueQuantity)
- ❌ VitalSignDEKoerpergroesseClass (2 errors)
    - Missing required member: 'code'
    - Code '/h' from system 'http://unitsofmeasure.org' does not exist in the value set 'VitalSignDE_Body_Length_UCUM' (http://fhir.de/ValueSet/VitalSignDE_Body_Length_UCUM), but the binding is of strength 'required' (for slice valueQuantity)
- ❌ VitalSignDEKoerperkerntemperaturClass (2 errors)
    - Missing required member: 'code'
    - Value '{"value":72,"comparator":">","unit":"1","system":"http://unitsofmeasure.org","code":"/h"}' does not match pattern '{"system":"http://unitsofmeasure.org","code":"Cel"}' (for slice valueQuantity)
- ❌ VitalSignDEKopfumfangClass (2 errors)
    - Missing required member: 'code'
    - Code '/h' from system 'http://unitsofmeasure.org' does not exist in the value set 'VitalSignDE_Body_Length_UCUM' (http://fhir.de/ValueSet/VitalSignDE_Body_Length_UCUM), but the binding is of strength 'required' (for slice valueQuantity)

---

[← Back to Summary](./pipeline-parity-summary.md)
