# SAP Clean Core Expert

A Claude Code **plugin** that turns a curated SAP Clean Core knowledge base into a documentary,
read-only subject-matter expert. Ask it questions about SAP S/4HANA Clean Core extensibility and it
answers from a **GraphRAG knowledge graph** (246 nodes / 371 edges / 19 communities) plus **~106,000
words** of SAP source documents — always citing its sources.

It **explains and advises**. It never modifies a SAP system. For evidence-gated planning and guarded
execution on a live tenant, use the companion `sap-erp-clean-core-refactor` skill instead.

## What it answers

- Clean Core principles and the **Level A/B/C/D** model
- **Key User** vs **Developer** (on-stack) vs **side-by-side** (BTP) extensibility — when to use which
- **Released APIs and wrappers**; what makes an extension Level A
- The **ABAP Cloud development model** and the **AEM** (Application Extension Methodology)
- **ATC** clean-core check variants, **Clean Core Share** and technical-debt KPIs, governance setup
- **Brownfield** conversion / technical-debt reduction
- **SAP Business AI (Joule)** and the Custom Code Migration Agent in a clean-core context

## Install (local / development)

```bash
/plugin marketplace add /Users/gabriele.rendina/tools/sap-clean-core-expert
/plugin install sap-clean-core-expert@sap-clean-core-expert-dev
```

Restart Claude Code, then just ask a clean-core question — the skill activates on topic. The bundled
graph is queried via the [`graphify`](https://github.com/safishamsi/graphify) CLI; install it for
graph-native retrieval (there is a plain-text fallback if it is absent):

```bash
uv tool install graphifyy   # or: pip install graphifyy
```

## Usage examples

- "What's the difference between Clean Core Level A and Level B?"
- "When should I choose Key User extensibility over Developer Extensibility or a side-by-side app?"
- "How is Clean Core Share measured, and which ATC variant proves Level A?"
- "Walk me through the brownfield conversion runbook."

## Structure

```
sap-clean-core-expert/
├── .claude-plugin/
│   ├── plugin.json          # plugin manifest
│   └── marketplace.json     # dev marketplace (source: ./)
├── skills/
│   └── sap-clean-core-expert/
│       ├── SKILL.md          # expert protocol (retrieve → ground → cite)
│       ├── references/
│       │   └── knowledge-map.md   # communities, god nodes, patterns, doc index
│       └── knowledge/
│           └── clean-core-extensibility/
│               └── graphify-out/   # graph.curated.json (primary) + graph.json + reports
│                                   # raw/ (SAP full text) is NOT in this public repo — see below
└── README.md
```

## Knowledge provenance & copyright

Corpus: SAP publication *Clean Core Extensibility for Architects*, dated **2026-07**, imported from the
`sap-erp-clean-core-refactor` knowledge base and graphed with `graphify`. The curated graph adds a
few `CURATED` bridge edges (see `graphify-out/CURATION.md`) that are treated as interpretation, not
source text. Treat the corpus as SAP's documented position at that date — verify fast-moving details
against current SAP Notes / SAP Help.

**This public repository ships only the derived knowledge graph** (concept labels, relations, and
page citations) — it does **not** redistribute SAP's copyrighted full text. The `raw/*.md` source
documents are intentionally excluded (see `.gitignore`). Consequently, a clone of this repo runs the
expert in **graph-only mode**: it explains concepts and their relationships and cites the SAP
publication by page, but cannot quote passages it does not have. To enable full documentary mode,
supply your own licensed copy of the source under
`skills/sap-clean-core-expert/knowledge/clean-core-extensibility/raw/` — the skill detects it
automatically.

## Extending the knowledge

Add new sources and rebuild the graph with graphify:

```bash
cd skills/sap-clean-core-expert/knowledge/clean-core-extensibility
graphify add <url> --contributor "Your Name"   # fetch + ingest a source
graphify update .                               # re-extract and merge
```

## License

Not yet specified — add a `LICENSE` file before public distribution.
