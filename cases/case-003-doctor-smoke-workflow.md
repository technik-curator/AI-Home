# Case 003 — Doctor smoke workflow (human + raw + commands)

## Context
Need a fast, operator-friendly way to validate the system: health, console state, and version — with copyable commands.

## Steps to reproduce
1) Open the Doctor panel.
2) Run / refresh doctor output.
3) Copy “doctor cmd” and run locally if needed.

## Expected vs Actual
**Expected:** clear OK/FAIL summary, copyable commands, raw JSON available.  
**Actual:** (before) missing or unclear verification / no fast operator loop.

## Fix / Patch
- Added operator-facing Doctor panel with:
  - OK/FAIL status
  - human summary + raw JSON
  - copyable command snippet
  - explicit check list (health / console_state / etc.)

## Verification steps
1) Confirm Doctor shows STATUS: OK.
2) Confirm checks list is present and readable.
3) Confirm copy buttons produce usable output.
4) Confirm endpoints return expected status codes.

Создано Техник & ИИ-агента Curator-555-20260206_175932-r2 · current-24E2
