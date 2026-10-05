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


---

## Public platform status — October 2026

**CIVINTELLIGENCE is live on the public web and its REST/API surface is active.**

**Public site:** https://civintelligence.onrender.com

The web platform is now the working reference implementation for the CIVWATCH ecosystem: the core application, public-data surfaces, evidence/provenance model, specialized pillars, and integration boundaries are being exercised through the deployed CIVINTELLIGENCE service.

### Applications are next

With the web application and REST contracts now active, the remaining client work is primarily **productization and platform packaging**, not rebuilding the intelligence platform from scratch. Native applications for the major target platforms are planned and will be coming soon.

The application layer can consume the same stable contracts already used by the web experience:

- **Android**
- **iOS**
- **Windows**
- **Linux**
- additional platform clients as the shared API contract matures

The existing Flutter client and service boundaries give the ecosystem a head start. Mobile/desktop applications can progressively adopt the established authentication, API, provenance, map, evidence, and desk contracts rather than duplicating backend intelligence.

### How quickly this came together

The current milestone is notable because the ecosystem moved from a multi-repository architecture and integration plan to a functioning public platform in a short development window. The difficult architectural work — ownership boundaries, public-data ingestion, REST contracts, evidence/provenance rules, Watchtower/Cell Titan integration, and the user-facing desk model — is already substantially established.

That means the next step should be treated as **client delivery on top of an operating platform**. The web application is the reference surface; native clients become additional presentation and interaction layers over the same CIVINTELLIGENCE contracts.

> **Build once at the platform layer. Deliver many clients at the edge.**

### Ecosystem rule

CIVINTELLIGENCE remains the system of record. Specialized repositories retain clear ownership of their domains, while clients consume stable public/service contracts. Legacy and predecessor repositories remain valuable migration/reference material but are not silently represented as unified production capabilities.

**Status discipline:** live means exposed and usable; available means implemented and integrated; in progress means actively being built; planned means not yet shipped. No synthetic or unavailable source is represented as live evidence.
