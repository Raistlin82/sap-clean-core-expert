# Knowledge Map — SAP Clean Core Expert

Orientation for picking good query anchors. Node labels here are the **exact labels** to pass to
`graphify explain "<label>" --graph "$GRAPH"`. Full detail: `../knowledge/clean-core-extensibility/graphify-out/GRAPH_REPORT.md`.

The knowledge base spans **all five clean-core principles** — Business Processes, Extensibility,
Data, Integration, Operations — plus the governance/maturity scoring model and the KPI measurement
framework. Sources (2026-07/08): the *Clean Core Extensibility for Architects* PDF, the L200 deck,
the Governance & Operational Practices Maturity deck, the Measurement Criteria for Clean Core KPIs
deck, the SAP SE Clean Core Data white paper, and the **Clean core integration white paper**.

## God nodes (most connected — the core abstractions)

Start here for broad questions; these bridge multiple communities. (Degree in the curated graph —
verified against `graph.curated.json`; `GRAPH_REPORT.md` lists slightly lower degrees because it
describes `graph.json`.) All labels in this file are verified to exist as exact node labels.

| Node | Edges | Use it for |
|---|---:|---|
| `Clean Core Integration` | 64 | The Integration principle: patterns, clean interfaces, Integration Suite, governance |
| `Clean Core Operations` | 35 | The Operations principle: toolchain, stack currency, secure ops, agility |
| `Released SAP APIs` | 30 | What makes an extension Level A; released vs classic APIs; integration contracts |
| `Clean Core Extensibility` | 28 | The Extensibility principle: on-stack / side-by-side, levels, released APIs |
| `Clean Core Level A` | 28 | The compliant target level and its patterns |
| `Clean Core Business Processes` | 27 | The Business-Processes principle: fit-to-standard, EAM/BPM/ALM |
| `SAP Cloud ALM` | 26 | Operations toolchain, monitoring, RISE methodology delivery |
| `Clean Core Data` | 25 | The Data principle: strategy, governance, quality, volume, protection |
| `ABAP Test Cockpit` | 21 | Clean-core measurement, ATC variants, governance, AI fixes |
| `Governance and Maturity` | 20 | Governance model + maturity scoring across the five principles |
| `Clean Core Extensibility Governance` | 19 | Extensibility governance, EXT-GOV / EXT-SYS practices |
| `Stay Clean` / `Get Clean` | 18 | Get-clean vs stay-clean journey across principles (esp. integration) |

## Communities — use the **curated** numbering (30 communities)

> ⚠️ **Two different numberings exist. Use this table, not `GRAPH_REPORT.md`'s.**
> The `community=N` tag printed by `graphify query`/`explain` comes from `graph.curated.json` (the graph
> the skill queries), which has **30** communities. `GRAPH_REPORT.md` describes `graph.json` and its
> **32** communities under *different numbers*. Never translate a `community=N` tag through the report.
> When in doubt, `graphify explain "<label>"` reports the definitive community for a specific node.

