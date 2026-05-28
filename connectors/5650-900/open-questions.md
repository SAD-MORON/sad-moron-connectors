# Open Questions for 5650 / 900

## Purpose

This document records the open governance questions that must be answered before the `5650` / `900` spreadsheet workflow specification can support implementation planning.

## Governance

This connector is governed by:
- `sad-moron-framework`
- declared source protocol
- temporal boundary protocol
- evidence classification protocol
- connector compliance protocol

## Open Questions

1. Which SAD resolutions or administrative processes are included in this workflow family: Res. 5650, MAD, others?
2. Which Google Sheets, tabs, ranges, or spreadsheet families act as the declared sources for each included process?
3. Who is the institutional owner of each declared spreadsheet workflow surface?
4. What is the institutional purpose of each included process within SAD Moron workflows?
5. Which fields are required for governed use in each included process?
6. Which fields, comments, formatting conventions, or mixed-purpose content are excluded from governed use?
7. What temporal reconstruction window is realistic and governable for each included spreadsheet workflow?
8. Which Apps Script functions currently exist in the associated local-only
   implementation reference?
9. Which parts of the workflow are reusable across spreadsheet-based administrative processes?
10. What audit and evidence expectations can later be supported for these mutable spreadsheet records?
11. What data limitations are already known institutionally?
12. Which parts, if any, must be explicitly deferred before implementation handoff to `sad-moron-appscript`?

## Blocking Note

This connector cannot move to implementation until the relevant spreadsheet workflows and their declared Google Sheets sources are formally described in the declared sources catalog.

## Summary

These questions are not optional refinement items. They are the minimum unresolved governance conditions for this spreadsheet workflow connector boundary.
