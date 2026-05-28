# SAD-MORON-CONNECTORS

## Purpose

`SAD-MORON-CONNECTORS` is a governance-first, documentation-first repository for
the SAD connector-contract layer.

It inherits governance principles from Janus Core and implements the
SAD Framework connector-contract layer through connector contracts, source
boundaries, governance packs, and compliance rules.

This repository is governed by `sad-moron-framework`:
- Governance source: https://github.com/SAD-MORON/sad-moron-framework
- Canonical repository standard: `../SAD-MORON-FRAMEWORK/docs/repository-governance-standard.md`

This repository does not depend on the full Janus runtime ecosystem.

## Governance Posture

This repository exists to define connector contracts, source boundaries, and
connector compliance packs before operational implementation exists.

Connector-layer documents may apply governance, but they cannot redefine
governance, evidence semantics, normative scope, repository separation,
or omission review meaning inherited through the SAD Framework.

Current governance authority lives in:
- `docs/`
- `contracts/`
- connector pack governance documents under `connectors/`
- relevant framework governance references

`reports/` is evidence and history, not the default source of current
governance authority.

## Connector Conditions

Every connector requires:
- a declared source
- a temporal boundary
- an institutional use justification
- a declared boundary suitable for audit reconstruction

Every connector must remain bounded by:
- declared source scope
- expected event relevance when applicable
- institutional purpose
- framework-defined governance rules
- explicit human review and authorization where operationalization is proposed

## Public / Private Boundary

This repository preserves a hybrid posture.

Public governance/documentation surfaces may include:
- connector contracts
- source-boundary templates
- synthetic examples
- governance packs
- compliance rules

Private or external operational surfaces may include:
- real operational connectors
- API credentials
- production endpoints
- institutional mappings
- deployment configs
- sensitive source adapters

This repository does not publish production connectors.

Real operational connectors and sensitive integrations may remain external or
private where boundary, security, or institutional constraints require it.

## Security And Exposure Posture

This repository does not allow:
- unrestricted scraping
- credential storage
- data extraction beyond declared boundary
- production execution
- runtime services
- API implementation
- Apps Script implementation
- committed Sheet IDs
- committed Script IDs
- committed live endpoints

No credentials, Google Sheet IDs, Apps Script IDs, or production endpoints
should be committed to Git in this repository.

## Licensing

Apache License 2.0 applies to the governance, documentation, contract, and
scaffold layers in this repository.

- License: [LICENSE](LICENSE)
- Notice: [NOTICE](NOTICE)

Copyright 2026 Martín Nicolás Sánchez Morales

## Guidance

- AI agent guidance: [docs/AI_AGENT_GUIDE.md](docs/AI_AGENT_GUIDE.md)
- Pilot context and governance primitives:
  [docs/pilot-context-and-governance-primitives.md](docs/pilot-context-and-governance-primitives.md)
- Connector public/private boundary:
  [docs/connector-public-private-boundary.md](docs/connector-public-private-boundary.md)

## Repository Structure

```text
.
├── README.md
├── LICENSE
├── NOTICE
├── docs/
├── contracts/
├── connectors/
└── reports/
```

## Layer Role

This repository is a pre-implementation connector governance layer.
Runtime execution belongs only in a separate governed implementation repository.

Its role is to define the bounded connector layer between declared institutional
sources and any future separately governed lower-layer implementation.
