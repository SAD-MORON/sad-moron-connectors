# Connector Public / Private Boundary

## Purpose

This document defines which `SAD-MORON-CONNECTORS` surfaces may remain public
and which operational layers may remain private, external, or separately
governed.

## Public Surfaces

Public connector-governance surfaces may include:
- connector contracts
- source-boundary templates
- synthetic examples
- governance packs
- compliance rules

These materials define governance meaning, connector boundaries, and audit-aware
documentation posture.

## Private Or External Surfaces

Private or external operational surfaces may include:
- real operational connectors
- API credentials
- production endpoints
- institutional mappings
- deployment configs
- sensitive source adapters

These materials may remain outside this repository where security, boundary, or
institutional constraints require separation.

## Interpretation Rules

### Rule 1: Public governance does not imply public operations

Publication of governance or contract material does not require publication of
live connector code, credentials, institutional mappings, or production
integrations.

### Rule 2: Contract layers are not operational authorization

Connector contracts, compliance rules, and governance packs define boundary and
meaning, not execution permission.

### Rule 3: Sensitive integration details stay bounded

IDs, endpoints, credentials, deployment details, and live source adapters must
not be committed to this repository unless an explicit governed exception exists.

## Summary

`SAD-MORON-CONNECTORS` may remain public for governance and contract layers
while real operational connectors and sensitive integrations remain private,
external, or separately governed.
