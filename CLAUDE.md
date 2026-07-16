# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

A Claude Code **plugin** — not an application. There is no build, lint, or test tooling. It packages a read-only, documentary subject-matter expert on SAP S/4HANA Clean Core extensibility: a `/clean-core-ask` slash command plus a skill that answers questions from a bundled GraphRAG knowledge graph and (optionally) SAP source documents, always citing sources.

## Commands

Install locally for development (inside a Claude Code session):

```
/plugin marketplace add /Users/gabriele.rendina/tools/sap-clean-core-expert
/plugin install sap-clean-core-expert@sap-clean-core-expert-dev
```

Package for Claude Desktop / Cowork (single `.plugin` zip; the artifact bundles `raw/` when present, so never publish it). Exclude `sources/` — the original SAP binaries are large and unneeded in the plugin (the `raw/*.md` chunks carry the full text):

```bash
zip -r dist/sap-clean-core-expert.plugin . -x '*.DS_Store' -x './.git/*' -x './dist/*' -x '*.plugin' -x '*/clean-core-extensibility/sources/*'
```

Query the knowledge graph directly (the skill's retrieval engine; install with `uv tool install graphifyy` or `pip install graphifyy`):

```bash
GRAPH=skills/sap-clean-core-expert/knowledge/clean-core-extensibility/graphify-out/graph.curated.json
graphify query "<question>" --graph "$GRAPH" --budget 1500
graphify explain "<Exact Node Label>" --graph "$GRAPH"   # exact labels are in references/knowledge-map.md
```

Extend the knowledge base (run from `skills/sap-clean-core-expert/knowledge/clean-core-extensibility/`):

```bash
graphify add <url> --contributor "Your Name"
graphify update .
```

## Architecture

Standard Claude Code plugin layout:

- `.claude-plugin/plugin.json` — plugin manifest; `marketplace.json` — dev marketplace with `source: "./"`.
- `commands/clean-core-ask.md` — the `/clean-core-ask` command; it delegates entirely to the skill.
- `skills/sap-clean-core-expert/SKILL.md` — the expert protocol: resolve KB path → retrieve via graphify → ground in cited sources → answer with citations.
- `skills/sap-clean-core-expert/references/knowledge-map.md` — the query-anchor index: exact node labels (god nodes), the 19 communities, hyperedge patterns, and the page-range index of source documents.
- `skills/sap-clean-core-expert/knowledge/clean-core-extensibility/` — the knowledge base itself.

Knowledge base layers:

- `graphify-out/graph.curated.json` — **primary retrieval artifact** (471 nodes / 931 edges). Alias-merged, zero isolated nodes, plus 3 curated bridge edges marked `confidence=CURATED` (interpretation, not source text — see `graphify-out/CURATION.md`).
- `graphify-out/graph.json` — the merged Graphify extraction (476 / 930). Never hand-edit it; extend it only via graphify extraction; it exists to cross-check the curated graph.
- `raw/*.md` — 51 page/slide-range chunks of the SAP sources (~170k words): the *Clean Core Extensibility for Architects* PDF plus the 2026-07 L200 / Governance & Maturity / KPI decks and the Data white paper. Gitignored; present only in private/full installs. The original binaries live under `sources/` (also gitignored).

The skill detects at runtime whether `raw/` exists (`HAS_RAW`): with it, answers quote the actual SAP wording (documentary mode); without it (any clone of the public repo), answers come from graph structure alone and cite the SAP sources by PDF page / slide — never fabricating quotations.

## Copyright constraint (critical)

The public repo ships **only the derived graph**. SAP's copyrighted full text (`raw/`), the original SAP source binaries (`sources/` — PDF/PPTX), and the packaged artifacts that bundle `raw/` (`dist/`, `*.plugin`) must never be committed or published — `.gitignore` enforces this. Do not weaken those ignore rules, and do not inline substantial `raw/*.md` text into committed files. The MIT license covers the plugin software only, not the knowledge under `knowledge/` (derived from SAP's *Clean Core Extensibility for Architects* PDF plus the 2026-07 Clean Core L200 / Governance & Maturity / KPI decks and Data white paper).

## Content conventions

- The expert is strictly **read-only / advisory**. It explains and compares; it never plans or executes changes on a live SAP system — that is handed off to the companion `sap-erp-clean-core-refactor` skill. Preserve this framing in any edit to `SKILL.md` or the command.
- Every answer must cite its source (node → `src=raw/<file>.md loc=PDF page N`), and edge-confidence labels (`EXTRACTED` vs `INFERRED`/`CURATED`) are part of the honesty contract in `SKILL.md`.
- Graph statistics (471 nodes / 931 edges / 24 communities, ~170k words, 51 source docs) are repeated across `README.md`, `plugin.json`, `marketplace.json`, `SKILL.md`, `knowledge-map.md`, and `graphify-out/CURATION.md` — if the graph is rebuilt, update all of them together. (Convention: node/edge counts are the curated graph; the community count is the `GRAPH_REPORT.md` figure from `graph.json`.)
