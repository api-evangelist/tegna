# Quarantined scaffold artifacts — NOT published by TEGNA

**Date quarantined:** 2026-08-13
**Quarantined by:** API Evangelist enrichment pipeline (local pass, `pipeline-enrich.md` STEP 0c ownership check)

Everything in this directory was **written by API Evangelist**, not harvested from TEGNA.
It is retained for audit rather than deleted. **Nothing here should be treated as evidence
that TEGNA publishes an API, and nothing here is wired into `apis.yml`.**

## Why these were quarantined

The OpenAPI definitions in `_scaffold/openapi/` declare a host that **does not exist**, and the
one host that does exist does not serve the paths the spec claims.

| Check | Result (probed 2026-08-13) |
|---|---|
| `dig api.tegna.com` (servers[] host of 8 of the 9 specs) | **NXDOMAIN** — no A record, no CNAME |
| `dig developer.tegna.com` / `docs.tegna.com` / `developers.tegna.com` | **NXDOMAIN** |
| `GET https://api.premion.com/v1/campaigns` (a declared path of the Premion spec) | **404** `Cannot GET /v1/campaigns` |
| `GET https://api.premion.com/v1` | **404** |
| `GET https://api.premion.com/` | 200 `{"message":"App is running"}` |
| `GET https://api.premion.com/api` | **401** `{"message":"Access Denied: No Token Provided"}` |
| `GET https://api.premion.com/openapi.json` `/swagger.json` `/api-docs` `/docs` `/redoc` | **404** each |
| GitHub orgs `tegna`, `TEGNA`, `premion`, `tegna-digital` | **404** — no public org exists |
| npm `tegna` / `premion` / `audienceone`, PyPI `tegna` / `premion` | **404** each |

`api.premion.com` **is** a real, live TEGNA host — but it is an unversioned Express service whose
only public surfaces are `/` and `/health`; its actual API lives under `/api`, is token-gated, and
publishes no specification. The quarantined Premion spec describes a `/v1` base path that returns
404 and operations that do not exist.

None of the quarantined specs carried an `x-provenance` or `x-generated-from` marker, so the
provenance grader would have read all nine as first-party. Their shape — tidy 1–2 operation CRUD
split across seven files, uniform `bearerAuth`, uniform `/v1` base — is the signature of the
network-wide scaffold sweep, matching the pattern documented for `plans/` and `rate-limits/`
(already remediated in this repo on 2026-08-11, see roadmap#35).

## What was quarantined, and why each is contaminated

| Path | Contamination |
|---|---|
| `openapi/` (7 refined + 2 `_original`) | Root cause — `servers[]` host is NXDOMAIN |
| `collections/` (9 Postman + 9 Open Collection) | Generated from the quarantined OpenAPIs |
| `examples/` | Response examples for operations that do not exist |
| `json-schema/`, `json-structure/`, `json-ld/` | Model the invented `Campaign` / `AudienceSegment` entities |
| `authentication/` | Derived from the invented `bearerAuth` / `X-API-Key` securitySchemes |
| `agentic-access/` | Classified 15 operations that do not exist |

## What TEGNA actually publishes

Replacements written in this same pass are **host-verified and live**:

- `openapi/tegna-content-api-openapi.yml` — derived from the live, public WordPress REST route
  index at `https://www.tegna.com/wp-json/` (405 routes, 200 OK, unauthenticated reads).
- `openapi/tegna-premion-content-api-openapi.yml` — same, from `https://premion.com/wp-json/`.
- `llms/tegna-llms.txt` — verbatim from `https://www.tegna.com/llms.txt` (200, `text/plain`).

TEGNA publishes **no** public developer program, no developer portal, no SDK, no MCP server and
no A2A agent card. AudienceOne and Premion are sold through insertion orders, programmatic deal
IDs and agency contracts — see `plans/tegna-plans-pricing.yml`.

## Do not restore

If a future pass wants to restore any of this, the bar is a **200 from a host TEGNA controls**
serving the document. Absence of a public advertising API is an honest, correct measurement of
this company; a plausible invented one is not.
