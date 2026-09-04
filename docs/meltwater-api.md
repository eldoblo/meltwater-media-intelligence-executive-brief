# Meltwater configuration notes

This repository does not publish or invent a universal Meltwater endpoint. Meltwater API products, access tiers, endpoint names, and response schemas may differ. A legitimate customer should use the endpoint and authentication method specified in their current Meltwater documentation or contract.

The optional HTTP Request node reads:

- `MELTWATER_API_BASE_URL` — the complete contract-specific endpoint;
- `MELTWATER_API_TOKEN` — a secret bearer token supplied at runtime;
- `MELTWATER_SAVED_SEARCH_ID` — the saved-search identifier.

Keep secrets out of JSON, Git, screenshots, and execution exports. Validate the response shape and permissions before switching from Demo Mode. The normalizer accepts a direct array or common `mentions`, `data`, and `results` wrappers, but it marks missing metrics unavailable.

Remote MCP is intentionally documentation-only for this MVP. Add it only after confirming compatibility with the installed n8n version and the official Meltwater MCP documentation.
