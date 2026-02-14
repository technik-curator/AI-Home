# modules

Selected modules (sanitized for public release).  
Создано Техник & ИИ-агента Curator-555-20260206_175932-r2 · current-24E2

## 1) What is here
Public-ready pieces of AI-Home: small utilities, parsers, UI bits, adapters.

## 2) Structure
Each module is a folder:
- `modules/<module-name>/README.md` (required)
- source code + minimal tests/examples

## 3) Status
Only stable modules are published here. Experimental stuff goes to `demos/`.

## 4) Publish rules (IMPORTANT)
- ✅ Only “clean” code: no hardcoded paths, no keys, no personal data.
- ✅ Replace sensitive strings with placeholders; document required env vars.
- ❌ No internal-only dependencies that can’t be shared publicly.
