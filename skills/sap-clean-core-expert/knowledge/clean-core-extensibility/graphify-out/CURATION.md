# Clean Core Graph Curation

`graph.json` is the merged Graphify extraction over the 51 source documents (the original
*Clean Core Extensibility for Architects* PDF plus the 2026-07 additions: the Clean Core L200 deck,
the Governance & Operational Practices Maturity deck, the Measurement Criteria for Clean Core KPIs
deck, and the SAP SE Clean Core Data white paper). `graph.curated.json` is a deterministic
runtime/exploration refinement on top of it.

| Metric | graph.json | curated |
|---|---:|---:|
| Nodes | 476 | 471 |
| Links | 930 | 931 |
| Zero-degree nodes | 5 | 0 |
| Curation alias merges | — | 5 |

## Cross-agent concept dedup (in graph.json)

The four new sources were extracted in parallel by four agents that independently labelled shared
concepts — most visibly the **five clean-core principles**, which arrived as three spellings each
("Business Processes" / "Clean Business Processes" / "Clean Core Business Processes", etc.). During
the merge these were folded to one canonical per concept (the `Clean Core X` family, matching the
pre-existing `Clean Core Extensibility`), plus two product-name variants (`SAP One Data Model` →
`SAP One Domain Model`, `SAP Advanced Event Mesh` → `SAP Integration Suite, Advanced Event Mesh`).
Folded ids are recorded in each canonical node's `alias_ids`. This is same-concept deduplication of
an extraction artifact, not content interpretation.

## Curated layer (curated only)

Five named alias merges collapse residual duplicate concepts:

- `custom_code_migration_agent` → `s4hana_custom_code_migration_agent`
- `extension_points` → `released_sap_extension_point`
- `joule_for_developers_abap` → `sap_joule_for_developers_abap_ai`
- `rise_with_sap_methodology_dashboard` → `rise_methodology_dashboard`
- `web_dynpro_fiori_modernization_agent` → `web_dynpro_to_sap_fiori_modernization_agent`

Three curated bridges connect otherwise weakly-linked high-level concepts:

- `sap_discovery_center_missions` -[supports]-> `side_by_side_extensibility`
- `abap_restful_application_programming_model` -[implements]-> `developer_extensibility`
- `sap_cloud_erp_private_advisory` -[supports]-> `clean_core_extensibility_governance`

The bridges are marked `confidence=CURATED` and never authorize execution. Finally, zero-degree nodes
are pruned (5 → 0). These three edges are interpretation, not source text: cite them as such, and never
let them stand in for a documented SAP statement.

## Reading `GRAPH_REPORT.md` against the curated graph

The report is generated from `graph.json`; three figures do **not** carry over to `graph.curated.json`:

| Report says | Curated reality |
|---|---|
| 24 communities, numbered 0–23 | **14** communities, **renumbered** — never resolve a `community=N` tag through the report (use `references/knowledge-map.md`) |
| 904 edges | 930 links in `graph.json`, **931** in curated (904 is a same-endpoint collapsed count) |
| 142 isolated nodes (≤1 connection) | 0 *zero-degree* nodes; degree-1 nodes still exist — different definitions, not a contradiction |

Link confidence in curated: 848 `EXTRACTED` · 80 `INFERRED` · 3 `CURATED`.

Metadata note (normalized in v0.2.0): `source_url` used to read `source/…` (singular) on the 246
extensibility-PDF nodes and `sources/…` on the other 225. All 471 curated nodes — and all 51 `raw/*.md`
frontmatter headers — now use `sources/…` consistently. The replacement was an exact quoted-string
substitution: node/link/hyperedge counts (471 / 931 / 35) and the full link set are byte-for-byte
unchanged. `graph.json` deliberately still carries the old `source/…` spelling, because this repo forbids
hand-editing it; it will re-align on the next graphify extraction. Note the CLI never prints this field,
so nothing user-visible depended on it either way.
