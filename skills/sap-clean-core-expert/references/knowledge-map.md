# Knowledge Map — SAP Clean Core Expert

Orientation for picking good query anchors. Node labels here are the **exact labels** to pass to
`graphify explain "<label>" --graph "$GRAPH"`. Full detail: `../knowledge/clean-core-extensibility/graphify-out/GRAPH_REPORT.md`.

The knowledge base now spans **all five clean-core principles** — Business Processes, Extensibility,
Data, Integration, Operations — plus the governance/maturity scoring model and the KPI measurement
framework (added 2026-07 from the L200, Governance & Maturity, KPI, and Data white-paper sources).

## God nodes (most connected — the core abstractions)

Start here for broad questions; these bridge multiple communities. (Degree in the curated graph —
verified against `graph.curated.json`; `GRAPH_REPORT.md` lists slightly lower degrees because it
describes `graph.json`.) All labels in this file are verified to exist as exact node labels.

| Node | Edges | Use it for |
|---|---:|---|
| `Clean Core Integration` | 37 | The Integration principle: clean interface tech, Integration Suite, monitoring |
| `Clean Core Operations` | 35 | The Operations principle: toolchain, stack currency, secure ops, agility |
| `Clean Core Extensibility` | 30 | The Extensibility principle: on-stack / side-by-side, levels, released APIs |
| `Clean Core Data` | 29 | The Data principle: strategy, governance, quality, volume, protection |
| `Clean Core Business Processes` | 27 | The Business-Processes principle: fit-to-standard, EAM/BPM/ALM |
| `ABAP Test Cockpit` | 25 | Clean-core measurement, ATC variants, governance, AI fixes |
| `Released SAP APIs` | 22 | What makes an extension Level A; released vs classic APIs |
| `SAP Cloud ALM` | 22 | Operations toolchain, monitoring, RISE methodology delivery |
| `Governance and Maturity` | 20 | Governance model + maturity scoring across the five principles |
| `Clean Core Extensibility Governance` | 19 | Extensibility governance, EXT-GOV / EXT-SYS practices |
| `Side-by-Side Extensibility` | 17 | BTP / decoupled extension option |
| `Data Quality` | 17 | Data-quality management, master data, get/keep data clean |
| `Technical Debt Score` | 15 | Custom-code debt KPI, ATC-driven measurement |
| `Clean Core Level A` | 14 | The compliant target level and its patterns |

## Communities — use the **curated** numbering (14 communities)

> ⚠️ **Two different numberings exist. Use this table, not `GRAPH_REPORT.md`'s.**
> The `community=N` tag printed by `graphify query`/`explain` comes from `graph.curated.json` (the graph
> the skill queries), which has **14** communities. `GRAPH_REPORT.md` describes `graph.json` and its
> **24** communities under *different numbers* — e.g. curated `community=1` is **Clean Core Data**, while
> `GRAPH_REPORT`'s community 1 is "Extensibility Model & Levels". Never translate a `community=N` tag
> through the report.

