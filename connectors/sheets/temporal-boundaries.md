# Google Sheets Temporal Boundaries

## Purpose

This document defines the temporal boundaries that should govern Google Sheets source interpretation in the SAD Moron connector layer.

## Monthly Reconstruction Windows

Google Sheets review should assume bounded monthly reconstruction windows unless a more specific institutional period is declared for a given process.

Monthly reconstruction windows help:
- compare operational sheet state across bounded periods
- frame omission review against declared update expectations
- reduce ambiguity caused by constantly editable working sheets

## Update Cadence

Connector planning should assume that update cadence may vary by sheet and process.

The cadence should be declared where possible, for example:
- daily operational update expectation
- weekly coordination update expectation
- monthly consolidation expectation

Undefined cadence should be treated as a governance limitation, not silently assumed away.

## Snapshot Expectations

Because Sheets are mutable working sources, governance-aware connector planning should expect that later reconstruction may depend on bounded snapshots or equivalent declared review states.

The connector layer does not define snapshot implementation, but it recognizes snapshot expectation as a governance need for later audit compatibility.

## Historical Ambiguity Limits

Google Sheets sources may not preserve reliable full historical state by default.

Connector planning must account for historical ambiguity caused by:
- overwrites
- row reordering
- tab restructuring
- manual cleanup
- undocumented corrections

Historical interpretation should therefore remain bounded and cautious.

## No Timeless Omission Rule

No omission should be inferred from a Google Sheets source without a declared period or bounded reconstruction window.

Absence in a sheet is not enough by itself.

The review must still define:
- what was expected
- where it should have appeared
- during which bounded period

## Summary

Google Sheets temporal interpretation must remain windowed, cadence-aware, and resistant to timeless omission claims.
