# davinci-dtr - Detailed Report (FHIR all)
Generated: 2026-09-04T20:07:34.311Z

Package: `hl7.fhir.us.davinci-dtr@2.2.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 14 | 14 | 100% |
| Random Validation Parity | 14 | 14 | 100% |
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

## Random Generation Validation + Parity Results

### ✅ Passing (2)
- ✅ DTRBaseQuestionnaireClass
- ✅ DTRLogErrorsInputParametersClass

### ❌ Failing (12)
- ❌ DTRQuestionnaireAdaptClass (1 errors)
    - The Profile 'http://hl7.org/fhir/us/davinci-dtr/StructureDefinition/dtr-questionnaire-adapt|2.2.0' definition allows for the type url but found type boolean
- ❌ DTRQuestionnaireAdaptSearchClass (1 errors)
    - The Profile 'http://hl7.org/fhir/us/davinci-dtr/StructureDefinition/dtr-questionnaire-adapt-search|2.2.0' definition allows for the type url but found type boolean
- ❌ DTRQuestionnaireNextQuestionnaireInputParametersClass (7 errors)
    - QuestionnaireResponse.contained: minimum required = 1, but only found 0
    - QuestionnaireResponse.extension: minimum required = 2, but only found 0
    - Slice 'QuestionnaireResponse.extension:coverage' for extension 'http://hl7.org/fhir/us/davinci-dtr/StructureDefinition/qr-coverage': a matching slice is required, but not found
    - Slice 'QuestionnaireResponse.extension:intendedUse' for extension 'http://hl7.org/fhir/us/davinci-dtr/StructureDefinition/intendedUse': a matching slice is required, but not found
    - QuestionnaireResponse.questionnaire: minimum required = 1, but only found 0
- ❌ DTRQuestionnaireNextQuestionnaireOutputParametersClass (7 errors)
    - QuestionnaireResponse.contained: minimum required = 1, but only found 0
    - QuestionnaireResponse.extension: minimum required = 2, but only found 0
    - Slice 'QuestionnaireResponse.extension:coverage' for extension 'http://hl7.org/fhir/us/davinci-dtr/StructureDefinition/qr-coverage': a matching slice is required, but not found
    - Slice 'QuestionnaireResponse.extension:intendedUse' for extension 'http://hl7.org/fhir/us/davinci-dtr/StructureDefinition/intendedUse': a matching slice is required, but not found
    - QuestionnaireResponse.questionnaire: minimum required = 1, but only found 0
- ❌ DTRQuestionnairePackageBundleClass (6 errors)
    - Questionnaire.subjectType: minimum required = 1, but only found 0
    - QuestionnaireResponse.extension: minimum required = 2, but only found 0
    - Slice 'QuestionnaireResponse.extension:coverage' for extension 'http://hl7.org/fhir/us/davinci-dtr/StructureDefinition/qr-coverage': a matching slice is required, but not found
    - Slice 'QuestionnaireResponse.extension:intendedUse' for extension 'http://hl7.org/fhir/us/davinci-dtr/StructureDefinition/intendedUse': a matching slice is required, but not found
    - QuestionnaireResponse.item.answer.extension: minimum required = 1, but only found 0
- ❌ DTRQuestionnairePackageInputParametersClass (1 errors)
    - At least one of 'order', 'questionnaire' and 'context' SHALL be present
- ❌ DTRQuestionnairePackageOutputParametersClass (4 errors)
    - Bundle.entry: minimum required = 2, but only found 0
    - Slice 'Bundle.entry:questionnaire': a matching slice is required, but not found
    - Slice 'Bundle.entry:questionnaireResponse': a matching slice is required, but not found
    - The first resource in bundle must be a Questionnaire.
- ❌ DTRQuestionnaireResponseAdaptClass (7 errors)
    - Unable to find resourceType property
    - Resource requires an id, but none is present
    - The Profile 'http://hl7.org/fhir/us/davinci-dtr/StructureDefinition/dtr-questionnaireresponse-adapt|2.2.0' definition allows for the type Questionnaire but found type Resource
    - The type 'Resource' is not valid - no resources allowed here (allowed = Questionnaire)
    - QuestionnaireResponse.item.answer.extension: minimum required = 1, but only found 0
- ❌ DTRQuestionnaireResponseBundleClass (5 errors)
    - QuestionnaireResponse.extension: minimum required = 2, but only found 0
    - Slice 'QuestionnaireResponse.extension:coverage' for extension 'http://hl7.org/fhir/us/davinci-dtr/StructureDefinition/qr-coverage': a matching slice is required, but not found
    - Slice 'QuestionnaireResponse.extension:intendedUse' for extension 'http://hl7.org/fhir/us/davinci-dtr/StructureDefinition/intendedUse': a matching slice is required, but not found
    - QuestionnaireResponse.item.answer.extension: minimum required = 1, but only found 0
    - Slice 'QuestionnaireResponse.item.answer.extension:origin' for extension 'http://hl7.org/fhir/us/davinci-dtr/StructureDefinition/information-origin': a matching slice is required, but not found
- ❌ DTRQuestionnaireResponseClass (2 errors)
    - QuestionnaireResponse.item.answer.extension: minimum required = 1, but only found 0
    - Slice 'QuestionnaireResponse.item.answer.extension:origin' for extension 'http://hl7.org/fhir/us/davinci-dtr/StructureDefinition/information-origin': a matching slice is required, but not found
- ❌ DTRStdQuestionnaireClass (20 errors)
    - Only 'choice' and 'open-choice' items can have answerValueSet
    - If one or more answerOption is present, initial[x] must be missing
    - The Extension 'http://hl7.org/fhir/uv/sdc/StructureDefinition/sdc-questionnaire-contextExpression' definition allows for the types [] but found type Expression
    - Extension.extension: minimum required = 2, but only found 0
    - Slice 'Extension.extension:label': a matching slice is required, but not found
- ❌ DTRSupportedPayersClass (1 errors)
    - Bundled or contained reference not found within the bundle/resource Resource/id-b23zid9d

---

[← Back to Summary](./pipeline-parity-summary.md)
