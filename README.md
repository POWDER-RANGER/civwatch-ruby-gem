# civwatch-ruby-gem

**Ruby integration/package scaffold for the CIVWATCH ecosystem.**

This repository is the future Ruby/Rails integration point for the unified CIVWATCH platform.

> **Current status:** packaging/integration scaffold.
> **Canonical platform:** [CivilianIntelligence](https://github.com/POWDER-RANGER/CivilianIntelligence).

## Role

The intended purpose is a Ruby-friendly client/library boundary for systems that consume CIVWATCH public-service APIs without coupling directly to internal implementation details.

The current repository is intentionally minimal and does not contain the unified application's runtime.

## Integration target

Stable service contracts should be preferred over internal database schemas.

| Service | Purpose |
|---|---|
| CivilianIntelligence | Unified application and public-data hub |
| Watchtower | Geospatial oversight APIs |
| Cell Titan | Defensive RF telemetry/evidence APIs |

See the [cross-repo integration contract](https://github.com/POWDER-RANGER/CivilianIntelligence/blob/main/docs/CROSS_REPO_INTEGRATION.md).

## Development status

The repository currently contains the package/release scaffold rather than a complete Ruby client implementation. Do not treat it as a production SDK yet.

Before publishing a client, implementation should cover:

- typed request/response contracts
- endpoint compatibility tests
- secure token handling
- timeout/retry behavior
- provenance preservation

## Security

Never embed server-side credentials in a client library or distribute bearer secrets to end users.

Remote service access should use HTTPS and each owning service's documented authentication boundary.

## Related repositories

- [CivilianIntelligence](https://github.com/POWDER-RANGER/CivilianIntelligence)
- [Watchtower](https://github.com/POWDER-RANGER/civwatch-watchtower)
- [Cell Titan](https://github.com/POWDER-RANGER/civwatch-cell-titan)
- [CIVWATCH App](https://github.com/POWDER-RANGER/civwatch-app)

## License

MIT
