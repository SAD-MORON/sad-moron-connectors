# Implementation Handoff Protocol

## Purpose

This document defines how connector-layer governance artifacts in `SAD-MORON-CONNECTORS` may hand off to a separate governed implementation repository.

## Implementation Repository

The implementation repository for Apps Script-based bounded execution is `sad-moron-appscript`.

`sad-moron-appscript` is a separate governed implementation repository.

It is not part of the connector layer and must not be treated as implied by connector documentation alone.

## Connector Layer Boundary

Connectors in this repository do not execute.

This repository defines governance, source boundaries, temporal expectations, and compliance constraints only.

No connector may move to implementation by implication, naming convention, folder completeness, or technical convenience.

## Required Handoff Conditions

Implementation handoff from this repository requires:
1. declared source status
2. connector source contract
3. temporal boundary
4. open questions resolved or explicitly deferred
5. framework compliance check
6. no credential leakage
7. change-control discipline

## Handoff Interpretation Rules

### Rule 1: Declared source first

No implementation handoff is valid unless the target source is already declared or explicitly governed as intended for declaration under the SAD Moron framework.

### Rule 2: Connector contract completeness

The connector-facing source contract and connector boundary documents must exist in a form sufficient to preserve institutional meaning and bounded use.

### Rule 3: Temporal boundedness required

Implementation handoff requires a declared temporal boundary suitable for later reconstruction and audit interpretation.

### Rule 4: Open questions cannot disappear silently

Any unresolved governance questions must either be resolved before handoff or be explicitly deferred with bounded justification and no hidden assumption transfer.

### Rule 5: Framework compliance must be checked

The handoff must confirm that the target implementation remains subordinate to `sad-moron-framework`, including declared-source discipline, evidence handling, repository separation, and change control.

### Rule 6: No credential leakage

Connector-layer artifacts must not carry credentials, secrets, or unmanaged access material into implementation planning or repository transfer.

### Rule 7: No implied execution authority

Connector completeness, planning detail, or event specificity does not authorize runtime execution. Execution authority must be established separately inside the governed implementation repository.

## Summary

Implementation for SAD Moron connectors must hand off explicitly to `sad-moron-appscript` or another separately governed implementation repository, never by implication from connector-layer documentation.
