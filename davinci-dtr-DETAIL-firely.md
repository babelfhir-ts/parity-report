# davinci-dtr - Detailed Report (FHIR all)
Generated: 2026-09-04T19:51:21.020Z

Package: `hl7.fhir.us.davinci-dtr@2.2.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 14 | 14 | 100% |
| Random Validation Parity | 12 | 14 | 86% |
| Random Generation Validation + Parity | 2 | 14 | 14% |


---

## Empty Validation Parity Results

### ✅ Passing (14)
- ✅ DTRBaseQuestionnaireClass
- ✅ DTRQuestionnaireAdaptClass
- ✅ DTRQuestionnaireAdaptSearchClass
- ✅ DTRQuestionnaireNextQuestionnaireInputParametersClass
- ✅ DTRQuestionnaireNextQuestionnaireOutputParametersClass
- ✅ DTRQuestionnairePackageBundleClass
- ✅ DTRQuestionnairePackageInputParametersClass
- ✅ DTRQuestionnairePackageOutputParametersClass
- ✅ DTRQuestionnaireResponseAdaptClass
- ✅ DTRQuestionnaireResponseBundleClass
- ✅ DTRQuestionnaireResponseClass
- ✅ DTRStdQuestionnaireClass
- ✅ DTRLogErrorsInputParametersClass
- ✅ DTRSupportedPayersClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (12)
- ✅ DTRBaseQuestionnaireClass
- ✅ DTRQuestionnaireAdaptClass
- ✅ DTRQuestionnaireAdaptSearchClass
- ✅ DTRQuestionnaireNextQuestionnaireInputParametersClass
- ✅ DTRQuestionnaireNextQuestionnaireOutputParametersClass
- ✅ DTRQuestionnairePackageBundleClass
- ✅ DTRQuestionnairePackageInputParametersClass
- ✅ DTRQuestionnairePackageOutputParametersClass
- ✅ DTRQuestionnaireResponseBundleClass
- ✅ DTRQuestionnaireResponseClass
- ✅ DTRLogErrorsInputParametersClass
- ✅ DTRSupportedPayersClass

### ❌ Failing (2)
- ❌ DTRQuestionnaireResponseAdaptClass
  - Field-level comparison:
  Both validators: unclassified
  Only Internal: resourceType, constraint, resource, extension

- ❌ DTRStdQuestionnaireClass
  - Field-level comparison:
  Both validators: unclassified, code, value, extension
  Only Internal: constraint, entry


---

## Random Generation Validation + Parity Results

### ✅ Passing (2)
- ✅ DTRBaseQuestionnaireClass
- ✅ DTRLogErrorsInputParametersClass

### ❌ Failing (12)
- ❌ DTRQuestionnaireAdaptClass (1 errors)
    - The declared type of the element (url) is incompatible with that of the instance (boolean). (for slice questionnaireAdaptive)
- ❌ DTRQuestionnaireAdaptSearchClass (1 errors)
    - The declared type of the element (url) is incompatible with that of the instance (boolean). (for slice questionnaireAdaptive)
- ❌ DTRQuestionnaireNextQuestionnaireInputParametersClass (7 errors)
    - Missing required member: 'contained'
    - Missing required member: 'extension'
    - Missing required member: 'questionnaire'
    - Missing required member: 'subject'
    - Missing required member: 'authored'
- ❌ DTRQuestionnaireNextQuestionnaireOutputParametersClass (7 errors)
    - Missing required member: 'contained'
    - Missing required member: 'extension'
    - Missing required member: 'questionnaire'
    - Missing required member: 'subject'
    - Missing required member: 'authored'
- ❌ DTRQuestionnairePackageBundleClass (6 errors)
    - Missing required member: 'subjectType'
    - Missing required member: 'extension'
    - No elements matched required slice: 'extension:coverage'
    - No elements matched required slice: 'extension:intendedUse'
    - Missing required member: 'extension'
- ❌ DTRQuestionnairePackageInputParametersClass (1 errors)
    - Instance failed constraint dtr-1 "At least one of 'order', 'questionnaire' and 'context' SHALL be present"
- ❌ DTRQuestionnairePackageOutputParametersClass (5 errors)
    - Instance failed constraint dtrb-1 "The first resource in bundle must be a Questionnaire."
    - Missing required member: 'entry'
    - No elements matched required slice: 'entry:questionnaire'
    - No elements matched required slice: 'entry:questionnaireResponse'
    - Instance failed constraint dtrb-1 "The first resource in bundle must be a Questionnaire." (for slice packagebundle)
- ❌ DTRQuestionnaireResponseAdaptClass (1 errors)
    - One or more errors occurred. (Resource has no 'resourceType' property. At line 22, position 6.)
- ❌ DTRQuestionnaireResponseBundleClass (5 errors)
    - Missing required member: 'extension'
    - No elements matched required slice: 'extension:coverage'
    - No elements matched required slice: 'extension:intendedUse'
    - Missing required member: 'extension'
    - No elements matched required slice: 'extension:origin'
- ❌ DTRQuestionnaireResponseClass (2 errors)
    - Missing required member: 'extension'
    - No elements matched required slice: 'extension:origin'
- ❌ DTRStdQuestionnaireClass (13 errors)
    - Instance failed constraint que-5 "Only 'choice' and 'open-choice' items can have answerValueSet"
    - Instance failed constraint que-11 "If one or more answerOption is present, initial[x] must be missing"
    - Missing required member: 'extension'
    - No elements matched required slice: 'extension:label'
    - No elements matched required slice: 'extension:expression'
- ❌ DTRSupportedPayersClass (1 errors)
    - Encountered a reference (Resource/id-b23zid9d) of kind 'Referenced', which is not one of the allowed kinds (Contained).

---

[← Back to Summary](./pipeline-parity-summary.md)
