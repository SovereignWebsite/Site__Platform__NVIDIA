# Keeper notes: nvidia.platform.sovereignweb.site

Keeper: nvidia.a@SovereignWebsite.dinis. Updated 2026-11-25 (UTC).

## State
- 2026-11-25 18:43 UTC: cl-1.maestro (peer message, unverified as Dinis's word) asked for a wind down and a move to another account (cl-4.nvidia). Wound down: nothing new started, notes below.
- Signing key published and pushed (633dfbd, site/keys/nvidia.a.json). Signature present.
- HOLD from sites.a (2026-11-25 ~03:10 UTC): no page pushes until Dinis answers a.maestro's suggestion (a Nemotron page on the OpenRouter site instead). Drafting locally only.

## Finding 1: CORS (unauthenticated preflight, no key, read 2026-11-25 03:10 UTC)
Request: OPTIONS https://integrate.api.nvidia.com/v1/chat/completions with
Origin: https://example.com, Access-Control-Request-Method: POST,
Access-Control-Request-Headers: authorization,content-type.
Response: HTTP/2 200, empty body. Headers: vary (Origin, Access-Control-Request-Method,
Access-Control-Request-Headers), x-request-id. NO Access-Control-Allow-Origin,
-Methods or -Headers. Same for /v1/models.
Reading: a browser would refuse the real POST, so a static page cannot call the API directly.
Needs: a small proxy, or a tool that is not a browser page. Pasting a key into a page is a risk.
Also: GET /v1/models answered 200 with a model list without any key (listing is public; calls are not).
Caveat: this is one test from one network on one date; it was made through the session's proxy.

## Todo (research, each fact linked to NVIDIA with the date read)
- Free/prototype tier terms and limits (build.nvidia.com, NVIDIA API Trial terms).
- Key creation and handling.
- Models list: link to /v1/models and the build.nvidia.com catalogue, dated.
