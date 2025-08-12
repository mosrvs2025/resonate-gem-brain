# Resonate Gem Brain

A GitHub-first orchestration pattern for Google **Gems**. Attach this repo as a **Source** and instruct the Gem to:
> "Read `/MANIFEST.md` first. Route tasks to a single primary agent in `/agents/`. Consult guardrails and examples before answering. Output in Markdown."

## Why this exists
- Make Gems behave like an **agentic system** without extra code.
- Keep instructions composable, auditable, and versioned.
- Reuse across **Resonate**, **baibe.net**, **TrueShot AI**, client work, and personal ops.

## Quick start
1. Import this repository as a Source inside your Gem.
2. In the Gem's description, add: *Primary policy lives in `/MANIFEST.md`.*
3. Enable extensions you want the Gem to use (Docs/Drive/Sheets/YouTube/Maps).
4. Ask the Gem: *"Plan a 30-day launch content system for baibe.net. Use strategist → copy-smith → fact-checker pipeline."*

## Structure
See the full tree in `/MANIFEST.md`. Edit role files in `/agents/` as you learn.
