---
url: /parity-report/docs/validation.md
description: >-
  How BabelFHIR-TS generates FHIRPath runtime validators from
  StructureDefinitions, what constraints are checked, parity testing against HL7
  and Firely validators, and known limitations.
---

# Validation

BabelFHIR-TS generates runtime validators that evaluate FHIRPath constraints from StructureDefinitions. This page covers what the validators check, their limitations, and how they compare to external FHIR validators.

## What Validators Check

The generated `validate()` methods **DO** check:

* **FHIRPath constraints** from StructureDefinition invariants
* **Cardinality rules** (min/max occurrences)
* **Required fields** from profiles
* **Pattern constraints** (`patternCodeableConcept`, `patternCoding`)
* **Fixed values** (top-level scalar fields, `meta.profile`)
* **Prohibited fields** (`max=0`)
* **Slice validation** for extension URL, pattern/value, and exists-extension discriminators
* **Required ValueSet bindings** (inline code validation when ValueSet is resolved)
* **Bundle reference resolution** (checks that bundled/contained references resolve)
* **Extension structural rules** (`ext-1`, `url` required, empty object check)
* **Data type correctness** (string, number, boolean, etc.)

## What Validators Don't Check

The generated validators **DO NOT** check:

* **Terminology validation** for non-required bindings or large ValueSets without `--tx-server`
* **Cross-resource reference resolution** (checking that references to external resources exist)
* **Complex discriminator types** (type, position) — only pattern/value, extension URL, and exists-extension discriminators supported
* **Cross-resource business rules** — application-specific logic

