# Knowledge Map — SAP Clean Core Expert

Orientation for picking good query anchors. Node labels here are the **exact labels** to pass to
`graphify explain "<label>" --graph "$GRAPH"`. Full detail: `../knowledge/clean-core-extensibility/graphify-out/GRAPH_REPORT.md`.

The knowledge base now spans **all five clean-core principles** — Business Processes, Extensibility,
Data, Integration, Operations — plus the governance/maturity scoring model and the KPI measurement
framework (added 2026-07 from the L200, Governance & Maturity, KPI, and Data white-paper sources).

## God nodes (most connected — the core abstractions)

Start here for broad questions; these bridge multiple communities. (Degree in the curated graph.)

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

## Communities (24; hubs to navigate by theme)

0. **Extensibility Governance & ATC Measurement** — ATC, Clean Core Share, Technical Debt Score, usage data (66 nodes)
1. **Extensibility Model & Levels** — Levels A/B/C/D, ABAP Cloud, side-by-side, SAP Build (62)
2. **Clean Integration** — clean interface technologies, SAP Integration Suite, monitoring coverage (52)
3. **Clean Business Processes & Toolchain** — fit-to-standard, Cloud ALM, integrated toolchain, agile delivery (51)
4. **Governance & Maturity Scoring** — governance model, Maturity Rating Scale, measurement framework, RISE dashboard (38)
5. **Data Volume & Protection** — data volume efficiency/improvement, ILM, tiering, data protection (32)
6. **Key User Extensibility Toolset** — Custom Fields/Logic/Objects/CDS/Analytical apps, Extensibility Cockpit (29)
7. **Clean Operations** — stack currency (FPS/SPS age), EarlyWatch, secure baseline, test management (29)
8. **AI Custom-Code Modernization** — Custom Code Migration Agent, Joule Studio, AI fix proposals (24)
9. **Brownfield Debt Reduction** — technical-debt reduction, retire/renovate/innovate, Fiori adoption (17)
10. **Data Strategy & Products** — SAP Business Data Cloud, data products, democratization, One Domain Model (15)
11. **Master Data & Data Quality** — Master Data Governance/Management, get/keep data clean (14)
12. **Data Governance** — data governance board, DAT practices, metadata, data catalog (9)
13. **Application Extension Methodology (AEM)** — assess use case / technology / target solution (8)
14. **Clean Data Foundation & AI** — clean-data foundation, Applications-Data-AI flywheel, Business AI (6)
15. **Data Quality Management** — profiling, standardization, cleansing, Information Steward (6)
16. **Governance Boards** — Solution Standardization Board, SSB review, steering committee (6)
17. **Data Quality Index** — Data Quality Index and its FI / Business Partner / Material Master components (5)

Thin hubs (1–2 nodes) also present: Business AI Advisory, Released Extension Points, Discovery Center
Missions, Joule ABAP Capabilities, RAP Model, Cloud ERP Private Advisory.

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
- **On-Stack / Side-by-Side Selection Pattern** — decision tree + on-stack + side-by-side + Key User + Developer
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
