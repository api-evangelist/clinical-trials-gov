# ClinicalTrials.gov

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

**Areas:** Clinical Trials · Government · Health · NIH · Open Data · Public Health · Research

## ClinicalTrials.gov on APIs.io

Everything profiled for ClinicalTrials.gov is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/clinical-trials-gov/](https://apis.io/providers/clinical-trials-gov/)** — or go straight to one of the APIs or properties below.

### APIs (6)

- [ClinicalTrials.gov Classic API](https://apis.io/apis/clinical-trials-gov/classic-api/) — RETIRED. The Classic API was withdrawn in June 2024 and its endpoints now return HTTP 404 (probed 2026-09-06: /api/query/full_studies and /api/info/data_vrs…
- [ClinicalTrials.gov Bulk Downloads](https://apis.io/apis/clinical-trials-gov/bulk-downloads/) — ClinicalTrials.gov provides bulk CSV and JSON downloads of the full study registry through the data-api download endpoints. These artifacts support…
- [AACT Database](https://apis.io/apis/clinical-trials-gov/aact/) — AACT (Aggregate Analysis of ClinicalTrials.gov) is a publicly available relational database of all ClinicalTrials.gov study content maintained by the…
- [ClinicalTrials.gov Stats API](https://apis.io/apis/clinical-trials-gov/clinical-trials-gov-stats-api/) — The Stats API from ClinicalTrials.gov — 3 operation(s) for stats.
- [ClinicalTrials.gov Studies API](https://apis.io/apis/clinical-trials-gov/clinical-trials-gov-studies-api/) — The Studies API from ClinicalTrials.gov — 5 operation(s) for studies.
- [ClinicalTrials.gov Version API](https://apis.io/apis/clinical-trials-gov/clinical-trials-gov-version-api/) — The Version API from ClinicalTrials.gov — 1 operation(s) for version.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [ClinicalTrials.gov Data API v2 (candidate MCP surface)](https://apis.io/servers/clinical-trials-gov/clinicaltrials-gov-data-api-v2-candidate-mcp-surface/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Clinical Trials Gov Agentic Access](https://apis.io/agentic-access/clinical-trials-gov/clinical-trials-gov-agentic-access/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Clinical Trials Gov Context](https://apis.io/jsonld/clinical-trials-gov/clinical-trials-gov-context/)

#### Collections (4)

Postman and Open Collection request collections.

- [ClinicalTrials.gov Data API v2](https://apis.io/collections/clinical-trials-gov/open-clinical-trials-gov/)
- [ClinicalTrials.gov Data API v2 Stats API](https://apis.io/collections/clinical-trials-gov/open-clinical-trials-gov-stats-api/)
- [ClinicalTrials.gov Data API v2 Stats Studies API](https://apis.io/collections/clinical-trials-gov/open-clinical-trials-gov-studies-api/)
- [ClinicalTrials.gov Data API v2 Stats Version API](https://apis.io/collections/clinical-trials-gov/open-clinical-trials-gov-version-api/)

#### Overlays (3)

OpenAPI overlays, including conversational phrasing for each operation.

- [Clinical Trials Gov Stats Api Overlay](https://apis.io/overlays/clinical-trials-gov/clinical-trials-gov-stats-api-overlay/)
- [Clinical Trials Gov Studies Api Overlay](https://apis.io/overlays/clinical-trials-gov/clinical-trials-gov-studies-api-overlay/)
- [Clinical Trials Gov Version Api Overlay](https://apis.io/overlays/clinical-trials-gov/clinical-trials-gov-version-api-overlay/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [ClinicalTrials.gov API Rules](https://apis.io/rules/clinical-trials-gov/clinical-trials-gov-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Clinical Trials Gov Authentication](https://apis.io/security/clinical-trials-gov/clinical-trials-gov-authentication/)
- [Clinical Trials Gov Domain Security](https://apis.io/security/clinical-trials-gov/clinical-trials-gov-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Clinical Trials Gov Plans Pricing](https://apis.io/plans/clinical-trials-gov/clinical-trials-gov-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Clinical Trials Gov Rate Limits](https://apis.io/rate-limits/clinical-trials-gov/clinical-trials-gov-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://clinicaltrials.gov/)
- [Documentation](https://clinicaltrials.gov/data-api/api)
- [Getting started](https://clinicaltrials.gov/data-api/about-api)
- [API reference](https://clinicaltrials.gov/data-api/api)
- [Pricing](https://clinicaltrials.gov/about-site/terms-conditions)
- [Support](https://support.nlm.nih.gov/)
- [Changelog](https://clinicaltrials.gov/about-site/release-notes)
- [Blog](https://clinicaltrials.gov/blog/)
- [Terms of service](https://clinicaltrials.gov/about-site/terms-conditions)
- [Privacy policy](https://www.nlm.nih.gov/privacy.html)

## API Evangelist rating

**Kin Score 36.4** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 65.2 |
| Contract quality | 42.0 |
| Contract governance | 31.8 |
| Operational transparency | 0.0 |
| Developer ergonomics | 30.4 |
| Access clarity | 42.1 |

**Agent readiness 24.8** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | na |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | na |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | na |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 20.6** — Government & Public Sector

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/clinical-trials-gov/](https://apis.io/providers/clinical-trials-gov/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for ClinicalTrials.gov: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/clinical-trials-gov/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
