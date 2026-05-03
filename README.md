# TEGNA (tegna)

TEGNA Inc. is an American broadcast, digital media, and marketing services company operating as a subsidiary of Nexstar Media Group. TEGNA operates 64 full-power broadcast television stations across 51 U.S. markets, reaching approximately 39 percent of all television households. TEGNA offers digital advertising solutions including AudienceOne first-party data targeting and OTT/CTV advertising through its Premion platform.

**URL:** [https://raw.githubusercontent.com/api-evangelist/tegna/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/tegna/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Fortune:** Fortune 500

## Tags:

 - Broadcasting, CTV, Digital Advertising, Media, OTT, Television

## Timestamps

- **Created:** 2026-03-24
- **Modified:** 2026-05-03

## APIs

### TEGNA AudienceOne API

First-party data targeting platform for digital advertising across TEGNA's 64 local TV brands in 51 markets.

**Human URL:** [https://www.tegna.com/advertise/solutions/digital/](https://www.tegna.com/advertise/solutions/digital/)

#### Tags:

 - Advertising, Audience Targeting, Digital Media, First-Party Data, Programmatic

#### Properties

- [Documentation](https://www.tegna.com/advertise/solutions/digital/)
- [OpenAPI](openapi/tegna-audience-one-openapi.yml)
- [JSONSchema](json-schema/tegna-campaign-schema.json)

### TEGNA Premion OTT Advertising API

OTT/CTV advertising platform for streaming video ads across Roku, Hulu, Amazon Fire TV, and other platforms.

**Human URL:** [https://premion.com/](https://premion.com/)

#### Tags:

 - CTV, Connected TV, OTT Advertising, Streaming, Video Advertising

#### Properties

- [Documentation](https://premion.com/)
- [OpenAPI](openapi/tegna-premion-openapi.yml)

## Artifacts

### OpenAPI Specifications

| File | Description |
|---|---|
| [tegna-audience-one-openapi.yml](openapi/tegna-audience-one-openapi.yml) | AudienceOne API - audiences, campaigns, performance reporting, markets |
| [tegna-premion-openapi.yml](openapi/tegna-premion-openapi.yml) | Premion OTT API - campaigns, inventory, creatives, performance |

### JSON Schemas

| File | Description |
|---|---|
| [tegna-campaign-schema.json](json-schema/tegna-campaign-schema.json) | Schema for TEGNA advertising campaign objects |

### JSON Structure

| File | Description |
|---|---|
| [tegna-campaign-structure.json](json-structure/tegna-campaign-structure.json) | Field-level documentation for campaign objects |

### JSON-LD Context

| File | Description |
|---|---|
| [tegna-context.jsonld](json-ld/tegna-context.jsonld) | Linked data context mapping TEGNA advertising terms to schema.org |

### Examples

| File | Description |
|---|---|
| [tegna-list-campaigns-example.json](examples/tegna-list-campaigns-example.json) | Example request/response for listing campaigns |
| [tegna-get-campaign-performance-example.json](examples/tegna-get-campaign-performance-example.json) | Example request/response for campaign performance |

### Spectral Rules

| File | Description |
|---|---|
| [tegna-rules.yml](rules/tegna-rules.yml) | Spectral ruleset for TEGNA API conventions |

### Naftiko Capabilities

| File | Description |
|---|---|
| [capabilities/media-advertising.yaml](capabilities/media-advertising.yaml) | Media advertising workflow - digital + OTT campaigns (8 MCP tools) |
| [capabilities/shared/audience-one.yaml](capabilities/shared/audience-one.yaml) | Shared AudienceOne API consumed definition |
| [capabilities/shared/premion-ott.yaml](capabilities/shared/premion-ott.yaml) | Shared Premion OTT API consumed definition |

### Vocabulary

| File | Description |
|---|---|
| [tegna-vocabulary.yml](vocabulary/tegna-vocabulary.yml) | Domain vocabulary for TEGNA media advertising |

## Common Properties

- [Website](https://www.tegna.com)
- [Nexstar Parent](https://www.nexstar.tv/)
- [Advertise With TEGNA](https://www.tegna.com/advertise/)
- [Digital Solutions](https://www.tegna.com/advertise/solutions/digital/)
- [Broadcast Solutions](https://www.tegna.com/advertise/solutions/broadcast/)
- [Premion OTT](https://premion.com/)
- [LinkedIn](https://www.linkedin.com/company/tegna)

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
