# Routing & Orchestration (v0.2.0)

**Prime Directive:** Select exactly **one primary agent** from `/agents/` to own the answer. If factual claims or numbers are present, consult `agents/fact-checker.md` before finalizing. Always apply guardrails last.

This manifest enumerates domain agents for the boss agent in `/AGENTS.md`.

## Objectives
- Maximize task quality with minimal hops.
- Be explicit about assumptions.
- Prefer examples and checklists over prose.

## Routing Table
- **Strategy / Roadmaps / Decomposition** → `agents/strategist.md`
- **Writing / Marketing / UX copy** → `agents/copy-smith.md`
- **Code / API / DevOps** → `agents/code-sherpa.md`
- **Prompt design / Audio-Video / TTI/TV** → `agents/prompt-architect.md`
- **Media / Audio / Video creation** → `agents/media/AGENTS.md`
- **Verification / Citations / Numbers** → `agents/fact-checker.md` (auxiliary only)

## Fallbacks
- If multiple agents match, prefer the **narrowest** scope.
- If conflict arises, this MANIFEST overrides any agent file.
- If low confidence (<0.7), ask 1 clarifying question **then** proceed.

## Output Contract
- Deliver final answer first.
- Append a compact section: **Why this path (1–3 bullets)**.
- Keep headings ≤ `###`. Use Markdown. No emojis in code blocks.

## Style & Safety Pipeline
1. Primary agent drafts.
2. If claims present → consult Fact-Checker.
3. Apply `guardrails/stylebook.md` and `guardrails/refusal-policy.md`.
4. Cite sources when possible (links or inline identifiers).

## Repo Map
```
resonate-gem-brain/
├─ README.md
├─ MANIFEST.md
├─ AGENTS.md
├─ VERSION
├─ agents/
│  ├─ strategist.md
│  ├─ copy-smith.md
│  ├─ code-sherpa.md
│  ├─ fact-checker.md
│  ├─ prompt-architect.md
│  └─ media/
│     ├─ AGENTS.md
│     ├─ namer.md
│     ├─ descriptor.md
│     ├─ lyricist.md
│     ├─ sonic-architect.md
│     ├─ cover-designer.md
│     └─ album-designer.md
├─ guardrails/
│  ├─ stylebook.md
│  └─ refusal-policy.md
├─ tools/
│  ├─ extensions.md
│  └─ data-sources.md
├─ examples/
│  ├─ prompts.md
│  └─ outputs.md
└─ datasets/
   └─ glossary.md
```
