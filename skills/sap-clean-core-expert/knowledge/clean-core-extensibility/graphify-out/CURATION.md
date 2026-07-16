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
are pruned (5 → 0). Runtime decisions use `decision-rules.json` plus live evidence, not these edges.
