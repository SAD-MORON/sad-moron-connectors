# Google Sheets Connector

## Purpose

This folder defines the governance-scaffold documentation for a future Google Sheets institutional connector.

## Status

This connector is governance-scaffold only.

No extraction, runtime, API, or Apps Script implementation exists here yet.

## Governance Dependency

Future implementations in this area must comply with `sad-moron-framework`.

This means future connector work must inherit:
- declared-source discipline
- temporal boundaries
- evidence classification rules
- omission review boundaries
- repository separation rules

## Folder Role

This folder defines institutional connector contracts only.

It exists to specify:
- source scope
- scaffold-level event families
- temporal boundaries
- connector compliance rules
- known source limitations

## Prohibitions

This folder does not authorize:
- extraction code
- runtime execution
- credential storage
- unrestricted ingestion
- governance override by connector logic

## Summary

This folder prepares the Sheets connector boundary before any implementation exists.
