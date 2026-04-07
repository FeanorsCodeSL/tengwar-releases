# Tengwar Releases

Release manifests for the Tengwar update system. This repo contains only version metadata — no source code.

## Structure

```
backend/v{version}.json    — Backend release manifests
desktop/v{version}.json    — Desktop release manifests (future)
```

## Manifest Format

```json
{
  "version": "2026.4.3",
  "channel": "stable",
  "releaseNotes": "...",
  "releasedAt": "2026-04-07T00:00:00Z",
  "minClientVersion": "2026.2.0"
}
```
