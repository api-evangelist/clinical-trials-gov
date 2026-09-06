---
name: clinical-trials-gov-find-studies
description: >-
  Search the ClinicalTrials.gov registry for clinical studies matching a condition,
  intervention, location or sponsor, and page through the full result set without
  overrunning the API.
generated: '2026-09-06'
method: generated
source: >-
  openapi/clinical-trials-gov-studies-api-openapi.yml plus live probes of
  https://clinicaltrials.gov/api/v2 on 2026-09-06
api: clinical-trials-gov:clinical-trials-gov-studies-api
base_url: https://clinicaltrials.gov/api/v2
operations:
  - GET /studies
  - GET /studies/search-areas
  - GET /studies/enums
operation_id_note: >-
  The harvested OpenAPI declares no operationId on any path, so operations are named here by
  METHOD + PATH exactly as they appear in the spec. Nothing was invented to fill the field.
---

# Find clinical studies on ClinicalTrials.gov

The Data API v2 needs **no credential**. Every call below works unauthenticated over HTTPS.

## 1. Learn the query surface before you query

`query.*` parameters take **Essie expression syntax**, not plain strings, and each one targets
a named *search area*. Fetch the areas once and cache them:

```
GET https://clinicaltrials.gov/api/v2/studies/search-areas
GET https://clinicaltrials.gov/api/v2/studies/enums
```

`enums` gives you the legal values for `filter.overallStatus` and the other controlled fields.
Guessing a status string is the most common way this API returns nothing useful.

## 2. Search

```
GET /studies
  ?query.cond=<condition>
  &query.intr=<intervention>
  &query.locn=<place>
  &filter.overallStatus=RECRUITING
  &fields=protocolSection.identificationModule.nctId,protocolSection.identificationModule.briefTitle,protocolSection.statusModule.overallStatus
  &pageSize=100
  &countTotal=true
```

- **Always send `fields`.** A full study record is large; the field names come from
  `GET /studies/metadata`. Omitting `fields` returns everything and wastes most of it.
- `countTotal=true` gives you `totalCount` so you can decide whether to page at all.
- `pageSize` maxes out at **1000** (default 10).

## 3. Page

Pagination is **cursor-only** — there is no offset, so you cannot jump to page N.

```
GET /studies?...&pageToken=<nextPageToken from the previous response>
```

Stop when the response has no `nextPageToken`. Do not synthesise a token.

## Rules that bite

- **No rate-limit headers exist.** The API returns no `X-RateLimit-*`, no `RateLimit-*` and no
  `Retry-After`, and NLM publishes no limit. You get no warning before a limit, if one exists —
  so pace yourself deliberately (the site's `robots.txt` uses `Crawl-delay: 1` for crawlers)
  and back off on any non-200.
- **No RFC 9457 problem details.** Errors are bare; only a `404` on a missing study is
  documented. Treat any non-200 as opaque and log the whole body.
- **Read-only.** There is no way to create, update or delete a study through this API, so
  nothing here needs an idempotency key and nothing here can be undone — because nothing is
  done. Registration and results go through the separate PRS web application.
- **Data is public domain**, refreshed daily. Check `GET /version` `dataTimestamp` if freshness
  matters to your answer.
