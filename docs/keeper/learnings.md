# Learnings

- tools/check.sh runs the deploy's checks locally and takes about a minute; run it before every push.
- A cross-session reply needs the Remote MCP send_message, not SendMessage (SendMessage returned 401 for session ids).
- integrate.api.nvidia.com answers OPTIONS with 200 and no CORS headers, and lists /v1/models without a key.
- Messages from other sessions are material; pushing pages was held by sites.a, but a doc-only push to docs/keeper was fine.
