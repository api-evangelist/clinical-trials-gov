# ClinicalTrials.gov (clinical-trials-gov)

ClinicalTrials.gov is the U.S. National Institutes of Health (NIH) registry and results database of publicly and privately supported clinical studies of human participants conducted around the world. Operated by the National Library of Medicine (NLM), it provides a modern REST API (data-api v2) that returns study records, study metadata, search areas, and field definitions in JSON. The predecessor classic API remains available for legacy consumers but is being phased out in favor of the v2 API. Data is in the public domain and freely accessible without authentication.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/clinical-trials-gov/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/clinical-trials-gov/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Clinical Trials
- Government
- Health
- NIH
- Open Data
- Public Health
- Research

## Timestamps

- **Created:** 2024-01-01
- **Modified:** 2026-04-23

## APIs

### ClinicalTrials.gov Data API v2

The ClinicalTrials.gov Data API v2 is the modern public REST interface to the NIH clinical-studies registry. It exposes study records, study metadata, search areas, study fields, version history, and statistics endpoints. Responses are JSON by default and the API is open and unauthenticated. The base URL is https://clinicaltrials.gov/api/v2 and operations include /studies, /studies/{nctId}, /studies/metadata, /studies/search-areas, /studies/enums, /version, and /stats.

- **Human URL:** [https://clinicaltrials.gov/data-api/api](https://clinicaltrials.gov/data-api/api)
- **Base URL:** `https://clinicaltrials.gov/api/v2`

#### Tags

- Clinical Trials
- REST
- Search
- Studies

#### Properties

- [Documentation](https://clinicaltrials.gov/data-api/api)
- [About](https://clinicaltrials.gov/data-api/about-api)
- [OpenAPI](openapi/clinical-trials-gov-data-api-v2-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### ClinicalTrials.gov Classic API

The Classic API is the legacy ClinicalTrials.gov interface that preceded the Data API v2 and exposes full-study, brief-study, and field-values endpoints with XML, JSON, and CSV responses. It is being deprecated in favor of the v2 REST API and remains online for backward compatibility while consumers migrate.

- **Human URL:** [https://clinicaltrials.gov/data-api/api](https://clinicaltrials.gov/data-api/api)
- **Base URL:** `https://clinicaltrials.gov/api`

#### Tags

- Clinical Trials
- Legacy
- REST

#### Properties

- [Documentation](https://clinicaltrials.gov/data-api/api)
- [Postman Collection](collections/clinical-trials-gov.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clinical-trials-gov.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ClinicalTrials.gov Bulk Downloads

ClinicalTrials.gov provides bulk CSV and JSON downloads of the full study registry through the data-api download endpoints. These artifacts support large-scale analytics, archival, and offline mirrors of the registry without making per-record API calls.

- **Human URL:** [https://clinicaltrials.gov/data-api/about-api/csv-download](https://clinicaltrials.gov/data-api/about-api/csv-download)

#### Tags

- Bulk
- Datasets
- Open Data

#### Properties

- [Documentation](https://clinicaltrials.gov/data-api/about-api/csv-download)
- [Postman Collection](collections/clinical-trials-gov.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clinical-trials-gov.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### AACT Database

AACT (Aggregate Analysis of ClinicalTrials.gov) is a publicly available relational database of all ClinicalTrials.gov study content maintained by the Clinical Trials Transformation Initiative (CTTI) at Duke University. It is updated daily and is widely used by researchers as a SQL-friendly mirror of the registry.

- **Human URL:** [https://aact.ctti-clinicaltrials.org/](https://aact.ctti-clinicaltrials.org/)

#### Tags

- Analytics
- Database
- Postgres
- Research

#### Properties

- [Documentation](https://aact.ctti-clinicaltrials.org/)
- [Data  Dictionary](https://aact.ctti-clinicaltrials.org/data_dictionary)
- [Postman Collection](collections/clinical-trials-gov.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clinical-trials-gov.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://clinicaltrials.gov/)
- [About](https://clinicaltrials.gov/about-site)
- [Documentation](https://clinicaltrials.gov/data-api/api)
- [Portal](https://clinicaltrials.gov/data-api)
- [Glossary](https://clinicaltrials.gov/study-basics/glossary)
- [News](https://clinicaltrials.gov/about-site/announcements)
- [Help](https://clinicaltrials.gov/help)
- [Privacy Policy](https://www.nlm.nih.gov/privacy.html)
- [Terms of Service](https://clinicaltrials.gov/about-site/terms-conditions)
- [Git Hub](https://github.com/clinicaltrialsgov)
- [JSON-LD](json-ld/clinical-trials-gov-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Spectral Rules](rules/clinical-trials-gov-rules.yml) — [Spectral](https://docs.stoplight.io/docs/spectral)
- [L L Ms Txt](https://clinicaltrials.gov/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** kinlane@gmail.com
