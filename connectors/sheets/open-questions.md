# Google Sheets Open Questions

## Purpose

This document records the open governance questions that must be answered before any Google Sheets connector can support bounded implementation planning.

## Status

This document is governance-specification only.

It does not authorize extraction, runtime behavior, API work, or Apps Script work.

## Governance

This connector is governed by:
- `sad-moron-framework`
- declared source protocol
- temporal boundary protocol
- evidence classification protocol
- connector compliance protocol

## Open Questions

1. Which specific spreadsheet or spreadsheet family is the declared source of record?
2. What is the institutional owner of each governed sheet surface?
3. Which tabs, ranges, or worksheet segments are in scope, and which are excluded?
4. What is the institutional purpose of the governed Sheets source within SAD Moron workflows?
5. What temporal reconstruction window is realistic for each governed review path?
6. What cadence of updates is expected, and how much timing variance is acceptable?
7. Which fields or visible sheet structures are allowed for governed use?
8. Which fields, comments, formatting conventions, or mixed-purpose content are excluded from governed use?
9. What audit and evidence expectations can be supported for mutable spreadsheet records?
10. Which known limitations must remain explicit before any implementation handoff is considered?

## Blocking Note

No Google Sheets connector should move toward implementation unless these questions are resolved or explicitly deferred under governed change control.

## Summary

Google Sheets sources are useful but mutable, so unresolved scope, ownership, and temporal questions must remain visible at the connector layer.
