---
name: clinical-trials-gov-get-study-record
description: >-
  Retrieve one ClinicalTrials.gov study record by its NCT number, in JSON, CSV or HL7 FHIR,
  and pull only the fields you need out of the study data structure.
generated: '2026-09-06'
method: generated
source: >-
  openapi/clinical-trials-gov-studies-api-openapi.yml, data-model/clinical-trials-gov-data-model.yml
  and live probes of https://clinicaltrials.gov/api/v2 on 2026-09-06
api: clinical-trials-gov:clinical-trials-gov-studies-api
base_url: https://clinicaltrials.gov/api/v2
operations:
  - GET /studies/{nctId}
  - GET /studies/metadata
  - GET /version
operation_id_note: >-
  The harvested OpenAPI declares no operationId on any path; operations are named by
  METHOD + PATH exactly as the spec has them.
---

# Read one ClinicalTrials.gov study record

## 1. Fetch the record

```
GET https://clinicaltrials.gov/api/v2/studies/NCT00141635
```

The identifier is `NCT` plus 8 digits. Since API version 2.0.2 the endpoint **follows
NCTIdAlias redirects**, so a historical identifier resolves to the current record. A `404`
means no alias matched either — do not retry it, search instead.

## 2. Ask for only the fields you need

```
GET /studies/{nctId}?fields=protocolSection.statusModule,protocolSection.designModule
```

Field names come from `GET /studies/metadata`, the authoritative field dictionary. The record
is nested in five sections:

| Section | What it holds |
|---|---|
| `protocolSection` | what the study intends to do — identification, status, sponsor, design, arms, outcomes, eligibility, contacts and locations |
| `resultsSection` | what it found — present only when `hasResults` is `true` |
| `annotationSection` | registry annotations |
| `documentSection` | uploaded protocol / SAP / consent documents |
| `derivedSection` | fields NLM computes, including MeSH condition and intervention terms |

Check `hasResults` before reaching into `resultsSection`.

## 3. Choose a format

Format is a **query parameter**, not an `Accept` header:

```
GET /studies/{nctId}?format=json        # default
GET /studies/{nctId}?format=csv
GET /studies/{nctId}?format=fhir.json   # HL7 FHIR
```

`format=fhir.json` returns `Content-Type: application/fhir+json` — a FHIR `Bundle` whose
`ResearchStudy` entry carries
`meta.profile: http://hl7.org/fhir/uv/ebm/StructureDefinition/study-registry-record`, plus a
`Group` resource for the eligibility cohort. NLM documents this as a **pilot**
(https://clinicaltrials.gov/data-api/fhir). Use it when you are handing data to a system that
already speaks FHIR; it is a format projection, not a FHIR REST server — there is no
`/metadata` CapabilityStatement and no FHIR search.

## 4. Know how fresh the answer is

```
GET /version   ->   {"apiVersion":"2.0.5","dataTimestamp":"2026-09-04T09:00:06"}
```

The registry is updated daily. Quote `dataTimestamp`, not the time you called, when the
recency of a trial's status matters.

## Rules that bite

- No authentication, no key, no signup.
- No rate-limit headers and no published limit — pace yourself and back off on any non-200.
- Read-only: no writes, so no idempotency key and nothing to reverse.
- Data is U.S. Government public domain; attribution to NLM and ClinicalTrials.gov is requested,
  and some records may carry third-party copyright.
