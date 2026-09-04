# mcode - Detailed Report (FHIR all)
Generated: 2026-09-04T19:51:29.135Z

Package: `hl7.fhir.us.mcode@4.0.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 35 | 35 | 100% |
| Random Validation Parity | 35 | 35 | 100% |
| Random Generation Validation + Parity | 30 | 35 | 86% |


---

## Empty Validation Parity Results

### ✅ Passing (35)
- ✅ CancerPatientClass
- ✅ CancerRelatedMedicationAdministrationClass
- ✅ CancerRelatedMedicationRequestClass
- ✅ CancerRelatedSurgicalProcedureClass
- ✅ HumanSpecimenClass
- ✅ MCODEPatientBundleClass
- ✅ MCODEPatientGroupClass
- ✅ PrimaryCancerConditionClass
- ✅ SecondaryCancerConditionClass
- ✅ ALLRiskAssessmentClass
- ✅ BodySurfaceAreaClass
- ✅ CancerDiseaseStatusClass
- ✅ CancerRiskAssessmentClass
- ✅ CancerStageClass
- ✅ ComorbiditiesClass
- ✅ DeauvilleScaleClass
- ✅ ECOGPerformanceStatusClass
- ✅ GenomicRegionStudiedClass
- ✅ GenomicsReportClass
- ✅ HistologicBehaviorAndTypeClass
- ✅ HistologicGradeClass
- ✅ HistoryOfMetastaticCancerClass
- ✅ KarnofskyPerformanceStatusClass
- ✅ LanskyPlayPerformanceStatusClass
- ✅ RadiotherapyCourseSummaryClass
- ✅ RadiotherapyVolumeClass
- ✅ RhabdomyosarcomaRiskAssessmentClass
- ✅ TNMCategoryClass
- ✅ TNMDistantMetastasesCategoryClass
- ✅ TNMPrimaryTumorCategoryClass
- ✅ TNMRegionalNodesCategoryClass
- ✅ TumorClass
- ✅ TumorMarkerTestClass
- ✅ TumorMorphologyClass
- ✅ TumorSizeClass

### ❌ Failing (0)
_None_

---

## Random Validation Parity Results

### ✅ Passing (35)
- ✅ CancerPatientClass
- ✅ CancerRelatedMedicationAdministrationClass
- ✅ CancerRelatedMedicationRequestClass
- ✅ CancerRelatedSurgicalProcedureClass
- ✅ HumanSpecimenClass
- ✅ MCODEPatientBundleClass
- ✅ MCODEPatientGroupClass
- ✅ PrimaryCancerConditionClass
- ✅ SecondaryCancerConditionClass
- ✅ ALLRiskAssessmentClass
- ✅ BodySurfaceAreaClass
- ✅ CancerDiseaseStatusClass
- ✅ CancerRiskAssessmentClass
- ✅ CancerStageClass
- ✅ ComorbiditiesClass
- ✅ DeauvilleScaleClass
- ✅ ECOGPerformanceStatusClass
- ✅ GenomicRegionStudiedClass
- ✅ GenomicsReportClass
- ✅ HistologicBehaviorAndTypeClass
- ✅ HistologicGradeClass
- ✅ HistoryOfMetastaticCancerClass
- ✅ KarnofskyPerformanceStatusClass
- ✅ LanskyPlayPerformanceStatusClass
- ✅ RadiotherapyCourseSummaryClass
- ✅ RadiotherapyVolumeClass
- ✅ RhabdomyosarcomaRiskAssessmentClass
- ✅ TNMCategoryClass
- ✅ TNMDistantMetastasesCategoryClass
- ✅ TNMPrimaryTumorCategoryClass
- ✅ TNMRegionalNodesCategoryClass
- ✅ TumorClass
- ✅ TumorMarkerTestClass
- ✅ TumorMorphologyClass
- ✅ TumorSizeClass

### ❌ Failing (0)
_None_

---

## Random Generation Validation + Parity Results

### ✅ Passing (30)
- ✅ CancerPatientClass
- ✅ CancerRelatedMedicationAdministrationClass
- ✅ CancerRelatedMedicationRequestClass
- ✅ CancerRelatedSurgicalProcedureClass
- ✅ HumanSpecimenClass
- ✅ MCODEPatientBundleClass
- ✅ MCODEPatientGroupClass
- ✅ PrimaryCancerConditionClass
- ✅ SecondaryCancerConditionClass
- ✅ ALLRiskAssessmentClass
- ✅ BodySurfaceAreaClass
- ✅ CancerDiseaseStatusClass
- ✅ CancerRiskAssessmentClass
- ✅ CancerStageClass
- ✅ ComorbiditiesClass
- ✅ DeauvilleScaleClass
- ✅ ECOGPerformanceStatusClass
- ✅ GenomicRegionStudiedClass
- ✅ HistologicBehaviorAndTypeClass
- ✅ HistologicGradeClass
- ✅ HistoryOfMetastaticCancerClass
- ✅ KarnofskyPerformanceStatusClass
- ✅ LanskyPlayPerformanceStatusClass
- ✅ TNMCategoryClass
- ✅ TNMDistantMetastasesCategoryClass
- ✅ TNMPrimaryTumorCategoryClass
- ✅ TNMRegionalNodesCategoryClass
- ✅ TumorClass
- ✅ TumorMarkerTestClass
- ✅ TumorMorphologyClass

### ❌ Failing (5)
- ❌ GenomicsReportClass (1 errors)
    - No elements matched required slice: 'category:Genetics'
- ❌ RadiotherapyCourseSummaryClass (1 errors)
    - The declared type of the element (Period) is incompatible with that of the instance (dateTime).
- ❌ RadiotherapyVolumeClass (1 errors)
    - Instance failed constraint mcode-description-or-id-required "One of description or identifier MUST be present"
- ❌ RhabdomyosarcomaRiskAssessmentClass (1 errors)
    - Code 'unknown' (display 'Unknown') from system 'http://terminology.hl7.org/CodeSystem/data-absent-reason' does not exist in the value set 'Rhabdomyosarcoma Assessment Value Set' (http://hl7.org/fhir/us/mcode/ValueSet/mcode-rhabdomyosarcoma-assessment-value-vs), but the binding is of strength 'required'
- ❌ TumorSizeClass (1 errors)
    - Instance failed constraint must-have-focus-or-specimen-invariant "Either `focus` OR `specimen` MUST be populated"

---

[← Back to Summary](./pipeline-parity-summary.md)
