# Source Declaration Model

## Purpose

This document explains how source declarations should be interpreted at the connector layer.

## Model

A connector may exist only for a source that is already declared or intended to be declared under the SAD Moron governance framework.

Each connector-facing source model should preserve:
- source name
- institutional origin
- document or record class
- intended governance use
- temporal relevance
- known limitations
- boundary note

## Connector Use Rule

A connector must not create a broader source boundary than the declared source model allows.

## Exclusions

This model does not define:
- extraction logic
- API fields
- scraping selectors
- data transport formats

## Summary

The connector layer consumes declared source meaning; it does not invent source authority.