| N | Theme (curated) | Nodes | Highest-degree members |
|---:|---|---:|---|
| 0 | **Extensibility Governance & ATC Measurement** | 69 | Clean Core Extensibility, ABAP Test Cockpit, Clean Core Extensibility Governance, Technical Debt Score, RISE with SAP Methodology Dashboard |
| 1 | **Clean Core Data — volume, products, indices** | 58 | Clean Core Data, SAP Business Data Cloud, Data Volume Efficiency, Data Volume Improvement Potential, Data Quality Index |
| 2 | **Extensibility Model & Levels A/B/C/D** | 58 | Side-by-Side Extensibility, Clean Core Level A, SAP Build, Clean Core Level B, Clean Core Level C |
| 3 | **Clean Business Processes & Toolchain** | 51 | Clean Core Business Processes, SAP Cloud ALM, End-to-End Toolchain, agile delivery / operational excellence |
| 4 | **Clean Integration** | 42 | Clean Core Integration, SAP BTP, SAP Integration Suite, SAP Readiness Check, Usage of Clean Interface Technologies |
| 5 | **Governance & Maturity Scoring** | 37 | Governance and Maturity, Clean Core Measurement Framework, RISE with SAP Methodology, Solution Standardization Board, Clean Core Maturity Rating Scale |
| 6 | **Brownfield Debt Reduction & AI Custom-Code Modernization** | 30 | Technical Debt Reduction, S/4HANA Custom Code Migration Agent, SAP Fiori Adoption, Post-Conversion Retire/Renovate/Innovate, Joule Studio |
| 7 | **Released APIs, AEM & Extension Process** | 30 | Released SAP APIs, Extension End-to-End Process, Extension Deployment, SAP Application Extension Methodology, EXT-GOV-02 |
| 8 | **Key User Extensibility Toolset** | 29 | Custom Fields App, Custom CDS Views App, OData Services, Core Data Services, Custom Business Objects App |
| 9 | **Clean Operations** | 29 | Clean Core Operations, SAP S/4HANA Cloud, Age of Feature Pack Stack, Age of Support Package Stack, SAP Early Watch Alert |
| 10 | **Data Quality & Clean Data Foundation / AI** | 24 | Data Quality, Clean Core Data Foundation, Data Quality Management, SAP Business AI, Custom Code Assistant |
| 11 | **UI Extension Building Blocks** | 7 | Create Custom UI Extension Task, Extension Architecture Guide, SAP Fiori Elements, SAPUI5, SAP Mobile Services |
| 12 | **Data Tiering & Temperature** | 5 | Data Tiering, Hot / Warm / Cold Data, SAP HANA Native Storage Extension |
| 13 | **Business AI Advisory** | 2 | SAP Business AI Advisory, SAP Business AI Activation Advisory |

Sizes total 471 ✓. `GRAPH_REPORT.md`'s finer 24-community split (incl. thin hubs like Data Governance,
Governance Boards, Data Quality Index, RAP Model) is still useful as a **thematic** inventory — just not
for resolving a `community=N` tag.

## Hyperedges (multi-node patterns — cite these for "how does the whole X work")

**Five-principle framing**
- **Five Clean Core Principles** — the five principle nodes + their shared parent
- **Clean Core KPI Measurement System** — Clean Core Share + Technical Debt Score + Unused Code Share + Business Modifications + ATC + RISE dashboard
- **Governance & Maturity Scoring Model** / **Clean Core Maturity Rating Scale (0–5)** — the maturity levels, evaluation criteria, current/target scoring
- Per-principle practice sets: **Clean Core Business Processes / Extensibility Governance / Extensibility System Setup / Data / Integration / Operations Practices** (the PRO/EXT/DAT/INT/OPS operational practices)
- Per-principle KPI sets: **Extensibility KPI Set**, **Clean Integration KPIs**, **Data Volume Efficiency KPIs**, **Adopt Clean Core Requirements Indices**

**Data dimension**
- **Five Pillars of Clean Core Data** — Data Strategy / Governance / Quality / Volume Efficiency / Protection
- **Six Data Quality Dimensions** and the **Data Quality Index** composition
- **Clean Core Data Foundation** — foundation + culture + Applications-Data-AI flywheel

**Extensibility dimension (existing)**
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

### 2026-07 additions (decks cited by Slide N; white paper by PDF page)
| Prefix / range | Source & topic |
|---|---|
| `l200-001-020`, `l200-021-039` | **Clean Core L200** deck — the five principles at first level of detail (Why/What/How) |
| `govops-001-025` … `govops-101-110` | **Governance & Operational Practices Maturity** deck — governance model, Maturity Rating Scale (0–5), PRO/DAT/INT/OPS practices |
| `kpi-001-025` … `kpi-076-095` | **Measurement Criteria for Clean Core KPIs** deck — measurement framework, recommended KPIs per principle + how to assess |
| `wp-001-015`, `wp-016-028` | **SAP SE Clean Core Data white paper** — data strategy, governance, quality, volume, protection |
