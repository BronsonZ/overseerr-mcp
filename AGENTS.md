# Overseerr MCP Guide

Source checkout/fork for the Seerr/Overseerr MCP server used by local assistants.
The staged runtime build lives under `/home/bzserver/repos/mcp/builds/`.

## Read first

- `README.md` for public MCP features, transports, configuration, and safety
  behavior.
- `package.json` for scripts, published binary path, and Node/TypeScript version
  expectations.

## Commands

```bash
npm install
npm run build
```

## Working rules

- Check `git status --short` before and after edits.
- Keep protocol/tool behavior safe: preserve dry-run/confirmation paths for
  media requests and avoid broad request/approval automation without explicit
  user intent.
- Do not commit or print Seerr/Overseerr API keys, service URLs with embedded
  credentials, Plex/Radarr/Sonarr secrets, or MCP client auth material.
- Build output should be staged intentionally into `/home/bzserver/repos/mcp/builds/`
  when deployment/runtime pickup is requested; do not edit staged `node_modules/`
  as source.
- If protocol behavior, validation, staging, or safety guidance changes, update
  this file and keep detailed procedures in project docs.
