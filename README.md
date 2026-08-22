# TEGNA (tegna)

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

TEGNA Inc. is an American broadcast, digital media, and marketing services company headquartered in Tysons, Virginia, operating as a subsidiary of Nexstar Media Group following FCC approval of the $6.2 billion acquisition in March 2026. TEGNA operates 64 full-power broadcast television stations across 51 U.S. markets, reaching approximately 39 percent of all television households. Its digital marketing portfolio includes AudienceOne first-party data targeting, OTT/CTV advertising through the Premion platform, and the TEGNA Marketing Solutions full-service agency.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/tegna/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/tegna/refs/heads/main/apis.yml)

## What TEGNA actually publishes

**TEGNA runs no public developer program.** There is no developer portal, no API documentation, no SDK, no public GitHub organization, no MCP server and no A2A agent card. `developer.tegna.com`, `docs.tegna.com` and `developers.tegna.com` do not resolve. AudienceOne and Premion are transacted through insertion orders, programmatic deal IDs and agency contracts — see [`plans/tegna-plans-pricing.yml`](plans/tegna-plans-pricing.yml).

What TEGNA *does* serve, verified live on 2026-08-13, is a pair of public WordPress REST content APIs and one token-gated advertising backend.

## Scope

- **Type:** Index

## Tags

- Broadcasting
- Media
- Television
- Digital Advertising
- OTT
- CTV
- Local News
- Content API
- Fortune 500

## Timestamps

- **Created:** 2026-03-24
- **Modified:** 2026-08-13

## APIs

### TEGNA Content API (WordPress REST)

The public, unauthenticated read API behind www.tegna.com — TEGNA's corporate and press site. 264 routes across 366 operations serving posts, pages, media, categories, tags, taxonomies, block types, site-health and the WordPress Abilities namespace as JSON, plus oEmbed and AIOSEO metadata. Reads on public content require no credential; writes require a WordPress Application Password.

- **Human URL:** [https://www.tegna.com/](https://www.tegna.com/)
- **Base URL:** `https://www.tegna.com/wp-json`

#### Properties

- [OpenAPI](openapi/tegna-content-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html) *(derived by API Evangelist from the provider-served route index; TEGNA publishes no OpenAPI)*
- [Documentation](https://developer.wordpress.org/rest-api/)
- [Authentication](authentication/tegna-authentication.yml)
- [Conventions](conventions/tegna-conventions.yml)
- [ErrorCatalog](errors/tegna-problem-types.yml)
- [DataModel](data-model/tegna-data-model.yml)

### PREMION Content API (WordPress REST)

The public, unauthenticated read API behind premion.com, the marketing site for Premion — TEGNA's OTT/CTV advertising business. 186 routes across 291 operations. This is a content API, not the Premion advertising platform API.

- **Human URL:** [https://premion.com/](https://premion.com/)
- **Base URL:** `https://premion.com/wp-json`

#### Properties

- [OpenAPI](openapi/tegna-premion-content-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html) *(derived, as above)*
- [Documentation](https://developer.wordpress.org/rest-api/)
- [Authentication](authentication/tegna-authentication.yml)
- [Conventions](conventions/tegna-conventions.yml)

### Premion Advertising Platform API (gated)

A live but undocumented and token-gated API behind Premion's OTT/CTV advertising platform. Probed 2026-08-13: the host root returns `200 {"message":"App is running"}`, `/health` returns 200, and every path under `/api` returns `401 {"message":"Access Denied: No Token Provided"}`. No OpenAPI, Swagger, GraphQL, docs or discovery document is served at any probed location. Recorded because the surface demonstrably exists; no specification is claimed.

- **Human URL:** [https://premion.com/](https://premion.com/)
- **Base URL:** `https://api.premion.com/api`

## Not published by TEGNA

Recorded absences. Each was probed, and each empty result is a measurement rather than a gap in the search.

| Surface | Result |
|---|---|
| Developer portal / API docs | None. `developer.tegna.com`, `docs.tegna.com`, `developers.tegna.com` all NXDOMAIN |
| OpenAPI / Swagger / GraphQL | None served. `api.premion.com/openapi.json`, `/swagger.json`, `/api-docs`, `/docs`, `/redoc` all 404 |
| `/.well-known/*` | 36 probes across 4 hosts, 36 × 404. No `WellKnown` or `SecurityTxt` pointer emitted |
| A2A agent card | `agent-card.json` and `agent.json` 404 on every host. No `a2a/` artifact written |
| MCP server | None hosted, none packaged. `mcp/tegna-mcp.yml` records `deployment.mode: none` and wires **no** `MCPServer` pointer |
| SDKs / packages | Zero across npm, PyPI, RubyGems, crates.io, NuGet, Maven, pkg.go.dev. No public GitHub org |
| Status page | None. `tegna.statuspage.io` returns 200 but so does a random control subdomain — a wildcard soft-200, not a status page |
| Rate limits | No `X-RateLimit-*`, `RateLimit-*` or `Retry-After` header on any response |
| Idempotency | Not supported; no idempotency key accepted |
| Compliance / trust center | No SOC 2 / ISO 27001 / PCI / HIPAA / FedRAMP claim. `trust.tegna.com` NXDOMAIN |
| Events / webhooks / AsyncAPI | No event surface. Not applicable rather than failed |

## Quarantined artifacts

Nine OpenAPI documents and everything derived from them were moved to [`_scaffold/`](_scaffold/README.md) in the 2026-08-13 pass. They declare `api.tegna.com`, which is **NXDOMAIN**, and a Premion `/v1` base path that returns 404. They were written by API Evangelist, not by TEGNA, and carried no provenance marker. See [`_scaffold/README.md`](_scaffold/README.md) for the full evidence table.

## Common Properties

- [Website](https://www.tegna.com)
- [Website](https://www.nexstar.tv/)
- [Advertising](https://www.tegna.com/advertise/)
- [Documentation](https://www.tegna.com/advertise/solutions/digital/)
- [Documentation](https://www.tegna.com/advertise/solutions/broadcast/)
- [Documentation](https://www.tegna.com/advertise/solutions/streaming/)
- [Website](https://premion.com/)
- [Support](https://www.tegna.com/contact/)
- [HelpCenter](https://tegnadigital.atlassian.net/servicedesk/customer/portal/17)
- [TermsOfService](https://www.tegna.com/terms-of-service/)
- [PrivacyPolicy](https://www.tegna.com/privacy-policy/)
- [LinkedIn](https://www.linkedin.com/company/tegna)
- [Blog](https://www.tegna.com/press/)
- [LLMsTxt](llms/tegna-llms.txt) — verbatim from `https://www.tegna.com/llms.txt` (200, `text/plain`)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
