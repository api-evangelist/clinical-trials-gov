# ClinicalTrials.gov (clinical-trials-gov)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
