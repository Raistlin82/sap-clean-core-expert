# Clean Core Graph Curation

`graph.json` is the merged Graphify extraction over the 53 source documents: the original
*Clean Core Extensibility for Architects* PDF, the 2026-07 additions (the Clean Core L200 deck, the
Governance & Operational Practices Maturity deck, the Measurement Criteria for Clean Core KPIs deck,
and the SAP SE Clean Core Data white paper), and the 2026-08 addition — the **Clean core integration
white paper** (49 pages, chunked to `raw/int-001-025…` and `raw/int-026-049…`). `graph.curated.json`
is a deterministic runtime/exploration refinement on top of it.

| Metric | graph.json | curated |
|---|---:|---:|
| Nodes | 536 | 531 |
| Links | 1041 | 1062 |
| Zero-degree nodes | 5 | 0 |
| Curation alias merges | — | 7 |
| Restored nodes (v0.3.1) | — | 2 |

## Cross-source concept dedup (in graph.json)

Sources are extracted by parallel agents that independently label shared concepts, so the same idea
can arrive under one id from several files. During the merge these collapse to one node (kept by id;
the drop is logged), and near-duplicates are fuzzy-merged. The integration white paper was extracted
by two agents instructed to **reuse existing labels**; 23 of its concepts merged straight onto
existing nodes (e.g. `Clean Core Integration`, `SAP Integration Suite`, `SAP Integration Solution
Advisory Methodology`, the `INT-0x` practices, `Released SAP APIs`), while 60 net-new integration
concepts were added. Folded ids are recorded in each canonical node's `alias_ids`. This is
same-concept deduplication of an extraction artifact, not content interpretation.

## Curated layer (curated only)

Seven named alias merges collapse residual duplicate concepts:

- `extension_points` → `released_sap_extension_point`
- `joule_for_developers_abap` → `sap_joule_for_developers_abap_ai`
- `custom_code_migration_agent` → `s4hana_custom_code_migration_agent`
- `rise_with_sap_methodology_dashboard` → `rise_methodology_dashboard`
- `web_dynpro_fiori_modernization_agent` → `web_dynpro_to_sap_fiori_modernization_agent`
- `cloud_integration` → `sap_cloud_integration` *(new in v0.3.0 — integration white paper split one concept across two spellings)*
- `clean_core_levels_a_b_c_d` → `clean_core_levels` *(new in v0.3.1 — both carried the label "Clean Core Levels A, B, C, D"; links redirected, none lost)*

Three curated bridges connect otherwise weakly-linked high-level concepts:

- `sap_discovery_center_missions` -[supports]-> `side_by_side_extensibility`
- `abap_restful_application_programming_model` -[implements]-> `developer_extensibility`
- `sap_cloud_erp_private_advisory` -[supports]-> `clean_core_extensibility_governance`

The bridges are marked `confidence=CURATED` and never authorize execution. Finally, zero-degree nodes
are pruned (5 → 0; two of the five were cleared by the alias merges above, three by the bridges). These
three edges are interpretation, not source text: cite them as such, and never let them stand in for a
documented SAP statement.

## v0.3.1 fixes (curated only)

`graph.curated.json` now carries `graph.curation_version: 1`, the contract version that the companion
`sap-erp-clean-core-refactor` skill checks before it uses the graph.

- **Level B and Level D restored.** Up to v0.3.0 the curated graph had no `clean_core_level_b` /
  `clean_core_level_d` nodes, although three hyperedges (*Clean Core Level Model Forms A/B/C/D*,
  *Wrapper Access Pattern for Non-Released Objects*, *Clean Extensibility Level ATC Mapping*) still
  named them. Both nodes and their **20** links were copied from the extensibility-only curated graph
  of the companion skill (`Raistlin82/arc-1-fork` at `ed3a3c2`), which was built by the same graphify
  extraction of the *Clean Core Extensibility for Architects* PDF. They keep their original
  `EXTRACTED` confidence, source chunk and PDF page: they are extraction records, not interpretation.
  The node `source_url` was normalized to `sources/…`; both nodes joined curated community 8 (the
  majority community of their neighbours). That graph also has 12 more links that differ from this
  one only by relation name on node pairs this graph already links; they were not copied. The two
  nodes are absent from `graph.json` (never hand-edited); they return there on the next extraction.
  Their page citations were not re-read against `raw/` for this release (*da verificare*).
- **Stale alias removed.** `clean_core_integration.alias_ids` listed `clean_integration`, which is
  still a node of its own (linked to it by `semantically_similar_to`). The alias entry was removed;
  the node and its links are unchanged.
- **Duplicate label merged.** See the seventh alias merge above.

## Reading `GRAPH_REPORT.md` against the curated graph

The report is generated from `graph.json`; its community numbering does **not** carry over to
`graph.curated.json`:

| Report says | Curated reality |
|---|---|
| 32 communities, numbered 0–31 | **30** communities, **renumbered** — never resolve a `community=N` tag through the report (use `references/knowledge-map.md`, or `graphify explain "<label>"`) |
| 536 nodes / 1041 edges | 531 nodes / **1062** links in curated (−7 alias merges, +2 restored level nodes with 20 links, +3 CURATED bridges, minus deduped parallels) |
| degree-1 "isolated" nodes | 0 *zero-degree* nodes; degree-1 nodes still exist — different definitions, not a contradiction |

Link confidence in curated: **935 `EXTRACTED` · 124 `INFERRED` · 3 `CURATED`**. Hyperedges: 41.

Metadata note: `source_url` reads `sources/…` consistently across all 531 curated nodes and all 53
`raw/*.md` frontmatter headers (the 246 extensibility-PDF nodes are normalized from the old `source/…`
singular spelling). `graph.json` may still carry the old `source/…` spelling on those nodes because this
repo forbids hand-editing it; it re-aligns on the next graphify extraction. The CLI never prints this
field, so nothing user-visible depends on it.
