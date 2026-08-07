# Clean Core Graph Curation

`graph.json` is the merged Graphify extraction over the 53 source documents: the original
*Clean Core Extensibility for Architects* PDF, the 2026-07 additions (the Clean Core L200 deck, the
Governance & Operational Practices Maturity deck, the Measurement Criteria for Clean Core KPIs deck,
and the SAP SE Clean Core Data white paper), and the 2026-08 addition — the **Clean core integration
white paper** (49 pages, chunked to `raw/int-001-025…` and `raw/int-026-049…`). `graph.curated.json`
is a deterministic runtime/exploration refinement on top of it.

| Metric | graph.json | curated |
|---|---:|---:|
| Nodes | 536 | 530 |
| Links | 1041 | 1042 |
| Zero-degree nodes | 5 | 0 |
| Curation alias merges | — | 6 |

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

Six named alias merges collapse residual duplicate concepts:

- `extension_points` → `released_sap_extension_point`
- `joule_for_developers_abap` → `sap_joule_for_developers_abap_ai`
- `custom_code_migration_agent` → `s4hana_custom_code_migration_agent`
- `rise_with_sap_methodology_dashboard` → `rise_methodology_dashboard`
- `web_dynpro_fiori_modernization_agent` → `web_dynpro_to_sap_fiori_modernization_agent`
- `cloud_integration` → `sap_cloud_integration` *(new in v0.3.0 — integration white paper split one concept across two spellings)*

Three curated bridges connect otherwise weakly-linked high-level concepts:

- `sap_discovery_center_missions` -[supports]-> `side_by_side_extensibility`
- `abap_restful_application_programming_model` -[implements]-> `developer_extensibility`
- `sap_cloud_erp_private_advisory` -[supports]-> `clean_core_extensibility_governance`

The bridges are marked `confidence=CURATED` and never authorize execution. Finally, zero-degree nodes
are pruned (5 → 0; two of the five were cleared by the alias merges above, three by the bridges). These
three edges are interpretation, not source text: cite them as such, and never let them stand in for a
documented SAP statement.

## Reading `GRAPH_REPORT.md` against the curated graph

The report is generated from `graph.json`; its community numbering does **not** carry over to
`graph.curated.json`:

| Report says | Curated reality |
|---|---|
| 32 communities, numbered 0–31 | **30** communities, **renumbered** — never resolve a `community=N` tag through the report (use `references/knowledge-map.md`, or `graphify explain "<label>"`) |
| 536 nodes / 1041 edges | 530 nodes / **1042** links in curated (−6 alias merges, +3 CURATED bridges, minus deduped parallels) |
| degree-1 "isolated" nodes | 0 *zero-degree* nodes; degree-1 nodes still exist — different definitions, not a contradiction |

Link confidence in curated: **915 `EXTRACTED` · 124 `INFERRED` · 3 `CURATED`**. Hyperedges: 41.

Metadata note: `source_url` reads `sources/…` consistently across all 530 curated nodes and all 53
`raw/*.md` frontmatter headers (the 246 extensibility-PDF nodes are normalized from the old `source/…`
singular spelling). `graph.json` may still carry the old `source/…` spelling on those nodes because this
repo forbids hand-editing it; it re-aligns on the next graphify extraction. The CLI never prints this
field, so nothing user-visible depends on it.
