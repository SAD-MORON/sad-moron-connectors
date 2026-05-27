# SAD-MORON-CONNECTORS

## Purpose

`SAD-MORON-CONNECTORS` is a documentation-first connector repository for SAD Moron.

It is governed by `sad-moron-framework`:
- Governance source: https://github.com/SAD-MORON/sad-moron-framework
- Remote target for this repo: https://github.com/SAD-MORON/sad-moron-connectors

This repository defines connector boundaries, source contracts, and connector compliance rules before any implementation exists.

## Governance Status

This repository is governed by `sad-moron-framework`.

Connector-layer documents may apply governance, but they cannot redefine governance, evidence semantics, normative scope, repository separation, or omission review meaning.

## Connector Conditions

Every connector requires:
- a declared source
- a temporal boundary
- an institutional use justification

Every connector must remain bounded by:
- declared source scope
- expected event relevance when applicable
- institutional purpose
- framework-defined governance rules

## Prohibitions

This repository does not allow:
- unrestricted scraping
- credential storage
- data extraction beyond declared boundary
- production execution
- runtime services
- API implementation
- Apps Script implementation

## Repository Structure

```text
.
├── README.md
├── docs/
├── contracts/
├── connectors/
└── reports/
```

## Layer Role

This repository is not a runtime repository. Runtime execution belongs in a separate governed implementation repository.

Its role is to define the connector layer as a governed boundary between declared institutional sources and any future lower-layer implementation.
