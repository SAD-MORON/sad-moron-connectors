# Pilot Context And Governance Primitives

## Purpose

This document explains the pilot context relevant to
`SAD-MORON-CONNECTORS` and defines the minimum governance primitives that give
meaning to this repository for future human readers and AI agents.

It exists to clarify why this repository is documentation-first, why connector
governance precedes operationalization, and which minimum concepts must remain
stable if later connector implementations inherit from this layer.

## Pilot Context

This repository should be read as a connector-governance and boundary layer
associated with pilot-era administrative workflow modernization in the SAD
Moron domain.

It is not itself a production connector repository.

It does not claim official endorsement beyond its documented repository scope.

It is intended to support continuity, auditability, interoperability, bounded
execution planning, and responsible repository separation.

## Why This Repository Exists

Connector contracts matter because operational connectors can silently widen
source scope, authority assumptions, or exposure risk if boundaries are not
declared before implementation expands.

Governance must precede connector operationalization because automation without
declared sources, declared boundaries, and declared authorization can produce
drift faster than it reduces ambiguity.

Public governance publication does not require publication of operational
connectors, privileged mappings, credentials, or live institutional
integrations.

Human institutional authority remains central because governance documents,
connector packs, and evidence reviews support decision-making but do not replace
accountable human authorization.

## Minimum Governance Primitives

### Boundary

A boundary is the declared limit of what a connector pack, source contract,
review, or repository governs.

### Declared Source

A declared source is an explicitly identified source that may support governed
connector interpretation within a defined scope.

### Authorization

Authorization is the accountable approval required before a declared connector
boundary can be operationalized against a real source.

### Expected Event

An expected event is an institutional action, obligation, or trace that should
exist under a defined connector scope and temporal window.

### Temporal Window

A temporal window is the defined period within which an expected event, review,
or evidence claim is evaluated.

### Evidence

Evidence is the recorded basis for supporting or constraining a governance
interpretation within a declared source, scope, and period.

### Omission

An omission is the bounded absence of an expected event or record under
declared source scope, expected-event scope, and temporal window.

### Drift

Drift is unintended change in connector meaning, workflow interpretation, source
assumptions, or execution scope without explicit review and approval.

### Public/Private Operational Boundary

The public/private operational boundary distinguishes what may remain public as
governance, templates, and documentation from what may remain external, private,
or separately governed for operational or security reasons.

### PASS / REVIEW / BLOCKED

`PASS` means the declared governance minimum is satisfied for the relevant
phase.

`REVIEW` means the repository or connector claim is usable only with unresolved
governance questions made explicit.

`BLOCKED` means progression should not continue until the blocking governance
issue is resolved.

## Janus Core Relation

`SAD-MORON-CONNECTORS` inherits governance principles from Janus Core through
the SAD Framework.

It does not depend on the full Janus runtime ecosystem.

It selectively applies governance principles derived from Janus Core to the
connector-contract layer through repository separation, bounded execution,
auditability, exposure control, and human authority preservation.

## Guidance For AI Agents

AI agents reading this repository should observe the following rules:
- do not infer runtime permissions from governance docs
- do not treat connector contracts as production connectors
- do not invent source access
- do not expose IDs, endpoints, credentials, or institutional mappings
- do not create operational connectors without declared source, boundary,
  and authorization
- do not treat old reports as current governance authority
- current authority lives in `docs/`, `contracts/`, connector pack docs, and
  framework references
- when uncertain, classify `REVIEW` or `BLOCKED`

## Institutional Neutrality

This repository should be read as an institutional governance artifact with
pilot context, not as a political statement, personal brand, or claim of
official state endorsement.

Its intended value is continuity, bounded modernization, and reconstructable
connector governance meaning.

## Summary

This repository is a pilot-context connector governance layer that preserves
minimum governance primitives so future readers, repositories, and AI agents can
interpret connector boundaries safely without assuming operational authority.
