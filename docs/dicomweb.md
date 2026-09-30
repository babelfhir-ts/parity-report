---
url: /parity-report/docs/dicomweb.md
description: >-
  Generate typed DICOMweb helpers that bridge FHIR ImagingStudy profiles with
  DICOMweb APIs and Cornerstone3D viewers using the --dicomweb flag.
---

# DICOMweb Integration

BabelFHIR-TS can generate typed DICOMweb helpers that bridge FHIR ImagingStudy profiles with DICOMweb APIs and Cornerstone3D rendering.

## Enabling DICOMweb

Pass the `--dicomweb` flag during generation:

```bash
babelfhir-ts install hl7.fhir.us.core@8.0.0 --dicomweb
```

This generates a `dicomweb/` directory in the output with helpers typed to your IG's ImagingStudy profiles.

## What Gets Generated

| File | Description |
|---|---|
| `dicomweb/index.ts` | Re-exports from `@babelfhir-ts/dicomweb` with typed overloads for IG-specific ImagingStudy profiles |
| `dicomweb/cornerstone.ts` | Re-exports Cornerstone3D integration helpers |

If your IG contains ImagingStudy profiles, a union type `ImagingStudyProfile` is generated that narrows all helpers to your specific profiles. If no ImagingStudy profiles are found, generic helpers are re-exported.

## Base Package

The runtime helpers come from [`@babelfhir-ts/dicomweb`](https://www.npmjs.com/package/@babelfhir-ts/dicomweb), which is automatically added as a dependency of the generated package.

## DICOMweb Client

Create a client for building DICOMweb URLs:

```ts
import { createDicomwebClient } from "my-ig-generated/dicomweb";

const dw = createDicomwebClient({
  baseUrl: "https://pacs.example.com/dicomweb",
  getAccessToken: () => myToken,
});

// Build URLs for thumbnails, metadata, and search
const thumbUrl = dw.studyThumbnailUrl(studyUID);
const metaUrl = dw.studyMetadataUrl(studyUID);
const seriesUrl = dw.seriesSearchUrl(studyUID);

// Auth headers for direct fetch
const headers = dw.authHeaders();
```

## FHIR-to-DICOM Mapping

Extract DICOM identifiers and metadata from FHIR ImagingStudy resources:

```ts
import {
  getStudyInstanceUID,
  getPrimaryModality,
  getStudyTitle,
  getModalityInfo,
} from "my-ig-generated/dicomweb";

const uid = getStudyInstanceUID(imagingStudy);  // DICOM Study Instance UID
const modality = getPrimaryModality(imagingStudy);  // e.g., "CT"
const title = getStudyTitle(imagingStudy);  // Human-readable title

if (modality) {
  const info = getModalityInfo(modality);
  console.log(`${info.emoji} ${info.label}`);  // e.g., "🫁 Computed Tomography"
}
```

## DICOM-to-FHIR: building an ImagingStudy from bytes

The inverse of the mapping above. Given the DICOM a patient or a department just
handed over, build the `ImagingStudy` that makes it visible to anything querying
FHIR rather than only to the PACS:

```ts
import {
  collectDicomFiles,
  parseDicomMeta,
  groupByStudy,
  buildImagingStudy,
} from "my-ig-generated/dicomweb";

// 1. Whatever was dropped → DICOM instances. Expands zips, and detects instances
//    by the DICM magic at byte 128 rather than by filename: real imaging media
//    ships extensionless files under DICOM/ next to a DICOMDIR index.
const { instances, skipped, mediaIndexes } = await collectDicomFiles(dropped);

// 2. Bytes → metadata → studies
const metas = (await Promise.all(instances.map(async (f) =>
  parseDicomMeta(new Uint8Array(await f.arrayBuffer()))))).filter((m) => m !== null);

// 3. One ImagingStudy per study, with a contained WADO-RS endpoint
for (const [uid, study] of groupByStudy(metas)) {
  const resource = buildImagingStudy(study, `Patient/${patientId}`, dicomwebBaseUrl);
  // PUT ImagingStudy?identifier=urn:dicom:uid|urn:oid:<uid> — conditional update,
  // so re-uploading a study updates it rather than duplicating it.
}
```

`buildImagingStudy` returns a STRUCTURAL shape (`BuiltImagingStudy`), not an
`fhir/r4` type: this package carries no FHIR-version dependency, and the result is
assignable to R4's `ImagingStudy` and to an IG-profiled one alike, so the caller
keeps whichever type it validates against.

The parser reads only the tags an ImagingStudy needs and stops before pixel data,
so a study's worth of instances costs a few kilobytes each. It handles explicit
and implicit VR little-endian, including undefined-length sequences appearing
before the 0020 group — the shape real scanner exports produce and naive parsers
trip on.

## Cornerstone3D Integration

For medical image rendering with [Cornerstone3D](https://www.cornerstonejs.org/), use the Cornerstone submodule:

```ts
import { buildImageId, fetchSeriesImageIds } from "my-ig-generated/dicomweb/cornerstone";

// Build a single wadors: imageId
const imageId = buildImageId(wadoRsRoot, studyUID, seriesUID, sopUID);

// Fetch all imageIds for a series (ready for viewport.setStack())
const imageIds = await fetchSeriesImageIds(wadoRsRoot, studyUID, seriesUID, authHeaders);
```

### Full Cornerstone Client

For a higher-level API that handles metadata caching and Cornerstone registration:

```ts
import { createCornerstoneDicomweb } from "@babelfhir-ts/dicomweb/cornerstone";
import * as dicomImageLoader from "@cornerstonejs/dicom-image-loader";

const dw = createCornerstoneDicomweb({
  baseUrl: "https://pacs.example.com/dicomweb",
  getAccessToken: () => token,
  cornerstone: { dicomImageLoader },
});

// Loads metadata, registers with Cornerstone, returns renderable imageIds
const { imageIds, fromCache } = await dw.loadSeries(studyUID, seriesUID);
viewport.setStack(imageIds);

// Load all series in a study in parallel
const result = await dw.loadStudy(studyUID, /* concurrency */ 4);

// Cache management
dw.evictStudy(studyUID);
console.log(dw.cacheStats()); // { studies, series, instances }
```

## Package Exports

When `--dicomweb` is used, the generated package exposes these subpath exports:

```json
{
  "./dicomweb": "./dicomweb/index.js",
  "./dicomweb/cornerstone": "./dicomweb/cornerstone.js"
}
```

## Additional Utilities

The `@babelfhir-ts/dicomweb` package also exports lower-level DICOM JSON helpers:

```ts
import { Tag, getValue, getNumberValue, getStringValue } from "@babelfhir-ts/dicomweb";
import { getFrameCount, isMultiframe } from "@babelfhir-ts/dicomweb";
import { MetadataCache } from "@babelfhir-ts/dicomweb";
```
