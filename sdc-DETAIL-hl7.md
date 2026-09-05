# sdc - Detailed Report (FHIR all)
Generated: 2026-09-05T11:26:52.283Z

Package: `hl7.fhir.uv.sdc@4.0.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 34 | 34 | 100% |
| Random Validation Parity | 34 | 34 | 100% |
| Random Generation Validation + Parity | 20 | 34 | 59% |


---

## Empty Validation Parity Results

### ✅ Passing (34)
- ✅ SDCBaseQuestionnaireClass
- ✅ SDCModularQuestionnaireClass
- ✅ SDCModularQuestionnaireLibraryClass
- ✅ SDCParametersQuestionnaireAssembleInClass
- ✅ SDCParametersQuestionnaireAssembleOutClass
- ✅ SDCParametersQuestionnaireNextQuestionnaireInClass
- ✅ SDCParametersQuestionnaireNextQuestionnaireOutClass
- ✅ SDCParametersQuestionnairePopulateHtmlOutClass
- ✅ SDCParametersQuestionnairePopulateInClass
- ✅ SDCParametersQuestionnairePopulateLinkOutClass
- ✅ SDCParametersQuestionnairePopulateOutClass
- ✅ SDCParametersQuestionnaireProcessResponseInClass
- ✅ SDCParametersQuestionnaireResponseExtractInClass
- ✅ SDCQuestionnaireAdaptClass
- ✅ SDCQuestionnaireAdaptSearchClass
- ✅ SDCQuestionnaireBehaveClass
- ✅ SDCQuestionnaireCommonClass
- ✅ SDCQuestionnaireExtractDefinitionClass
- ✅ SDCQuestionnaireExtractObservationClass
- ✅ SDCQuestionnaireExtractStructureMapClass
- ✅ SDCQuestionnaireExtractTemplateClass
- ✅ SDCQuestionnairePopulateExpressionClass
- ✅ SDCQuestionnairePopulateObservationClass
- ✅ SDCQuestionnairePopulateStructureMapClass
- ✅ SDCQuestionnaireRenderClass
- ✅ SDCQuestionnaireResponseAdaptClass
- ✅ SDCQuestionnaireResponseClass
- ✅ SDCQuestionnaireResponseCommonClass
- ✅ SDCQuestionnaireSearchClass
- ✅ SDCQuestionnaireServiceRequestClass
- ✅ SDCTaskQuestionnaireClass
- ✅ SDCCodeSystemClass
- ✅ SDCLibraryClass
- ✅ SDCValueSetClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (34)
- ✅ SDCBaseQuestionnaireClass
- ✅ SDCModularQuestionnaireClass
- ✅ SDCModularQuestionnaireLibraryClass
- ✅ SDCParametersQuestionnaireAssembleInClass
- ✅ SDCParametersQuestionnaireAssembleOutClass
- ✅ SDCParametersQuestionnaireNextQuestionnaireInClass
- ✅ SDCParametersQuestionnaireNextQuestionnaireOutClass
- ✅ SDCParametersQuestionnairePopulateHtmlOutClass
- ✅ SDCParametersQuestionnairePopulateInClass
- ✅ SDCParametersQuestionnairePopulateLinkOutClass
- ✅ SDCParametersQuestionnairePopulateOutClass
- ✅ SDCParametersQuestionnaireProcessResponseInClass
- ✅ SDCParametersQuestionnaireResponseExtractInClass
- ✅ SDCQuestionnaireAdaptClass
- ✅ SDCQuestionnaireAdaptSearchClass
- ✅ SDCQuestionnaireBehaveClass
- ✅ SDCQuestionnaireCommonClass
- ✅ SDCQuestionnaireExtractDefinitionClass
- ✅ SDCQuestionnaireExtractObservationClass
- ✅ SDCQuestionnaireExtractStructureMapClass
- ✅ SDCQuestionnaireExtractTemplateClass
- ✅ SDCQuestionnairePopulateExpressionClass
- ✅ SDCQuestionnairePopulateObservationClass
- ✅ SDCQuestionnairePopulateStructureMapClass
- ✅ SDCQuestionnaireRenderClass
- ✅ SDCQuestionnaireResponseAdaptClass
- ✅ SDCQuestionnaireResponseClass
- ✅ SDCQuestionnaireResponseCommonClass
- ✅ SDCQuestionnaireSearchClass
- ✅ SDCQuestionnaireServiceRequestClass
- ✅ SDCTaskQuestionnaireClass
- ✅ SDCCodeSystemClass
- ✅ SDCLibraryClass
- ✅ SDCValueSetClass

### ❌ Failing (0)
_None_

---

## Random Generation Validation + Parity Results

### ✅ Passing (20)
- ✅ SDCBaseQuestionnaireClass
- ✅ SDCModularQuestionnaireClass
- ✅ SDCParametersQuestionnaireAssembleOutClass
- ✅ SDCParametersQuestionnairePopulateHtmlOutClass
- ✅ SDCParametersQuestionnairePopulateInClass
- ✅ SDCParametersQuestionnairePopulateLinkOutClass
- ✅ SDCParametersQuestionnaireResponseExtractInClass
- ✅ SDCQuestionnaireAdaptSearchClass
- ✅ SDCQuestionnaireBehaveClass
- ✅ SDCQuestionnaireCommonClass
- ✅ SDCQuestionnaireExtractDefinitionClass
- ✅ SDCQuestionnaireExtractObservationClass
- ✅ SDCQuestionnaireExtractStructureMapClass
- ✅ SDCQuestionnairePopulateExpressionClass
- ✅ SDCQuestionnairePopulateStructureMapClass
- ✅ SDCQuestionnaireRenderClass
- ✅ SDCQuestionnaireResponseClass
- ✅ SDCQuestionnaireResponseCommonClass
- ✅ SDCQuestionnaireSearchClass
- ✅ SDCQuestionnaireServiceRequestClass

### ❌ Failing (14)
- ❌ SDCModularQuestionnaireLibraryClass (1 errors)
    - Slice 'Questionnaire.useContext:library': a matching slice is required, but not found
- ❌ SDCParametersQuestionnaireAssembleInClass (2 errors)
    - Questionnaire.extension: minimum required = 1, but only found 0
    - Slice 'Questionnaire.extension:assemble-expectation' for extension 'http://hl7.org/fhir/uv/sdc/StructureDefinition/sdc-questionnaire-assemble-expectation': a matching slice is required, but not found
- ❌ SDCParametersQuestionnaireNextQuestionnaireInClass (3 errors)
    - QuestionnaireResponse.contained: minimum required = 1, but only found 0
    - QuestionnaireResponse.questionnaire: minimum required = 1, but only found 0
    - QuestionnaireResponse.authored: minimum required = 1, but only found 0
- ❌ SDCParametersQuestionnaireNextQuestionnaireOutClass (3 errors)
    - QuestionnaireResponse.contained: minimum required = 1, but only found 0
    - QuestionnaireResponse.questionnaire: minimum required = 1, but only found 0
    - QuestionnaireResponse.authored: minimum required = 1, but only found 0
- ❌ SDCParametersQuestionnairePopulateOutClass (2 errors)
    - QuestionnaireResponse.questionnaire: minimum required = 1, but only found 0
    - QuestionnaireResponse.authored: minimum required = 1, but only found 0
- ❌ SDCParametersQuestionnaireProcessResponseInClass (2 errors)
    - QuestionnaireResponse.questionnaire: minimum required = 1, but only found 0
    - QuestionnaireResponse.authored: minimum required = 1, but only found 0
- ❌ SDCQuestionnaireAdaptClass (1 errors)
    - An adaptive questionnaire must be a contained resource within a QuestionnaireResponse.
- ❌ SDCQuestionnaireExtractTemplateClass (4 errors)
    - Unable to find resourceType property
    - Resource requires an id, but none is present
    - Either the `templateExtract` or a `templateExtractBundle` extension must be provided (or both).
    - The contained resource 'null' is not referenced to from elsewhere in the containing resource nor does it refer to the containing resource (dom-3)
- ❌ SDCQuestionnairePopulateObservationClass (1 errors)
    - The observationLinkPeriod extension must appear at least once in the Questionnaire
- ❌ SDCQuestionnaireResponseAdaptClass (3 errors)
    - Unable to find resourceType property
    - Resource requires an id, but none is present
    - The contained resource 'null' is not referenced to from elsewhere in the containing resource nor does it refer to the containing resource (dom-3)
- ❌ SDCTaskQuestionnaireClass (1 errors)
    - Either code is 'fulfill', focus is ServiceRequest and no 'questionnaire' input; or code is 'complete-questionnaire', focus is omitted and 'questionnaire' input is present
- ❌ SDCCodeSystemClass (1 errors)
    - If version is present, versionAlgorithm must be present.
- ❌ SDCLibraryClass (1 errors)
    - The element text is present in the instance but not allowed in the applicable fixed value specified in profile
- ❌ SDCValueSetClass (1 errors)
    - If version is present, versionAlgorithm must be present.

---

[← Back to Summary](./pipeline-parity-summary.md)
