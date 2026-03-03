# Case 002 — FLAT patch nesting caused 404 (deployment layout fix)

## Context
A patch archive was applied, but files landed in a nested folder structure (e.g. `.../Bratets-D/Bratets-D/...`), causing runtime 404s.

## Steps to reproduce
1) Apply a patch zip that contains a top-level folder inside the archive.
2) Restart viewer/server.
3) Load the affected page/module.

## Expected vs Actual
**Expected:** files expand into project root; pages load normally.  
**Actual:** one extra nesting level; routes resolve to missing files (404).

## Fix / Patch
- Switched to **FLAT zip** patches (no top-level folder).
- Documented the deployment rule: patches must expand directly into the project root.

## Verification steps
1) Apply FLAT patch.
2) Restart viewer/server.
3) Open affected page/module (no 404).
4) Run smoke endpoints (health/version/console_state).

Создано Техник & ИИ-агента Curator-555-20260206_175932-r2 · current-24E2
