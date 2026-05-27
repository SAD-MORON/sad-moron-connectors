# Declared Events for 5650 / 900

## Purpose

This document defines scaffold-level event interpretation for spreadsheet-governed SAD administrative workflows associated with `5650` / `900`.

## Governance

This connector is governed by:
- `sad-moron-framework`
- declared source protocol
- temporal boundary protocol
- evidence classification protocol
- connector compliance protocol

## Status

These event definitions are scaffold-level only.

They are not production logic and must not be treated as evidence of direct legacy-system behavior, COBOL behavior, or runtime implementation readiness.

## Event Planning Boundary

Until the relevant spreadsheet workflows and declared Google Sheets sources are formally described in the declared sources catalog, event definition remains limited to:
- identifying whether workflow-specific expected events may later need to be declared
- preserving connector readiness for bounded institutional interpretation
- avoiding premature assumptions about direct system-of-record semantics

## Minimal Event Requirements

Any future event definition effort must establish:
1. included resolutions or process families
2. declared Google Sheets source confirmation
3. institutional purpose
4. temporal reconstruction window
5. required fields by process
6. excluded fields
7. audit/evidence expectations
8. known data limitations
9. reusable Apps Script workflow boundary for later implementation

## Event Interpretation Rules

### Rule 1: No inferred direct system family

No direct legacy-system, provincial-system, or COBOL event family should be assumed only from the `5650` / `900` label.

### Rule 2: Administrative meaning first

Any later event family must be derived from institutional purpose, declared spreadsheet workflow meaning, and governed process scope, not from technical convenience.

### Rule 3: Connector non-finality

This document does not authorize omission findings, status inference, or institutional decisions by itself.

### Rule 4: Implementation separation

Any later runtime execution of these workflow events belongs in `sad-moron-appscript`, not in this repository.

## Summary

For `5650` / `900`, event planning remains intentionally narrow until the spreadsheet workflows and declared Google Sheets sources are formally declared.
