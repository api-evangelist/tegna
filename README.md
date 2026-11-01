# TEGNA

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

TEGNA Inc. is an American broadcast, digital media, and marketing services company headquartered in Tysons, Virginia, operating as a subsidiary of Nexstar Media Group following FCC approval of the $6.2 billion acquisition in March 2026. TEGNA operates 64 full-power broadcast television stations across 51 U.S. markets, reaching approximately 39 percent of all television households. Its digital marketing portfolio includes AudienceOne first-party data targeting, OTT/CTV advertising through the Premion platform, and the TEGNA Marketing Solutions full-service agency. TEGNA runs no public developer program and publishes no developer portal: those advertising products are transacted through insertion orders, programmatic deal IDs and agency contracts. The only publicly callable, machine-readable API surfaces TEGNA serves are the WordPress REST content APIs behind its corporate site and premion.com; the Premion advertising platform API at api.premion.com is live but token-gated and undocumented.

**Areas:** Broadcasting · Media · Television · Digital Advertising · OTT · CTV · Local News · content-api · Fortune 500

## TEGNA on APIs.io

Everything profiled for TEGNA is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/tegna/](https://apis.io/providers/tegna/)** — or go straight to one of the APIs or properties below.

### APIs (3)

- [Premion Advertising Platform API (gated)](https://apis.io/apis/tegna/tegna-premion-platform-api/) — A live but undocumented and token-gated API behind Premion's OTT/CTV advertising platform. Probed 2026-08-13: the host root returns 200 {"message":"App is…
- [TEGNA Website (WordPress REST)](https://apis.io/apis/tegna/tegna-com-website-wordpress-rest/) — The public WordPress REST API (wp-json) of the TEGNA website at www.tegna.com: the route index of the site's content management system, catalogued as one…
- [TEGNA Website (WordPress REST)](https://apis.io/apis/tegna/premion-com-website-wordpress-rest/) — The public WordPress REST API (wp-json) of the TEGNA website at premion.com: the route index of the site's content management system, catalogued as one site…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [tegna-mcp.yml](https://apis.io/servers/tegna/tegna-mcp-yml/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Tegna Agentic Access](https://apis.io/agentic-access/tegna/tegna-agentic-access/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Tegna Vocabulary](https://apis.io/vocabularies/tegna/tegna-vocabulary/)

#### Collections (2)

Postman and Open Collection request collections.

- [Moved to /providers/tegna/](https://apis.io/collections/tegna/open-tegna-content-api/)
- [PREMION Content API (WordPress REST)](https://apis.io/collections/tegna/open-tegna-premion-content-api/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [TEGNA — jsonschema rules](https://apis.io/rules/tegna/tegna-jsonschema-spectral-rules/)
- [TEGNA API Rules](https://apis.io/rules/tegna/tegna-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Tegna Authentication](https://apis.io/security/tegna/tegna-authentication/)
- [Tegna Domain Security](https://apis.io/security/tegna/tegna-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Tegna Plans Pricing](https://apis.io/plans/tegna/tegna-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Tegna Rate Limits](https://apis.io/rate-limits/tegna/tegna-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Tegna Finops](https://apis.io/finops/tegna/tegna-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.tegna.com)
- [Documentation](https://www.tegna.com/advertise/solutions/digital/)
- [Support](https://www.tegna.com/contact/)
- [Blog](https://www.tegna.com/press/)
- [Terms of service](https://www.tegna.com/terms-of-service/)
- [Privacy policy](https://www.tegna.com/privacy-policy/)

## API Evangelist rating

**Kin Score 26.0** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 69.6 |
| Contract quality | 1.7 |
| Contract governance | 31.8 |
| Operational transparency | 21.1 |
| Developer ergonomics | 30.4 |
| Access clarity | 26.3 |

**Agent readiness 10.6** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 24.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/tegna/](https://apis.io/providers/tegna/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for TEGNA: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/tegna/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
