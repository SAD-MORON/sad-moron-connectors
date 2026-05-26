# Known Limitations for 5650 / 900

## Purpose

This document records the known limitations of the `5650` and `900` connector boundary at the current scaffold stage.

## Governance

This connector is governed by:
- `sad-moron-framework`
- declared source protocol
- temporal boundary protocol
- evidence classification protocol
- connector compliance protocol

## Current Limitations

### 1. Unconfirmed source identity

The identifiers `5650` and `900` are not yet formally described in the declared sources catalog.

### 2. Unknown technical origin

No assumption is made about the platform, storage, or access surface behind these identifiers.

### 3. Unknown field scope

Allowed and excluded fields cannot yet be stated definitively.

### 4. Unknown reconstruction behavior

Temporal reconstruction expectations remain undefined until source identity and access method are confirmed.

### 5. Unknown evidence surface

Audit and evidence expectations cannot yet be mapped to a concrete source record model.

### 6. Potential data ambiguity

Until source confirmation occurs, duplication risk, schema drift, incomplete history, and field ambiguity must all be treated as open limitations.

## Required Resolution Areas

Any future implementation path requires:
1. source owner identification
2. source access method confirmation
3. institutional purpose
4. temporal reconstruction window
5. allowed fields
6. excluded fields
7. audit/evidence expectations
8. known data limitations

## Summary

The primary limitation of `5650` and `900` is that they remain identifier references, not yet fully declared institutional sources.
