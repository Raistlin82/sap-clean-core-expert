# Knowledge Map — SAP Clean Core Expert

Orientation for picking good query anchors. Node labels here are the **exact labels** to pass to
`graphify explain "<label>" --graph "$GRAPH"`. Full detail: `../knowledge/clean-core-extensibility/graphify-out/GRAPH_REPORT.md`.

## God nodes (most connected — the core abstractions)

Start here for broad questions; these bridge multiple communities.

| Node | Edges | Use it for |
|---|---:|---|
| `ABAP Test Cockpit` | 20 | Clean-core measurement, ATC variants, governance, AI fixes |
| `Released SAP APIs` | 16 | What makes an extension Level A; released vs classic APIs |
| `Clean Core Level A` | 14 | The compliant target level and its patterns |
| `Side-by-Side Extensibility` | 13 | BTP / decoupled extension option |
| `Clean Core Level B` | 11 | On-stack tolerated (deprecated tech) level |
| `Clean Core Level C` | 11 | Non-released usage / wrapper territory |
| `Key User Extensibility` | 11 | No-/low-code on-stack extensibility |
| `ABAP Cloud Development Model` | 11 | Developer on-stack model, released contracts |
| `SAP Build` | 10 | Low-code side-by-side + Key User bridge |
| `Clean Core Level D` | 9 | Non-compliant modifications |

## Communities (19; hubs to navigate by theme)

0. **Wrappers and Levels** — wrappers, ATC exemptions, level model, governance (33 nodes)
1. **ABAP Cloud Strategy** — ABAP Cloud vs classic model, BTP-first, brownfield transition (33)
2. **Key User Extensibility** — Custom Fields/Logic/Objects/CDS/Analytical Queries apps (29)
3. **Brownfield Technical Debt** — custom code migration, usage data, unused-code deletion (29)
4. **ATC Measurement** — ATC, check variants (`ABAP_CLOUD_DEVELOPMENT_DEFAULT`), KPI scores (26)
5. **Release Contracts** — release states, `ABAP_CLOUD_READINESS`, C0/C1 contracts, verification (23)
6. **AI Assisted Fixes** — ABAP MCP, AI fix proposals, S/4HANA Custom Code Migration Agent (18)
7. **RISE Methodology** — CALM runbook, success plan, maturity assessment, Joule (14)
8. **Architecture Decisioning** — AEM (assess use case / technology / target solution) (13)
9. **ABAP Cloud Components** — CAP, CDS views, extension implementation, developer skills (10)
10. **UI Extension Options** — Fiori Elements, SAPUI5, UI5 Web Components, Mobile Services (7)
11. **Governance Boards** — Solution Standardization Board, steering committee, decision templates (5)
12. **Classic Wrapper Setup** — classic ABAP, example wrapper software component (4)

Thinner hubs also present: Business AI Advisory, Released Extension Points, Discovery Center Missions,
Joule ABAP Capabilities, RAP Model, Cloud ERP Advisory.

## Hyperedges (multi-node patterns — cite these for "how does the whole X work")

- **Clean Core Level Model Forms A/B/C/D** — the level concept + all four levels
- **Level A Clean Extension Pattern** — Level A + ABAP Cloud model + SAP Build + Released APIs + on-stack + side-by-side
- **Wrapper Access Pattern for Non-Released Objects** — wrappers + non-released objects + ATC exemptions + levels B/C/D
- **On-Stack / Side-by-Side Selection Pattern** — decision tree + on-stack + side-by-side + Key User + Developer
- **SAP AEM Three Phase Pattern** — assess use case → assess technology → define target solution
- **Clean Core Governance and System Setup Pattern** — measurement framework + KPIs + the EXT-SYS-01..05 setup steps
- **Post-Conversion Debt Reduction Program** — debt reduction + unused-code retirement + pushdown + Fiori + replatforming + ATC
- **Clean Extensibility Level ATC Mapping** — levels A/B/C/D ↔ ATC checks (usage-of-APIs, critical statements)
- **Agentic Custom Code Modernization Flow** — Joule ABAP AI + Migration Agent + ATC + deterministic fixes + AI proposals + human review
- **Key User Extensibility Toolset** — UI adaptation + Custom Fields/Business Objects/Logic/CDS/Analytical Queries/Forms
- **Clean Core KPI Measurement System** — Clean Core Share + Technical Debt Score + Unused Code Share + Business Modifications + ATC + RISE dashboard
- **ATC to RISE Dashboard Import Flow** — ATC → clean-core variant → export file → RISE dashboard → object assessment

## Source-document index (`knowledge/clean-core-extensibility/raw/`)

Files are page-range chunks of the source PDF; the slug names the topic. Read the chunk cited by a
node's `src=` for exact wording.

> **Not in the public repo.** These `raw/*.md` files hold SAP's copyrighted full text and are **not**
> shipped in the public GitHub distribution. When absent, the same page ranges still let you cite the
> SAP publication (*Clean Core Extensibility for Architects*, 2026-07) by page — see SKILL.md step 2.

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
