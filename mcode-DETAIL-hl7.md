# mcode - Detailed Report (FHIR all)
Generated: 2026-09-04T19:55:44.162Z

Package: `hl7.fhir.us.mcode@4.0.0`
FHIR Release: all

## Summary

| Metric | Passed | Total | Rate |
|--------|--------|-------|------|
| Empty Validation Parity | 37 | 37 | 100% |
| Random Validation Parity | 38 | 38 | 100% |
| Random Generation Validation + Parity | 31 | 38 | 82% |


---

## Empty Validation Parity Results

### ✅ Passing (37)
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
- ✅ CancerDiseaseStatusClass
- ✅ CancerRiskAssessmentClass
- ✅ CancerStageClass
- ✅ ComorbiditiesClass
- ✅ DeauvilleScaleClass
- ✅ ECOGPerformanceStatusClass
- ✅ GenomicRegionStudiedClass
- ✅ GenomicsReportClass
- ✅ GenomicVariantClass
- ✅ HistologicBehaviorAndTypeClass
- ✅ HistologicGradeClass
- ✅ HistoryOfMetastaticCancerClass
- ✅ KarnofskyPerformanceStatusClass
- ✅ LanskyPlayPerformanceStatusClass
- ✅ LymphomaStageClass
- ✅ RadiotherapyCourseSummaryClass
- ✅ RadiotherapyVolumeClass
- ✅ RhabdomyosarcomaRiskAssessmentClass
- ✅ TNMCategoryClass
- ✅ TNMDistantMetastasesCategoryClass
- ✅ TNMPrimaryTumorCategoryClass
- ✅ TNMRegionalNodesCategoryClass
- ✅ TNMStageGroupClass
- ✅ TumorClass
- ✅ TumorMarkerTestClass
- ✅ TumorMorphologyClass
- ✅ TumorSizeClass

### ❌ Failing (0)
_None_

### ⚠️ Excluded - External Issues (1)
- ⚠️ BodySurfaceAreaClass (excluded - Validator bug)

---

## Random Validation Parity Results

### ✅ Passing (38)
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
- ✅ GenomicVariantClass
- ✅ HistologicBehaviorAndTypeClass
- ✅ HistologicGradeClass
- ✅ HistoryOfMetastaticCancerClass
- ✅ KarnofskyPerformanceStatusClass
- ✅ LanskyPlayPerformanceStatusClass
- ✅ LymphomaStageClass
- ✅ RadiotherapyCourseSummaryClass
- ✅ RadiotherapyVolumeClass
- ✅ RhabdomyosarcomaRiskAssessmentClass
- ✅ TNMCategoryClass
- ✅ TNMDistantMetastasesCategoryClass
- ✅ TNMPrimaryTumorCategoryClass
- ✅ TNMRegionalNodesCategoryClass
- ✅ TNMStageGroupClass
- ✅ TumorClass
- ✅ TumorMarkerTestClass
- ✅ TumorMorphologyClass
- ✅ TumorSizeClass

### ❌ Failing (0)
_None_

---

## Random Generation Validation + Parity Results

### ✅ Passing (31)
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
- ✅ TNMStageGroupClass
- ✅ TumorClass
- ✅ TumorMarkerTestClass
- ✅ TumorMorphologyClass

### ❌ Failing (7)
- ❌ GenomicsReportClass (1 errors)
    - Slice 'DiagnosticReport.category:Genetics': a matching slice is required, but not found
- ❌ GenomicVariantClass (1 errors)
    - None of the codings provided are in the value set 'LOINC Answer Codes for LL1971-2' (http://loinc.org/vs/LL1971-2), and a coding from this value set is required) (codes = http://terminology.hl7.org/CodeSystem/data-absent-reason#unknown)
- ❌ LymphomaStageClass (1 errors)
    - None of the codings provided are in the value set 'Lymphoma Stage Value Set' (http://hl7.org/fhir/us/mcode/ValueSet/mcode-lymphoma-stage-value-vs|4.0.0), and a coding from this value set is required) (codes = http://terminology.hl7.org/CodeSystem/data-absent-reason#unknown)
- ❌ RadiotherapyCourseSummaryClass (1 errors)
    - The Profile 'http://hl7.org/fhir/us/mcode/StructureDefinition/mcode-radiotherapy-course-summary|4.0.0' definition allows for the type Period but found type dateTime
- ❌ RadiotherapyVolumeClass (1 errors)
    - One of description or identifier MUST be present
- ❌ RhabdomyosarcomaRiskAssessmentClass (1 errors)
    - None of the codings provided are in the value set 'Rhabdomyosarcoma Assessment Value Set' (http://hl7.org/fhir/us/mcode/ValueSet/mcode-rhabdomyosarcoma-assessment-value-vs|4.0.0), and a coding from this value set is required) (codes = http://terminology.hl7.org/CodeSystem/data-absent-reason#unknown)
- ❌ TumorSizeClass (1 errors)
    - Either `focus` OR `specimen` MUST be populated

---

[← Back to Summary](./pipeline-parity-summary.md)
