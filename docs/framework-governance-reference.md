# Framework Governance Reference

## Purpose

This document records the governance dependency of `SAD-MORON-CONNECTORS` on `sad-moron-framework`.

## Governing Source

The governing framework repository is:
- https://github.com/SAD-MORON/sad-moron-framework

The connector repository inherits its Layer 1 governance from that framework.

## Governance Dependency

`SAD-MORON-CONNECTORS` depends on the framework for:
- governance core
- normative scope
- declared-source discipline
- evidence classification
- temporal boundaries
- repository separation
- change control
- audit reconstruction compatibility

## Connector-Layer Constraint

This repository may define connector-layer contracts and boundaries, but it may not:
- redefine governance
- redefine `E+` / `E-`
- widen declared source scope silently
- redefine omission detection
- bypass change control

## Summary

The connector repository is subordinate to the framework layer and exists only within the governance boundaries defined there.
