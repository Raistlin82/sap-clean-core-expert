# Changelog

All notable changes to the SAP Clean Core Expert plugin.

## 0.3.0 — Clean Core Integration white paper

### Added

- Ingested the SAP **Clean core integration** white paper (49 pages) as the Integration principle's
  dedicated source: chunked to `raw/int-001-025…` / `raw/int-026-049…`, extracted by two graphify
  agents instructed to reuse existing labels, and merged into the graph.
- ~60 net-new integration concepts — the three architecture patterns (central middleware / API-managed
  connectivity / event-driven), API contracts (C0–C2), clean-integration principles (loose coupling,
  API-first, secure-by-design), integration governance (ISA-M, ICoE, SSB, decision logging), the
  agent-led toolchain, and legacy-interface modernization (IDoc/RFC/SOAP → API-managed).
- `Clean Core Integration` is now the graph's most-connected god node (64 edges).

### Changed

- Graph grew — curated **471 → 530 nodes / 931 → 1042 links / 14 → 30 communities / 35 → 41 hyperedges**
  (raw `graph.json` 476 → 536 / 930 → 1041 / 24 → 32). Corpus 51 → **53 documents**, ~170k → **~185k
  words**, across **6** SAP source publications. Link confidence: 915 EXTRACTED · 124 INFERRED · 3 CURATED.
- Curation gained a sixth alias merge (`cloud_integration` → `sap_cloud_integration`); the five prior
  merges and the three `CURATED` bridges are unchanged, and zero-degree nodes remain 0.
- All published figures updated across `README.md`, `plugin.json`, `marketplace.json`, `SKILL.md`,
  `references/knowledge-map.md`, `CURATION.md`, `GRAPH_REPORT.md`, and this file.

## 0.2.0 — accuracy audit

Every factual claim in the skill was verified against `graph.curated.json` and the `graphify` CLI.
Six defects were found and fixed. Retrieval quality is materially affected by the first two.

### Fixed

- **Community numbering was wrong (critical).** `references/knowledge-map.md` documented the **24**
  communities of `graph.json`, but the skill queries `graph.curated.json`, which has **14**, numbered
  differently. Because `SKILL.md` instructs the model to read the `community=N` tag, every lookup
  resolved to the wrong theme — e.g. curated `community=1` is **Clean Core Data**, but the table
  reported "Extensibility Model & Levels". The table is now generated from the curated graph (themes,
  sizes, highest-degree members; sizes sum to 471), with an explicit warning never to resolve a
  `community=N` tag through `GRAPH_REPORT.md`. Spot-checked 6/6 correct (previously 6/6 wrong).
- **`source_url` is never printed by the CLI**, yet step 2 told the model to read it from query output.
  Citations are now anchored to the `src=raw/<chunk>.md` name, with a chunk-prefix → publication map.
- **`--graph` documented as if optional.** Omitting it silently falls back to `graphify-out/graph.json`
  — the un-curated cross-check graph. Now stated as mandatory, with the reason.
- **Dangling reference to `decision-rules.json`** in `graphify-out/CURATION.md`; no such file exists in
  this repo (it belongs to the companion `sap-erp-clean-core-refactor` skill). Replaced with the actual
  rule governing the three `CURATED` bridge edges.
- **Wrong hyperedge label** `On-Stack / Side-by-Side Selection Pattern` → `On-Stack Side-by-Side
  Selection Pattern`. Exact labels matter: `graphify explain` takes them verbatim.
- **`GRAPH_REPORT.md` discrepancies were undocumented.** It describes `graph.json`, so its 904 edges
  (a same-endpoint collapsed count vs 930 actual links), its 24 renumbered communities, and its 142
  "isolated" nodes (degree ≤1, not zero-degree) do not describe the curated graph. `CURATION.md` now
  carries a reconciliation table.

### Changed

- `source_url` normalized to `sources/…` across all 471 curated nodes and all 51 `raw/*.md` frontmatter
  headers (246 nodes previously read `source/…`). Verified non-destructive: node/link/hyperedge counts
  (471 / 931 / 35) and the complete link set are unchanged. `graph.json` intentionally retains the old
  spelling, since this repo forbids hand-editing it.
- Published community count is now **14** (the curated graph) everywhere. `graph.json`'s figures
  (476 / 930 / 24) appear only where explicitly attributed to it.
- `SKILL.md` gained CLI guidance: handle the `[!] TRUNCATED` marker by raising `--budget` rather than
  answering from a partial node set, and a note that `graphify --help` omits `query` and `affected`
  even though both exist and work.

### Verified unchanged

God-node degrees (14/14 exact), all cited node labels (34/34 exist), zero-degree node count (0),
graph size (471 / 931), default `--budget` (2000), and every documented CLI command
(`query`, `explain`, `path`, `affected`, `--dfs`) against graphify **0.9.29**.

## 0.1.0 — initial release

Documentary, read-only expert on SAP S/4HANA Clean Core covering all five principles, the governance &
maturity scoring model, and the KPI measurement framework, backed by a GraphRAG knowledge graph and the
`/clean-core-ask` command.