| N | Theme (curated) | Nodes | Highest-degree members |
|---:|---|---:|---|
| 0 | **Extensibility Debt & KPIs** | 58 | Clean Core Extensibility, Technical Debt Score, RISE with SAP Methodology Dashboard, Technical Debt Reduction, Clean Core Share |
| 1 | **ABAP Cloud & ATC Governance** | 46 | ABAP Test Cockpit, Clean Core Extensibility Governance, SAP BTP, ABAP Cloud |
| 2 | **Clean Operations & Toolchain** | 46 | Clean Core Operations, Integrated Toolchain Adoption, End-to-End Toolchain, agile delivery, SAP S/4HANA Cloud |
| 3 | **Clean Business Processes & Fit-to-Standard** | 41 | Clean Core Business Processes, SAP Cloud ALM, SAP Readiness Check, Five Clean Core Principles |
| 4 | **Key User Extensibility Toolset** | 32 | Custom Fields App, OData Services, Custom CDS Views App, SAP Fiori Adoption, Core Data Services |
| 5 | **Governance & Maturity Scoring** | 32 | Governance and Maturity, Clean Core Measurement Framework, Solution Standardization Board, Maturity Rating Scale |
| 6 | **Clean Core Integration hub / Get-&-Stay-Clean** | 26 | Clean Core Integration, Stay Clean, Get Clean, Center of Excellence, SAP LeanIX |
| 7 | **Released APIs & Integration Readiness** | 21 | Released SAP APIs, SAP Business Accelerator Hub, INT-08 SAP S/4HANA Integration Readiness, SAP API Policy |
| 8 | **Wrappers, Level C & ATC Exemptions** | 18 | Clean Core Level C, ATC Exemptions, ABAP Cloud Wrappers, Custom Wrappers, Partner Clean Core Certification |
| 9 | **Data Quality & Master Data** | 18 | Data Quality, SAP Master Data Governance, Master Data Management, Data Quality Management |
| 10 | **Business AI & Custom-Code Modernization** | 17 | S/4HANA Custom Code Migration Agent, Joule Studio, AI-Generated Fix Proposals, Customer-Built AI |
| 11 | **Integration Suite & Middleware** | 16 | SAP Integration Suite, SAP Application Interface Framework, API-Managed Connectivity, Central Middleware |
| 12 | **Data Volume Efficiency** | 15 | Data Volume Improvement Potential, Data Volume Efficiency, Clean Core Data Strategy, Outdated Data |
| 13 | **Clean Core Data & Governance** | 15 | Clean Core Data, Data Governance, SAP Information Lifecycle Management, DAT-01 Data Strategy Setup |
| 14 | **Event-Driven Integration** | 13 | Event-Driven Architecture, Business Events, INT-03 Integration Landscape, Advanced Event Mesh, Contract-Based Integration |
| 15 | **Level A & Modification Avoidance** | 13 | Clean Core Level A, Modifications/Clones/Implicit Enhancements, User and Customer Exits, BTP First Strategy |
| 16 | **Side-by-Side & SAP Build** | 13 | Side-by-Side Extensibility, SAP Build, SAP Build Code, SAP BTP ABAP Environment |
| 17 | **Extensibility Options (Key User / Dev / On-stack)** | 11 | Key User Extensibility, On-Stack Extensibility, Developer Extensibility, EXT-GOV-02 |
| 18 | **Data Strategy & Data Products** | 11 | Data Strategy, DAT-02 Data Governance Setup, Data Product, Data Product Economy, SAP One Domain Model |
| 19 | **Modern Data & Integration Tech** | 9 | SAP Business Data Cloud, Usage of Clean Interface Technologies, SAP Datasphere, Innovation Adoption |
| 20 | **AEM (Application Extension Methodology)** | 8 | SAP Application Extension Methodology, Extension Technology Mapping, Extension Architecture |
| 21 | **Data Protection & Compliance** | 8 | Data Protection, SAP Data Privacy Integration, Data Masking and Anonymization, Regulatory Compliance |
| 22 | **Integration Governance (ISA-M / ICoE)** | 8 | SAP Integration Solution Advisory Methodology, SAP Integration Assessment, Integration Center of Excellence, Decision Logging |
| 23 | **Integration Design Guidelines** | 7 | Integration Design Guidelines, Loose Coupling and API-First Design, Provider/Consumer Model, Graceful Error Handling |
| 24 | **Legacy Interfaces & Modernization** | 6 | Modernization Recommendations, API-Managed Protocols, IDoc, RFC, SOAP |
| 25 | **ABAP Cloud vs Classic Model** | 5 | ABAP Cloud Development Model, Clean Core Extensibility Model Level A, Classic ABAP Development Model, I_PRODUCT CDS View |
| 26 | **Applications-Data-AI Flywheel** | 5 | SAP Business AI, Clean Core Data Foundation, Joule, Applications-Data-AI Flywheel |
| 27 | **Data Quality Index (by domain)** | 5 | Data Quality Index, FI Data Quality, Business Partner Data Quality, Material Master Data Quality |
| 28 | **Data Tiering & Temperature** | 5 | Data Tiering, Warm/Hot/Cold Data, SAP HANA Native Storage Extension |
| 29 | **Business AI Advisory** | 2 | SAP Business AI Advisory, SAP Business AI Activation Advisory |

Sizes total 530 ✓. The Integration principle spans several hubs (6, 11, 14, 22, 23, 24) — start from
`Clean Core Integration` and follow edges. `GRAPH_REPORT.md`'s finer 32-community split is a useful
**thematic** inventory, but never resolve a `community=N` tag through it.

## Hyperedges (multi-node patterns — cite these for "how does the whole X work")

**Five-principle framing**
- **Five Clean Core Principles** — the five principle nodes + their shared parent
- **Clean Core KPI Measurement System** — Clean Core Share + Technical Debt Score + Unused Code Share + Business Modifications + ATC + RISE dashboard
- **Governance & Maturity Scoring Model** / **Clean Core Maturity Rating Scale (0–5)** — the maturity levels, evaluation criteria, current/target scoring
- Per-principle practice sets: **Clean Core Business Processes / Extensibility Governance / Extensibility System Setup / Data / Integration / Operations Practices** (the PRO/EXT/DAT/INT/OPS operational practices)
- Per-principle KPI sets: **Extensibility KPI Set**, **Clean Integration KPIs**, **Data Volume Efficiency KPIs**, **Adopt Clean Core Requirements Indices**

