# Case 001 — Telemetry encoding fix (CSV → panel)

## Context
Telemetry CSV was produced correctly, but ingestion/display was inconsistent due to encoding/format mismatch.

## Steps to reproduce
1) Generate telemetry CSV (monitoring tool).
2) Ingest into the panel pipeline.
3) Observe broken characters / missing fields / unstable parsing.

## Expected vs Actual
**Expected:** stable parsing and readable output.  
**Actual:** broken text/fields and inconsistent rendering.

## Fix / Patch
- Enforced a consistent encoding strategy for telemetry artifacts.
- Standardized formatting to match the panel parser expectations.
- Added an early check to detect mismatch before rendering.

## Verification steps
1) Run telemetry generation for 1–2 minutes.
2) Confirm panel updates in real time.
3) Confirm no broken characters and stable numeric values.
4) Confirm health/version checks report OK.

Создано Техник & ИИ-агента Curator-555-20260206_175932-r2 · current-24E2
