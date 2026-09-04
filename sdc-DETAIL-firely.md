# sdc - Detailed Report (FHIR all)
Generated: 2026-08-29T11:15:19.699Z

Package: `hl7.fhir.uv.sdc@4.0.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 34 | 34 | 100% |
| Random Validation Parity | 31 | 34 | 91% |
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

### ✅ Passing (31)
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
- ✅ SDCQuestionnairePopulateExpressionClass
- ✅ SDCQuestionnairePopulateObservationClass
- ✅ SDCQuestionnairePopulateStructureMapClass
- ✅ SDCQuestionnaireRenderClass
- ✅ SDCQuestionnaireResponseClass
- ✅ SDCQuestionnaireResponseCommonClass
- ✅ SDCQuestionnaireSearchClass
- ✅ SDCQuestionnaireServiceRequestClass
- ✅ SDCTaskQuestionnaireClass
- ✅ SDCCodeSystemClass
- ✅ SDCValueSetClass

### ❌ Failing (3)
- ❌ SDCQuestionnaireExtractTemplateClass
  - Field-level comparison:
  Both validators: unclassified
  Only Internal: resourceType, constraint

- ❌ SDCQuestionnaireResponseAdaptClass
  - Field-level comparison:
  Both validators: unclassified
  Only Internal: resourceType

- ❌ SDCLibraryClass
  - Field-level comparison:
  Both validators: none
  Only Internal: text
  Only Firely: pattern


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
    - No elements matched required slice: 'useContext:library'
- ❌ SDCParametersQuestionnaireAssembleInClass (2 errors)
    - Missing required member: 'extension'
    - No elements matched required slice: 'extension:assemble-expectation'
- ❌ SDCParametersQuestionnaireNextQuestionnaireInClass (3 errors)
    - Missing required member: 'contained'
    - Missing required member: 'questionnaire'
    - Missing required member: 'authored'
- ❌ SDCParametersQuestionnaireNextQuestionnaireOutClass (3 errors)
    - Missing required member: 'contained'
    - Missing required member: 'questionnaire'
    - Missing required member: 'authored'
- ❌ SDCParametersQuestionnairePopulateOutClass (2 errors)
    - Missing required member: 'questionnaire'
    - Missing required member: 'authored'
- ❌ SDCParametersQuestionnaireProcessResponseInClass (2 errors)
    - Missing required member: 'questionnaire'
    - Missing required member: 'authored'
- ❌ SDCQuestionnaireAdaptClass (1 errors)
    - Instance failed constraint sdc-adapt-1 "An adaptive questionnaire must be a contained resource within a QuestionnaireResponse."
- ❌ SDCQuestionnaireExtractTemplateClass (1 errors)
    - One or more errors occurred. (Resource has no 'resourceType' property. At line 22, position 6.)
- ❌ SDCQuestionnairePopulateObservationClass (1 errors)
    - Instance failed constraint sdc-pop-2 "The observationLinkPeriod extension must appear at least once in the Questionnaire"
- ❌ SDCQuestionnaireResponseAdaptClass (1 errors)
    - One or more errors occurred. (Resource has no 'resourceType' property. At line 22, position 6.)
- ❌ SDCTaskQuestionnaireClass (1 errors)
    - Instance failed constraint sdc-t1 "Either code is 'fulfill', focus is ServiceRequest and no 'questionnaire' input; or code is 'complete-questionnaire', focus is omitted and 'questionnaire' input is present"
- ❌ SDCCodeSystemClass (1 errors)
    - Instance failed constraint sdc-2 "If version is present, versionAlgorithm must be present."
- ❌ SDCLibraryClass (1 errors)
    - Value '{"coding":[{"system":"http://terminology.hl7.org/CodeSystem/library-type","code":"logic-library","display":"Logic Library"}],"text":"Logic Library"}' is not exactly equal to fixed value '{"coding":[{"system":"http://terminology.hl7.org/CodeSystem/library-type","code":"logic-library","display":"Logic Library"}]}'
- ❌ SDCValueSetClass (1 errors)
    - Instance failed constraint sdc-2 "If version is present, versionAlgorithm must be present."

---

[← Back to Summary](./pipeline-parity-summary.md)