::: tip
For comprehensive conformance testing, use the official [HL7 FHIR Validator](https://confluence.hl7.org/display/FHIR/Using+the+FHIR+Validator).
:::

## Runtime Validator Options

Every generated `validate()` function accepts an optional `ValidatorOptions` object as a second parameter. This enables runtime terminology validation, reference resolution, and debugging:

```ts
import { validateUSCorePatientProfile } from "hl7.fhir.us.core-generated/USCorePatientProfile";

const result = await validateUSCorePatientProfile(myPatient, {
  terminologyUrl: "https://tx.fhir.org/r4",
  fhirServerUrl: "https://hapi.fhir.org/baseR4",
  httpHeaders: {
    "https://tx.fhir.org/r4": "Bearer my-token",
  },
  traceFn: (value, label) => console.log(`[trace] ${label}:`, value),
});
```

### Available Options

| Option | Type | Description |
|---|---|---|
| `terminologyUrl` | `string` | Terminology server URL for `memberOf()` evaluation. When set, validators make HTTP calls to `$validate-code` for ValueSet bindings that couldn't be resolved at generation time. |
| `fhirServerUrl` | `string` | FHIR server URL for `resolve()` evaluation. When set, validators resolve external references by fetching from this server. |
| `httpHeaders` | `Record<string, string>` | HTTP headers keyed by server URL. Use for authentication with terminology or FHIR servers. |
| `signal` | `AbortSignal` | Cancels long-running async evaluations (e.g., terminology lookups). |
| `traceFn` | `(value: any, label: string) => void` | Debug callback invoked for every FHIRPath `trace()` call. Useful for diagnosing constraint evaluation. |

::: info
Without `terminologyUrl`, validators skip `memberOf()` checks and report no errors for unresolvable ValueSet bindings. Without `fhirServerUrl`, `resolve()` expressions are not evaluated.
:::

## Continuous Validation Pipeline

Every pull request runs two independent CI pipelines that validate generated code against real-world FHIR Implementation Guides. For each IG, the pipeline:

1. Downloads the FHIR package from a registry
2. Generates TypeScript interfaces, validators, and classes
3. Compiles the output with `tsc` (zero errors required)
4. Generates `empty()` and `random()` test resources for every profile
5. Validates those resources against two external FHIR validators

### Tested Implementation Guides (30 packages)

| Category | Implementation Guide | Package | FHIR |
|---|---|---|---|
| US | US Core | `hl7.fhir.us.core@8.0.0` | R4 |
| US | QI-Core | `hl7.fhir.us.qicore@6.0.0` | R4 |
| US | mCODE | `hl7.fhir.us.mcode@4.0.0` | R4 |
| US | SDOH Clinical Care | `hl7.fhir.us.sdoh-clinicalcare@2.2.0` | R4 |
| US | NDH (National Directory) | `hl7.fhir.us.ndh@1.0.0` | R4 |
| US | CARIN BB | `hl7.fhir.us.carin-bb@2.1.0` | R4 |
| US | CQF Measures | `hl7.fhir.us.cqfmeasures@4.0.0` | R4 |
| US | Physical Activity | `hl7.fhir.us.physical-activity@1.0.0` | R4 |
| DaVinci | PAS | `hl7.fhir.us.davinci-pas@2.0.1` | R4 |
| DaVinci | CDex | `hl7.fhir.us.davinci-cdex@2.1.0` | R4 |
| DaVinci | PDex | `hl7.fhir.us.davinci-pdex@2.1.0` | R4 |
| DaVinci | DTR | `hl7.fhir.us.davinci-dtr@2.1.0` | R4 |
| DaVinci | Alerts | `hl7.fhir.us.davinci-alerts@1.0.0` | R4 |
| DaVinci | DEQM | `hl7.fhir.us.davinci-deqm@4.0.0` | R4 |
| DaVinci | Drug Formulary | `hl7.fhir.us.davinci-drug-formulary@2.1.0` | R4 |
| Universal | IPS | `hl7.fhir.uv.ips@2.0.0` | R4 |
| Universal | SMART App Launch | `hl7.fhir.uv.smart-app-launch@2.2.0` | R4 |
| Universal | SDC (Structured Data Capture) | `hl7.fhir.uv.sdc@3.0.0` | R4 |
| Universal | Genomics Reporting | `hl7.fhir.uv.genomics-reporting@3.0.0` | R4 |
| Universal | CPG (Clinical Practice Guidelines) | `hl7.fhir.uv.cpg@2.0.0` | R4 |
| DE | ISiK Basis | `de.gematik.isik-basismodul@4.0.3` | R4 |
| DE | ISiK Medikation | `de.gematik.isik-medikation@4.0.1` | R4 |
| DE | KBV eRezept | `kbv.ita.erp@1.1.1` | R4 |
| DE | DE Basisprofil | `de.basisprofil.r4@1.5.0` | R4 |
| CH | CH Core (Switzerland) | `ch.fhir.ig.ch-core@5.0.0` | R4 |
| AU | AU Core (Australia) | `hl7.fhir.au.core@1.0.0` | R4 |
| IHE | PIXm | `ihe.iti.pixm@3.0.4` | R4 |
| IHE | MHD | `ihe.iti.mhd@4.2.2` | R4 |
| R5 | AE Research (R5) | `hl7.fhir.uv.ae-research-ig@1.0.1` | R5 |
| R5 | eMedicinal Product (R5) | `hl7.fhir.uv.emedicinal-product-info@1.0.0` | R5 |

### Firely SDK Validator

The first pipeline validates generated resources using the [Firely SDK Validator](https://docs.fire.ly/projects/Firely-NET-SDK/validation.html) — NuGet package `Firely.Fhir.Validation.R4` (v3.x), running on the [Firely .NET SDK](https://docs.fire.ly/projects/Firely-NET-SDK/) `Hl7.Fhir.R4` (v6.x).

These are two separate packages on separate version lines, and the report shows both. A validator version of 3.x alongside an SDK version of 6.x is expected — it does not mean the SDK is out of date.

The pipeline always validates against the **newest** release of each, matching how it always runs the newest HL7 Java Validator. [`FirelyValidator.csproj`](https://github.com/babelfhir-ts/BabelFHIR-TS/blob/main/scripts/firely-validator/FirelyValidator.csproj) declares major-bounded floating ranges (`3.*`, `6.*`) and carries no lock file, so every CI restore re-resolves them. The exact versions a given run used are recorded in the report header.

::: warning Known Firely SDK Issues
52 profiles are excluded from Firely validation due to schema loading or parser bugs in the Firely SDK, or to defects in the profiles themselves. See [Firely SDK Exclusions](#firely-sdk-exclusions) below.
:::

### HL7 Java Validator

The second pipeline validates using the [official HL7 FHIR Validator](https://confluence.hl7.org/display/FHIR/Using+the+FHIR+Validator) (v6.10.3), the reference implementation for FHIR conformance checking.

::: warning Known HL7 Validator Issues
27 profiles are excluded from HL7 validation due to terminology server limitations, profile resolution failures, missing snapshots, or cross-profile validation issues. See [HL7 Java Validator Exclusions](#hl7-java-validator-exclusions) below.
:::

::: info
Terminology validation requires a tx server. The pipeline uses `--tx-server https://tx.fhir.org/r4` during generation to expand ValueSets and produce valid codes.
:::

📊 **[Full Parity Report](https://babelfhir-ts.github.io/parity-report/)**

## Firely SDK Exclusions

52 profiles are excluded from Firely validation statistics because they fail for reasons outside the generated code: bugs in the Firely SDK Validator's profile/schema loading or parser, or a discriminator in the published profile that no instance can satisfy.

### Discriminator Loading Failures

The Firely SDK cannot evaluate complex discriminator expressions in certain StructureDefinitions (`fixed[x]`/`pattern[x]`/`resolve()` errors). **15 profiles** across 4 IGs:

| Package | Profiles | Error Pattern |
|---|---|---|
| ISiK Basis | ISiKOrganisation, ISiKOrganisationFachabteilung, ISiKAngehoeriger, ISiKPersonImGesundheitsberuf, ISiKPatient | `discriminator should have a 'fixed[x]', 'pattern[x]' or binding element` |
| IPS | CompositionUvIps, DiagnosticReportUvIps, BundleUvIps | `discriminator path 'resolve()'` — FHIR R4 spec explicitly supports this |
| CH Core | CHCorePractitioner, CHCorePractitionerEPR, CHCorePatient, CHCorePatientEPR | `Failed to load 'ch-core-address'` — compound discriminator on Extension |
| DaVinci PAS | PASClaimBase, PASClaim, PASClaimUpdate, PASClaimInquiry, PASRequestBundle, PASInquiryRequestBundle | `Failed to load` — discriminator evaluation failure |

### Parser Ordering Bug

The Firely SDK reports false element ordering errors (`coding` vs `text`) when parsing against certain profiles. The same resources validate without errors against base FHIR resource types. **5 profiles:**

| Package | Profiles |
|---|---|
| ISiK Basis | ISiKDiagnose, ISiKProzedur |
| DaVinci PAS | PASEncounter, PASDeviceRequest, PASTask |

### `resolve()` Discriminators

FHIR R4 lists `resolve()` as a legal discriminator path, and eight profiles use it to slice a reference by the profile its target conforms to. Firely rejects the path and abandons the schema, then validates against the base resource type. **8 profiles:**

| Package | Profiles | Element |
|---|---|---|
| IPS | CompositionUvIps, DiagnosticReportUvIps | `Composition.section:sectionMedications.entry`, `DiagnosticReport.result` |
| Physical Activity | PAConditionLowPA, PADiagnosticReport, PAGoal | `Condition.evidence.detail`, `DiagnosticReport.result`, `Goal.addresses` |
| SDOH | SDOHCCCondition, SDOHCCTaskForPatient | `Condition.evidence.detail`, `Task.partOf` |
| mCODE | TNMStageGroup | `Observation.hasMember` (`$this.resolve()`) |

### Snapshot Generator Crash

Firely's snapshot generator raises `Internal error ... (ElementMatcher.constructChoiceTypeMatch): choice type of diff does not occur in snap` for the NDH Practitioner profiles, naming the same path on both sides of the comparison. **3 profiles:** NdhPractitioner, NdhNdApiPractitioner, NdhPnLdApiPractitioner.

### Unmatchable Discriminators in the Profile

Six profiles slice on a value discriminator whose slice sets no `fixed[x]`, `pattern[x]` or binding, so no instance can ever satisfy it. Firely refuses to build the schema and validates the resource against its base type instead, reporting only the base type's required elements. The defect is in the published StructureDefinition, not in the validator:

| Package | Profiles | Discriminator |
|---|---|---|
| CPG | CHFBodyWeight, CHFO2Sat, CHFPotassium | `Observation.category` slice |
| AU Core | AUCorePathologyResult | `Observation.category:specificDiscipline.coding.code` |
| SDOH | SDOHCCObservationRaceOMB, SDOHCCObservationEthnicityOMB | `Observation.component:*Description.value[x]` |
| DaVinci PAS | PASClaimBase, PASClaim, PASClaimInquiry, PASClaimUpdate | `Claim.careTeam:OverallClaimMember` — value discriminator on a `boolean` |
| ISiK Basis | ISiKAngehoeriger | `RelatedPerson.name:Name` — pattern discriminator with no pattern |
| IHE MHD | FindDocumentReferencesResponse | `Bundle.entry:DocumentReference` — discriminator always succeeds |
| AU Core | AUCoreBloodPressure | `Observation.component:SystolicBP.code` — coding sliced to more than one choice |

::: tip
Both validators exclude profiles independently. Some profiles (e.g. ISiKOrganisation, ISiKPatient) are excluded from **both** pipelines for different reasons.
:::

## Keeping the Exclusion List Honest

Every exclusion records a *diagnosis*, and diagnoses go stale: the validator ships a fix, or an earlier harness bug turns out to have been the real cause. A stale entry is worse than no entry, because the report reads as parity while the check is simply not happening.

[`scripts/audit-parity-exclusions.mjs`](https://github.com/babelfhir-ts/BabelFHIR-TS/blob/main/scripts/audit-parity-exclusions.mjs) replays a run's recorded comparisons through the harness's own comparator, once with each exclusion applied and once without, and sorts every entry into *obsolete* (passes without it — delete), *load-bearing* (passes only with it — keep), *ineffective* (fails either way — the reason no longer describes what happens) or *unmeasured*.

### The re-check protocol

1. **Audit at least two runs.** Three entries read obsolete against a single run, were deleted, and failed in the next one.
2. **A run count does not settle a terminology-dependent finding.** Those same three then read obsolete across two consecutive runs and were still live, because whether the HL7 validator reports them depends on what the terminology server answers that day. Entries like that carry `intermittent: true` and the audit refuses to propose them for deletion. Flag an entry that behaves this way rather than deleting it a second time.
3. **Measure profile-level entries deliberately.** Run the pipeline with `PARITY_AUDIT_EXCLUSIONS=1`, which switches every curated exclusion off, so the suppressed comparisons actually run. Those numbers are diagnostic only and must never be published as the pipeline's own.
4. **Check the version spread.** The audit prints how many entries are pinned to each validator version. Anything older than the version in the run report has not been re-verified since.
5. **Deleting is the risky direction.** Keeping a live entry costs one tolerated field; deleting one costs a red pipeline. When in doubt, keep it and re-audit.

Profile-level exclusions come back *unmeasured* by construction: suppressing the profile suppresses the comparison, so the artifacts cannot say whether the exclusion is still needed. Those have to be audited by re-running with them disabled. Their `validatorVersion` is deliberately left at the version they were last verified against, so the gap between that and the version in the report is the staleness signal.

## HL7 Java Validator Exclusions

27 profiles are excluded from HL7 validation statistics due to terminology server limitations, profile resolution failures, missing snapshots, cross-profile validation, or discriminator evaluation failures.

### Profile Resolution Failures

The HL7 validator cannot resolve profile references needed for slicing evaluation. **7 profiles** in ISiK Basis:

| Profile | Error Pattern |
|---|---|
| ISiKOrganisation, ISiKOrganisationFachabteilung | `Unable to resolve profile` (identifier-bsnr) |
| ISiKAllergieUnvertraeglichkeit | `Unable to resolve profile` (CodingASK) |
| ISiKPersonImGesundheitsberuf | `Unable to resolve profile` (identifier-efn) |
| ISiKAbrechnungsfall | `Unable to resolve profile` (identifier-abrechnungsnummer) |
| ISiKPatient | `Unable to resolve profile` (identifier-kvid-10) |
| ISiKProzedur | `Unable to resolve profile` (CodingOPS) |

### Missing Snapshots

The HL7 validator reports that certain StructureDefinitions have no snapshot, preventing validation. **3 profiles** in ISiK Basis:

| Profile | Error Pattern |
|---|---|
| ISiKDiagnose, ISiKVersicherungsverhaeltnisSelbstzahler, ISiKVersicherungsverhaeltnisGesetzlich | `has no snapshot - validation is ...` |

### Slicing Evaluation Failure

The HL7 validator cannot match discriminators for `$this`-based slicing. **1 profile:**

| Profile | Error Pattern |
|---|---|
| ISiKAngehoeriger | `Could not match any discriminators ($this) for slice RelatedPerson.name:Name` |

### Environment Errors

The HL7 validator reported internal errors unrelated to the generated resource content. **6 profiles:**

| Package | Profiles |
|---|---|
| ISiK Basis | ISiKBerichtBundle, ISiKPatientMergeSubscription, ISiKLebensZustand, ISiKCodeSystem |
| IPS | BundleUvIps |
| DaVinci PAS | PASTask |
