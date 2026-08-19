---
name: track-tegna-press-releases
description: >-
  Pull TEGNA corporate press releases from the live WordPress REST API on www.tegna.com,
  filtered by date window or search term, with author and category resolved in a single
  request. Use for monitoring TEGNA announcements — earnings, leadership changes, station
  news, the Nexstar merger.
api: tegna:tegna-content-api
operations:
  - getWpV2Posts
  - getWpV2PostsById
  - getWpV2Categories
generated: '2026-08-13'
method: generated
source: openapi/tegna-content-api-openapi.yml
---

# Track TEGNA press releases

TEGNA's newsroom is served as JSON from a public WordPress REST API. No credential is required
for reads.

Base URL: `https://www.tegna.com/wp-json`

## 1. Pull the most recent releases

`getWpV2Posts` — `GET /wp/v2/posts`

```
GET https://www.tegna.com/wp-json/wp/v2/posts?per_page=20&orderby=date&order=desc&_embed=1
```

Use `_embed=1` so the author and category terms come back inline under `_embedded` instead of
costing one extra request per link. Use `_fields` to trim the payload — the default response
carries rendered HTML plus a large `aioseo_head` block you almost never want:

```
GET https://www.tegna.com/wp-json/wp/v2/posts?per_page=20&_fields=id,date,slug,link,title,excerpt
```

## 2. Page through the archive

There were **1,608** posts on 2026-08-13. Read the count from the response headers rather than
counting:

- `X-WP-Total` — total records matching the query
- `X-WP-TotalPages` — total pages at the current `per_page`
- `Link: <...page=2>; rel="next"`

`per_page` is capped at **100**. Asking for more is a **400** (`rest_invalid_param` wrapping
`rest_out_of_bounds`) — it is rejected, not clamped. Do not request a page beyond
`X-WP-TotalPages`.

## 3. Filter to a window or a topic

```
GET /wp/v2/posts?after=2026-01-01T00:00:00&before=2026-07-01T00:00:00&per_page=100
GET /wp/v2/posts?search=Nexstar&orderby=relevance
GET /wp/v2/posts?categories=<id>          # ids from getWpV2Categories
```

`modified_after` / `modified_before` filter on last-edit rather than publication — use those to
catch quietly revised releases.

## 4. Fetch one release in full

`getWpV2PostsById` — `GET /wp/v2/posts/{id}`

```
GET https://www.tegna.com/wp-json/wp/v2/posts/8972?_embed=1
```

`content.rendered` is HTML, not plain text. `title.rendered` and `excerpt.rendered` carry HTML
entities.

## Rules

- **Reads need no auth.** Anonymous callers only ever see `status=publish`; asking for another
  status returns 401, it does not silently filter.
- **Errors key on `code`, not `message`.** The envelope is
  `{"code": "...", "message": "...", "data": {"status": 4xx}}` — not RFC 9457. For a 400, read
  `data.details.<param>.code` for the precise cause.
- **There is no idempotency and no rate-limit signal.** No `X-RateLimit-*` or `Retry-After`
  header is returned. Cloudflare fronts the host, so back off on your own schedule; a
  10-minute edge cache (`cache-control: max-age=600`) means polling faster than that mostly
  returns cached bytes.
- **No stability guarantee.** TEGNA publishes no versioning or deprecation policy and returns
  no `Sunset` header. Re-read `https://www.tegna.com/wp-json/` if a route stops answering.
- **This is a content API.** It carries no advertising data — no campaigns, audiences,
  creatives or inventory. TEGNA publishes no advertising API.
