# kbv-erp - Detailed Report (FHIR all)
Generated: 2026-08-29T11:15:16.602Z

Package: `kbv.ita.erp@1.4.4`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 8 | 8 | 100% |
| Random Validation Parity | 3 | 8 | 38% |
| Random Generation Validation + Parity | 0 | 8 | 0% |


---

## Empty Validation Parity Results

### ✅ Passing (8)
- ✅ KBVPRERPMedicationCompoundingClass
- ✅ KBVPRERPMedicationFreeTextClass
- ✅ KBVPRERPMedicationIngredientClass
- ✅ KBVPRERPMedicationPZNClass
- ✅ KBVPRERPBundleClass
- ✅ KBVPRERPCompositionClass
- ✅ KBVPRERPPracticeSupplyClass
- ✅ KBVPRERPPrescriptionClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (3)
- ✅ KBVPRERPCompositionClass
- ✅ KBVPRERPPracticeSupplyClass
- ✅ KBVPRERPPrescriptionClass

### ❌ Failing (5)
- ❌ KBVPRERPMedicationCompoundingClass
  - Field-level comparison:
  Both validators: unclassified
  Only Internal: constraint, unit, text, extension, url, profile, entry

- ❌ KBVPRERPMedicationFreeTextClass
  - Field-level comparison:
  Both validators: profile
  Only Firely: pattern

- ❌ KBVPRERPMedicationIngredientClass
  - Field-level comparison:
  Both validators: unclassified, text, profile
  Only Internal: constraint, extension
  Only Firely: pattern

- ❌ KBVPRERPMedicationPZNClass
  - Field-level comparison:
  Both validators: unclassified, extension, url, profile
  Only Internal: constraint, entry

- ❌ KBVPRERPBundleClass
  - Field-level comparison:
  Both validators: unclassified, entry, meta
  Only Firely: pattern, text, display, qualification, type, use, extension, address, gender, birthDate


---

## Random Generation Validation + Parity Results

### ✅ Passing (0)
_None_

### ❌ Failing (8)
- ❌ KBVPRERPMedicationCompoundingClass (1 errors)
    - One or more errors occurred. (Encountered a json primitive while expecting a json object for non-primitive element 'extension'. At Medication.amount.numerator.extension[0], line 48, position 9.)
- ❌ KBVPRERPMedicationFreeTextClass (2 errors)
    - No elements matched required slice: 'profile:erpProfile'
    - Value 'code-id-2br' is not exactly equal to fixed value 'freitext' (for slice verordnungskategorieCode)
- ❌ KBVPRERPMedicationIngredientClass (7 errors)
    - Instance failed constraint -erp-angabeNormgroesseOderMenge "Packungsgröße oder Normgröße (Wert N1 oder N2 oder N3) müssen angegeben sein."
    - No elements matched required slice: 'profile:erpProfile'
    - Value 'code-id-qz5' is not exactly equal to fixed value 'wirkstoff' (for slice verordnungskategorieCode)
    - Missing required member: 'text' (for slice itemCodeableConcept)
    - Element does not match any slice and the group is closed. (for slice @default)
- ❌ KBVPRERPMedicationPZNClass (9 errors)
    - Instance failed constraint -erp-angabeNormgroesseOderMenge "Packungsgröße oder Normgröße (Wert N1 oder N2 oder N3) müssen angegeben sein"
    - No elements matched required slice: 'profile:erpProfile'
    - Missing required member: 'url'
    - No elements matched required slice: 'extension:Kategorie'
    - Element does not match any slice and the group is closed. (for slice @default)
- ❌ KBVPRERPBundleClass (51 errors)
    - Instance failed constraint -erp-referenzAufAusstellendePerson-1 "In der Ressource vom Typ MedicationRequest oder SupplyRequest zeigt die Referenz nicht auf die Ressource vom Typ Practitioner fuer die ausstellende/verschreibende Person."
    - Instance failed constraint -erp-referenzAufPatientInCoverage "In der Ressource vom Typ Coverage zeigt die Referenz der begünstigten Person nicht auf die Ressource vom Typ Patient, die sich im Bundle befindet."
    - Instance failed constraint -erp-referenzAufPatientInMedicationRequest "In der Ressource vom Typ MedicationRequest zeigt die Referenz der Person, für die Medikation verordnet wurde, nicht auf die Ressource vom Typ Patient, die sich im Bundle befindet."
    - Instance failed constraint -erp-referenzAufCoverageInMedicationRequest "In der Ressource vom Typ MedicationRequest zeigt die Referenz der Versicherung nicht auf die Ressource vom Typ Coverage, die sich im Bundle befindet."
    - Instance failed constraint -erp-angabeKVKVersichertennummerVerbot "In der Ressource vom Typ Patient ist eine KVK-Versichertennummer vorhanden, diese darf nicht angegeben werden."
- ❌ KBVPRERPCompositionClass (2 errors)
    - No elements matched required slice: 'profile:erpProfile'
    - Instance count at element 'identifier' is 1, which is not within the specified cardinality of 0..0 (for slice Arzt)
- ❌ KBVPRERPPracticeSupplyClass (3 errors)
    - Instance failed constraint -erp-begrenzungDate "Begrenzung der Datumsangabe auf 10 Zeichen JJJJ-MM-TT"
    - No elements matched required slice: 'profile:erpProfile'
    - Code 'UNK' from system 'http://terminology.hl7.org/CodeSystem/v3-NullFlavor' does not exist in the value set 'KBV_VS_FOR_Payor_type' (https://fhir.kbv.de/ValueSet/KBV_VS_FOR_Payor_type), but the binding is of strength 'required' (for slice valueCoding)
- ❌ KBVPRERPPrescriptionClass (10 errors)
    - Instance failed constraint -erp-begrenzungDate "Begrenzung der Datumsangabe auf 10 Zeichen JJJJ-MM-TT"
    - No elements matched required slice: 'profile:erpProfile'
    - Instance failed constraint -erp-multiplePrescriptionKennzeichenTrueNummerierung "Mehrfachverordnung: Wenn das Kennzeichen gleich true ist, muss eine Nummerierung (Zaehler und Nenner) angegeben werden."
    - Instance failed constraint -erp-multiplePrescriptionKennzeichenTrueZeitraum "Mehrfachverordnung: Wenn das Kennzeichen gleich true ist, muss ein Zeitraum (mindestens Beginn der Einlösefrist) angegeben werden."
    - Instance failed constraint -erp-multiplePrescriptionKennzeichenTrueID "Mehrfachverordnung: Wenn das Kennzeichen gleich true ist, muss eine ID angegeben werden."

---

[← Back to Summary](./pipeline-parity-summary.md)
