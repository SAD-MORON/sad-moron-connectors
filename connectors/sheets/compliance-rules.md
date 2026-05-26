# Google Sheets Compliance Rules

## Purpose

This document defines the compliance rules that any future Google Sheets connector implementation must inherit.

## Governance Inheritance

Any future Sheets connector must inherit governance from `sad-moron-framework`.

Connector logic may apply framework rules, but it may not redefine:
- governance meaning
- evidence classes
- declared-source scope
- omission review boundaries
- normative document authority

## Compliance Rules

### Rule 1: No credential persistence

A future connector must not store credentials inside repository content, connector definitions, or unmanaged local artifacts treated as part of the governed connector layer.

### Rule 2: No silent data mutation

A future connector must not silently mutate sheet data while presenting itself as a review or boundary-preserving connector.

### Rule 3: Append-only audit orientation

Connector behavior should support later append-only audit interpretation rather than conceal how sheet-derived evidence was bounded or observed.

### Rule 4: Governance inheritance from `sad-moron-framework`

All connector behavior must remain subordinate to framework governance and change-control discipline.

### Rule 5: No governance override by connector logic

No connector logic may reinterpret absence, evidence, or institutional decision authority in a way that overrides the framework.

## Exclusions

This document does not define:
- authentication methods
- API clients
- Apps Script behavior
- extraction mechanics
- synchronization workflows

## Summary

Future Sheets connectors must remain governance-inheriting, non-overriding, and compatible with append-only audit interpretation.