**Integration dimension**
- **Three clean core integration architectural patterns** — Central Middleware + API-Managed Connectivity + Event-Driven Architecture
- **Clean core integration governance model** — ISA-M + Integration Center of Excellence + Solution Standardization Board + SAP Integration Assessment
- **Core qualities of enterprise-grade integration flows** — Loose Coupling / API-First Design + Graceful Error Handling + Integration Design Guidelines
- **Agent-led toolchain** — SAP Signavio + SAP LeanIX + SAP Integration Suite + SAP Cloud ALM

**Data dimension**
- **Five Pillars of Clean Core Data** — Data Strategy / Governance / Quality / Volume Efficiency / Protection
- **Six Data Quality Dimensions** and the **Data Quality Index** composition
- **Clean Core Data Foundation** — foundation + culture + Applications-Data-AI flywheel

**Extensibility dimension**
- **Clean Core Level Model Forms A/B/C/D** — the level concept + all four levels
- **Level A Clean Extension Pattern** — Level A + ABAP Cloud model + SAP Build + Released APIs + on-stack + side-by-side
- **Wrapper Access Pattern for Non-Released Objects** — wrappers + non-released objects + ATC exemptions + levels B/C/D
- **On-Stack Side-by-Side Selection Pattern** — decision tree + on-stack + side-by-side + Key User + Developer
- **SAP AEM Three Phase Pattern** — assess use case → assess technology → define target solution
- **Clean Core Governance and System Setup Pattern** — measurement framework + KPIs + the EXT-SYS-01..05 setup steps
- **Clean Extensibility Level ATC Mapping** — levels A/B/C/D ↔ ATC checks
- **Key User Extensibility Toolset** — UI adaptation + Custom Fields/Business Objects/Logic/CDS/Analytical Queries/Forms

**Transition & AI**
- **Post-Conversion Debt Reduction Program** — debt reduction + unused-code retirement + pushdown + Fiori + replatforming + ATC
- **Agentic Custom Code Modernization Flow** — Joule ABAP AI + Migration Agent + ATC + deterministic fixes + AI proposals + human review
- **ATC to RISE Dashboard Import Flow** — ATC → clean-core variant → export → RISE dashboard → object assessment

## Source-document index (`knowledge/clean-core-extensibility/raw/`)

Files are page/slide-range chunks of the source documents; the slug names the topic. Read the chunk
cited by a node's `src=` for exact wording. Decks are cited by **Slide N**, PDFs by **PDF page N**.

> **Not in the public repo.** These `raw/*.md` files hold SAP's copyrighted full text and are **not**
> shipped in the public GitHub distribution. When absent, the same page/slide ranges still let you cite
> the SAP publications by page/slide — see SKILL.md step 2.

### Clean Core Extensibility for Architects (PDF, 2026-07) — the extensibility source
| Range | Topic |
|---|---|
| `001-025`, `026-050` | Introduction & the five clean-core principles |
| `051-075` | Clean Core Levels A/B/C/D — the level model |
| `076-100` | Level A on-stack: **Key User** extensibility |
| `101-125`, `126-150` | ABAP Cloud **Developer** extensibility (on-stack) |
| `151-175` | Level A **side-by-side** with SAP Build / BTP |
| `176-200`, `201-225` | **Released APIs and wrappers** |
| `226-250` | Architect transition to Level A |
| `251-275`, `276-300`, `301-325` | Layering & extensibility **option selection** (decision tree) |
| `326-350`, `351-375` | **AEM** (Application Extension Methodology) and wrapper guides |
| `376-400`, `401-425`, `426-450`, `451-475` | **Governance**, system setup, deployment, KPIs |
| `476-500`, `501-525`, `526-550` | **Brownfield conversion runbook** |
| `551-575`, `576-600` | **Custom code transition & ATC** |
| `601-625` … `701-725` | **SAP Business AI** context (Joule, agents) |
| `726-750`, `751-775`, `776-800` | Resources and references |
| `801-825` … `926-927` | Appendix: Key User deep-dive and details |

### 2026-07/08 additions (decks cited by Slide N; white papers by PDF page)
| Prefix / range | Source & topic |
|---|---|
| `l200-001-020`, `l200-021-039` | **Clean Core L200** deck — the five principles at first level of detail (Why/What/How) |
| `govops-001-025` … `govops-101-110` | **Governance & Operational Practices Maturity** deck — governance model, Maturity Rating Scale (0–5), PRO/DAT/INT/OPS practices |
| `kpi-001-025` … `kpi-076-095` | **Measurement Criteria for Clean Core KPIs** deck — measurement framework, recommended KPIs per principle + how to assess |
| `wp-001-015`, `wp-016-028` | **SAP SE Clean Core Data white paper** — data strategy, governance, quality, volume, protection |
| `int-001-025`, `int-026-049` | **Clean core integration white paper** — clean-integration principles, the three architecture patterns (middleware / API-managed / event-driven), API contracts (C0–C2), integration governance (ISA-M, ICoE, SSB), toolchain, and legacy-interface modernization |
