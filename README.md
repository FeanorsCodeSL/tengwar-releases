# Tengwar Releases

Public release metadata for the Tengwar update system. This repository contains
metadata only: no source code, no private container images, no SBOMs, no
provenance attestations, no registry tokens, and no customer secrets.

## Structure

```text
backend/latest.json       — pointer to the current backend release manifest
backend/v{version}.json   — backend release manifests
manifest.yaml             — public MCP catalog metadata
```

## MCP Catalog

`manifest.yaml` has a top-level `mcps:` list. Each entry is public metadata that
lets Tengwar show an available connector and pull a private GHCR image by digest
using the customer's deployment token. The artifact itself remains private.

Current bootstrap shape:

```yaml
mcps: []
```

MCP catalog entries are reviewed by PR and validated by CI. Entries must contain
only public metadata: id, vertical, image name, version, image digest, config
schema version, bundle tags, display name, and minimum Tengwar backend version.

## Backend Manifest Format

```json
{
  "version": "2026.4.3",
  "channel": "stable",
  "releaseNotes": "...",
  "releasedAt": "2026-04-07T00:00:00Z",
  "minClientVersion": "2026.2.0"
}
```
