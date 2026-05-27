# Connector 5650 / 900

## Purpose

This folder defines the governance-only connector specification pack for spreadsheet-governed SAD administrative workflows associated with `5650` / `900`.

## Status

This connector is documentation only.

`5650` / `900` is treated here as an administrative workflow specification boundary for spreadsheet-based SAD procedures such as Res. 5650, MAD, and related governed process families.

This pack is associated with Google Sheets as the likely declared source surface and with future bounded implementation in `sad-moron-appscript`.

This pack is not a COBOL source connector.

This pack is not a direct connector for a legacy or provincial system of record.

## Governance

This connector is governed by:
- `sad-moron-framework`
- declared source protocol
- temporal boundary protocol
- evidence classification protocol
- connector compliance protocol

## Connector Preconditions

This connector requires:
1. process family identification
2. declared Google Sheets source confirmation
3. institutional purpose
4. temporal reconstruction window
5. required fields by process
6. excluded fields
7. audit/evidence expectations
8. known data limitations
9. Apps Script reuse boundary for later implementation

## Implementation Block

This connector cannot move to implementation until the relevant spreadsheet workflows and their declared Google Sheets sources are formally described in the declared sources catalog.

Any later runtime execution belongs in `sad-moron-appscript`, not in this repository.

## Prohibitions

This folder does not authorize:
- extraction
- runtime code
- API code
- Apps Script code
- credential storage
- scraping
- source inference by convenience
- classification as COBOL or legacy/provincial system integration by assumption

## Summary

This folder establishes a governed spreadsheet-workflow boundary for SAD administrative processes associated with `5650` / `900` before any implementation exists.
