# Graph Report - clean-core-extensibility  (2026-08-07)

## Corpus Check
- 53 files · ~185,371 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 536 nodes · 1041 edges · 32 communities (26 shown, 6 thin omitted)
- Extraction: 88% EXTRACTED · 12% INFERRED · 0% AMBIGUOUS · INFERRED: 124 edges (avg confidence: 0.8)
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `e88a31a7`
- Run `git rev-parse HEAD` and compare to check if the graph is stale.
- Run `graphify update .` after code changes (no API cost).

## Community Hubs (Navigation)
- Clean Core Extensibility
- Clean Core Operations
- Clean Core Extensibility Governance
- Clean Core Level A
- Released SAP APIs
- ABAP Test Cockpit
- Clean Core Integration
- SAP Business Data Cloud
- Z_UNCLEAN / HOME Software Component
- Released SAP Extension Points
- Custom Fields App
- SAP Business AI
- SAP Application Extension Methodology
- Create Custom UI Extension Task
- SAP Discovery Center Missions
- Extension End-to-End Process
- Governance and Maturity
- EXT-SYS-04 Usage Data Collection
- Clean Core Business Processes
- Technical Debt Reduction
- Classic ABAP Custom Code Transition
- Joule for Developers ABAP AI Capabilities
- ABAP RESTful Application Programming Model
- RISE with SAP Methodology Dashboard
- SAP Cloud ERP Private Advisory
- SAP Business AI Advisory
- Clean Core Data
- Data Strategy
- Data Quality
- Data Volume Improvement Potential
- Data Protection
- Data Tiering

## God Nodes (most connected - your core abstractions)
1. `Clean Core Integration` - 64 edges
2. `Clean Core Operations` - 35 edges
3. `Released SAP APIs` - 30 edges
4. `Clean Core Extensibility` - 28 edges
5. `Clean Core Level A` - 28 edges
6. `Clean Core Business Processes` - 27 edges
7. `SAP Cloud ALM` - 26 edges
8. `Clean Core Data` - 25 edges
9. `ABAP Test Cockpit` - 22 edges
10. `Governance and Maturity` - 20 edges

## Surprising Connections (you probably didn't know these)
- `Clean Integration` --semantically_similar_to--> `Clean Core Integration`  [INFERRED] [semantically similar]
  raw/int-001-025-clean-core-integration.md → raw/govops-051-075-governance-operational-practices-maturity.md
- `Clean Core Extensibility` --references--> `SAP Fiori Elements`  [INFERRED]
  raw/001-025-introduction-clean-core-principles.md → raw/326-350-aem-and-wrapper-guides.md
- `SAP Cloud Connector` --references--> `SAP BTP`  [INFERRED]
  raw/int-001-025-clean-core-integration.md → raw/276-300-layering-and-extensibility-option-selection.md
- `SAP LeanIX` --supports--> `Enterprise Architecture Management`  [INFERRED]
  raw/l200-021-039-clean-core-l200-overview.md → raw/l200-001-020-clean-core-l200-overview.md
- `Event-Driven Integration` --semantically_similar_to--> `Event-Driven Architecture`  [INFERRED] [semantically similar]
  raw/int-026-049-clean-core-integration.md → raw/int-001-025-clean-core-integration.md

## Hyperedges (group relationships)
- **Three clean core integration architectural patterns** — central_middleware, api_managed_connectivity, event_driven_architecture [EXTRACTED 1.00]
- **Clean core integration governance model** — sap_integration_solution_advisory_methodology, integration_center_of_excellence, solution_standardization_board, sap_integration_assessment [EXTRACTED 0.85]
- **Clean core measurement framework KPI dimensions** — upgrade_stability, operational_risk, innovation_adoption, toolchain_adoption [EXTRACTED 1.00]
- **Core qualities of enterprise-grade integration flows** — loose_coupling_and_api_first_design, graceful_error_handling, integration_design_guidelines [EXTRACTED 0.75]
- **ICoE, SSB, and decision logging form the integration governance framework** — integration_center_of_excellence, solution_standardization_board, decision_logging [EXTRACTED 1.00]
- **Agent-led toolchain: SAP Signavio, SAP LeanIX, SAP Integration Suite, SAP Cloud ALM** — sap_signavio, sap_leanix, sap_integration_suite, sap_cloud_alm [EXTRACTED 1.00]
- **Clean Core Level Model Forms A/B/C/D** — clean_core_level_concept, clean_core_level_a, clean_core_level_c [EXTRACTED 1.00]
- **Level A Clean Extension Pattern** — clean_core_level_a, abap_cloud_development_model, sap_build, released_sap_apis, on_stack_extensibility, side_by_side_extensibility [EXTRACTED 1.00]
- **Wrapper Access Pattern for Non-Released Objects** — abap_cloud_development_model, abap_cloud_wrappers, non_released_sap_objects, atc_exemptions, standard_abap_software_component, clean_core_level_c [EXTRACTED 1.00]
- **On-Stack Side-by-Side Selection Pattern** — decision_tree_best_extensibility_option, on_stack_extensibility, side_by_side_extensibility, key_user_extensibility, developer_extensibility [EXTRACTED 1.00]
- **SAP AEM Three Phase Pattern** — sap_application_extension_methodology, assess_extension_use_case, assess_extension_technology, define_extension_target_solution, extension_target_solution_diagram [EXTRACTED 1.00]
- **Clean Core Governance and System Setup Pattern** — clean_core_measurement_framework, governance_and_maturity, extensibility_kpis, ext_sys_01_automated_code_checks, ext_sys_02_exemption_process, ext_sys_03_abap_cloud_software_component, ext_sys_04_usage_data_collection, ext_sys_05_sap_btp_account_side_by_side [EXTRACTED 1.00]
- **Post-Conversion Debt Reduction Program** — technical_debt_reduction, unused_custom_code_retirement, sql_code_pushdown_performance_optimization, sap_fiori_adoption, sap_btp_replatforming, abap_test_cockpit [EXTRACTED 1.00]
- **Clean Extensibility Level ATC Mapping** — clean_extensibility_levels, clean_core_level_a, clean_core_level_c, usage_of_apis_check, critical_statements_check [EXTRACTED 1.00]
- **Agentic Custom Code Modernization Flow** — sap_joule_for_developers_abap_ai, s4hana_custom_code_migration_agent, abap_test_cockpit, deterministic_quick_fixes, ai_generated_fix_proposals, human_in_the_loop_review [EXTRACTED 1.00]
- **Key User Extensibility Toolset** — ui_adaptation_mode, custom_fields_app, custom_business_objects_app, custom_business_logic, custom_cds_views_app, custom_analytical_queries, custom_forms [EXTRACTED 1.00]
- **Clean Core KPI Measurement System** — clean_core_share, technical_debt_score, unused_code_share, business_modifications, abap_test_cockpit, custom_code_analytics, rise_with_sap_methodology_dashboard [EXTRACTED 1.00]
- **ATC to RISE Dashboard Import Flow** — abap_test_cockpit, clean_core_atc_variant, atc_check_results_export_file, rise_with_sap_methodology_dashboard, customer_object_assessment [EXTRACTED 1.00]
- **The Five Clean Core Principles (L200)** — clean_core_business_processes, clean_core_extensibility, clean_core_data, clean_core_integration, clean_core_operations [INFERRED 0.75]
- **Clean Core Data Foundation** — data_governance, data_strategy, data_quality, data_volume_efficiency, data_protection [INFERRED 0.75]
- **Extension End-to-End Governance Process** — functional_request, extension_architecture, extension_implementation, extension_deployment [INFERRED 0.75]
- **Extensibility KPIs (L200)** — clean_core_share, technical_debt_score, unused_code_share, business_modifications [INFERRED 0.75]
- **Clean Integration KPIs** — upgrade_stability_kpi, operational_risk_kpi, innovation_adoption_kpi [INFERRED 0.75]
- **Five Clean Core Principles** — clean_core_business_processes, clean_core_extensibility, clean_core_data, clean_core_integration, clean_core_operations [INFERRED 0.75]
- **Clean Core Maturity Rating Scale (0-5)** — maturity_level_0_not_started, maturity_level_1_beginner, maturity_level_2_intermediate, maturity_level_3_proficient, maturity_level_4_advanced, maturity_level_5_expert [INFERRED 0.75]
- **Governance & Maturity Scoring Model** — clean_core_maturity_rating_scale, evaluation_criteria, governance_and_maturity_practice, practice_importance_rating, current_score, target_score [INFERRED 0.75]
- **Clean Core Business Processes Practices** — pro_01_enterprise_architecture_management, pro_02_business_process_management, pro_03_application_lifecycle_management, pro_04_process_deviations_management, pro_05_change_management_and_user_enablement, pro_06_organization_transformation_readiness [INFERRED 0.75]
- **Extensibility Governance Practices** — ext_gov_01_governance_process_for_extensions, ext_gov_02_extension_architecture_guidelines, ext_gov_03_development_guidelines, ext_gov_04_developer_skills_enablement, ext_gov_05_measurements_kpis, ext_gov_06_housekeeping_practice [INFERRED 0.75]
- **Extensibility System Setup Practices** — ext_sys_01_automated_code_checks, ext_sys_02_exemption_process, ext_sys_03_abap_cloud_software_component, ext_sys_04_usage_data_collection, ext_sys_05_sap_btp_account_side_by_side [INFERRED 0.75]
- **Clean Core Data Practices** — dat_01_data_strategy_setup, dat_02_data_governance_setup, dat_03_data_quality_management, dat_04_data_volume_efficiency_management, dat_05_data_protection_setup [INFERRED 0.75]
- **Clean Core Integration Practices** — int_01_integration_strategy, int_02_integration_governance_process, int_03_integration_landscape, int_04_integrated_tool_chain, int_05_integration_organization_and_expert_enablement, int_06_integration_lifecycle_management, int_07_integration_documentation, int_08_sap_s_4hana_integration_readiness, int_09_operational_framework [INFERRED 0.75]
- **Clean Core Operations Practices** — ops_01_clean_core_governance, ops_02_business_transformation_toolchain, ops_03_continuous_improvement_for_an_enduring_clean_core, ops_04_test_management_and_execution, ops_05_software_delivery_efficiency, ops_06_secure_operations, ops_07_release_management, ops_08_it_operations_excellence [INFERRED 0.75]
- **Five Clean Core Principles** — clean_core_business_processes, clean_core_extensibility, clean_core_data, clean_core_integration, clean_core_operations [INFERRED 0.75]
- **Extensibility KPI Set** — clean_core_share, technical_debt_score, unused_code_share, business_modifications [INFERRED 0.75]
- **Data Volume Efficiency KPIs** — outdated_data, unused_data, redundant_data, optimized_sap_hana_usage, custom_table_footprint [INFERRED 0.75]
- **Adopt Clean Core Requirements Indices** — clean_core_process_index, clean_core_extensibility_index, clean_core_data_index, clean_core_integration_index, tracking_technical_debt_and_improvements [INFERRED 0.75]
- **Modern SAP Integration Technologies** — sap_integration_suite, sap_integration_suite_advanced_event_mesh, sap_master_data_integration, sap_datasphere, sap_business_data_cloud [INFERRED 0.75]
- **Five Pillars of Clean Core Data** — data_strategy, data_governance, data_quality, data_volume_efficiency, data_protection [INFERRED 0.75]
- **Governance and Maturity Practices for Clean Core Data** — maturity_of_data_governance_setup, maturity_of_data_strategy_setup, maturity_of_data_quality_management, maturity_of_data_volume_efficiency_management, maturity_of_data_protection_setup [INFERRED 0.75]
- **Six Data Quality Dimensions** — accuracy, completeness, consistency, timeliness, validity, uniqueness [INFERRED 0.75]
- **Data Volume Efficiency KPIs** — outdated_data, unused_data, redundant_data, optimized_sap_hana_usage, custom_table_footprint [INFERRED 0.75]

## Communities (32 total, 6 thin omitted)

### Community 13 - "Clean Core Extensibility"
Cohesion: 0.32
Nodes (13): Clean Core Extensibility, Extensibility KPIs, Clean Core Share, Technical Debt Score, Unused Code Share, Business Modifications, EXT-GOV-05 Measurements and KPIs, RISE with SAP Methodology Dashboard (+5 more)

### Community 6 - "Clean Core Operations"
Cohesion: 0.10
Nodes (30): Five Clean Core Principles, SAP S/4HANA Cloud, SAP Early Watch Alert, ABAP Unit Tests, Customer Center of Expertise, Operations Control Center, Secure Operations, SAP Security Baseline (+22 more)

### Community 9 - "Clean Core Extensibility Governance"
Cohesion: 0.16
Nodes (17): Clean Core Extensibility Governance, Avoid Extensions When Possible, I_PRODUCT CDS View, MARA Table, ABAP Cloud, Create Application Logic Extension Task, Exemption Process, Quality Manager (+9 more)

### Community 2 - "Clean Core Level A"
Cohesion: 0.06
Nodes (55): Clean Core Level Concept, Clean Core Level A, Clean Core Level C, BTP First Strategy, On-Stack Extensibility, Side-by-Side Extensibility, SAP Build, SAP Build Code (+47 more)

### Community 3 - "Released SAP APIs"
Cohesion: 0.06
Nodes (39): Released SAP APIs, Released SAP Remote API, Released SAP Local API, Released SAP Extension Point, Release Contracts, Contract C0 Extend, Contract C1 Use System-Internally, Contract C2 Use as Remote API (+31 more)

### Community 10 - "ABAP Test Cockpit"
Cohesion: 0.21
Nodes (15): ABAP Test Cockpit, SAP Note 3565942, SAP Note 3578329, Customer Object Assessment, Clean Core Levels A, B, C, D, Usage of APIs Check, ABAP_CLOUD_DEVELOPMENT_DEFAULT, Transport Release Process (+7 more)

### Community 0 - "Clean Core Integration"
Cohesion: 0.06
Nodes (64): SAP Note 3690029, Get Clean, Stay Clean, Brownfield Clean Core Journey, Greenfield Clean Core Approach, Agent-Led Toolchain, SAP Integration Solution Advisory Methodology, Event-Driven Architecture (+56 more)

### Community 16 - "SAP Business Data Cloud"
Cohesion: 0.33
Nodes (11): SAP BTP, SAP Master Data Integration, SAP Datasphere, Innovation Adoption, Usage of Clean Interface Technologies, Usage of Modern Integration Technologies, SAP Business Data Cloud, Data Democratization (+3 more)

### Community 25 - "Z_UNCLEAN / HOME Software Component"
Cohesion: 0.50
Nodes (4): Classic ABAP, Z_UNCLEAN / HOME Software Component, ZI_EXAMPLE_WRAPPER, SMODILOG Table

### Community 7 - "Custom Fields App"
Cohesion: 0.10
Nodes (29): Custom Fields App, Remote Custom APIs, Web Dynpro to SAP Fiori Modernization Agent, SAP Fiori Launchpad, UI Adaptation Mode, Adapt UI, Data Source Extensions, OData Services (+21 more)

### Community 22 - "SAP Business AI"
Cohesion: 0.40
Nodes (5): System of Records and Transaction, Joule, Clean Core Data Foundation, Applications-Data-AI Flywheel, SAP Business AI

### Community 18 - "SAP Application Extension Methodology"
Cohesion: 0.29
Nodes (8): SAP Application Extension Methodology, Assess Extension Use Case, Assess Extension Technology, Define Extension Target Solution, Extension Target Solution Diagram, Extension Technology Mapping, Technical Extension Building Blocks, Extension Architecture

### Community 20 - "Create Custom UI Extension Task"
Cohesion: 0.29
Nodes (7): Create Custom UI Extension Task, Extension Architecture Guide, SAP BTP Guidance Framework, SAP Fiori Elements, SAPUI5, UI5 Web Components, SAP Mobile Services

### Community 21 - "Extension End-to-End Process"
Cohesion: 0.33
Nodes (6): Wrappers for Missing Public SAP APIs, Extension End-to-End Process, Functional Request, Extension Implementation, Extension Deployment, ABAP Cloud Language Version

### Community 5 - "Governance and Maturity"
Cohesion: 0.08
Nodes (34): Clean Core Measurement Framework, Governance and Maturity, EXT-GOV-01 Governance Process for Extensions, Solution Standardization Board, SSB Design Review Process, Key Decision Document Template, Steering Committee, SAP Activate (+26 more)

### Community 14 - "EXT-SYS-04 Usage Data Collection"
Cohesion: 0.25
Nodes (11): EXT-GOV-06 Housekeeping Practice, EXT-SYS-04 Usage Data Collection, SCMON, SUSG, Online Collectors, Custom Code Usage Data Collection, Delete Unused Code, Unused Custom Code Retirement (+3 more)

### Community 1 - "Clean Core Business Processes"
Cohesion: 0.05
Nodes (56): SAP Cloud ALM, Quality Gate Process, Clean Core Runbook in CALM, Extensibility Maturity Assessment, Fit-to-Standard Approach, Process Segmentation, Pace-Layering, TIME Framework (+48 more)

### Community 4 - "Technical Debt Reduction"
Cohesion: 0.07
Nodes (35): SAP Fiori Adoption, Query Browser, Seven Migration and Modernization Assistants, Custom Code Assistant, Technical Debt Reduction, Post-Conversion Retire Renovate Innovate Strategy, SQL Code Pushdown for Performance Optimization, SQL Monitor (+27 more)

### Community 23 - "Classic ABAP Custom Code Transition"
Cohesion: 0.40
Nodes (5): Brownfield Conversion Runbook, SAP S/4HANA Cloud Private Edition System Conversion, Classic ABAP Custom Code Transition, RAP-Based SAP Fiori App, Mass Clean Core Adoption Agent

### Community 17 - "RISE with SAP Methodology Dashboard"
Cohesion: 0.36
Nodes (8): RISE with SAP Methodology Dashboard, ATC Check Results Export File, SAP Note 2781766, Adopt Clean Core Requirements, Clean Core Process Index, Clean Core Extensibility Index, Clean Core Data Index, Clean Core Integration Index

### Community 12 - "Clean Core Data"
Cohesion: 0.16
Nodes (15): Data Governance, Data Governance Board, SAP Information Lifecycle Management, Clean Core Data, DAT-01 Data Strategy Setup, DAT-03 Data Quality Management, DAT-04 Data Volume Efficiency Management, DAT-05 Data Protection Setup (+7 more)

### Community 15 - "Data Strategy"
Cohesion: 0.20
Nodes (11): Data Strategy, DAT-02 Data Governance Setup, Data Mesh and Data Fabric, Data Product, Maturity of Data Strategy Setup, Business-Aligned Data Strategy, Data Architecture and Integration, SAP and Non-SAP Data Harmonization (+3 more)

### Community 8 - "Data Quality"
Cohesion: 0.10
Nodes (23): Data Quality, SAP Master Data Governance, Data Quality Index, SAP MaxAttention, Maturity of Data Quality Management, Accuracy, Completeness, Consistency (+15 more)

### Community 11 - "Data Volume Improvement Potential"
Cohesion: 0.21
Nodes (15): Data Volume Efficiency, Data Volume Improvement Potential, Outdated Data, Unused Data, Redundant Data, Optimized SAP HANA Usage, Custom Table Footprint, Data Volume Management (+7 more)

### Community 19 - "Data Protection"
Cohesion: 0.29
Nodes (8): Data Protection, SAP Data Privacy Integration, Maturity of Data Protection Setup, Disaster Recovery and Backup, Data Access and Authorization Controls, Regulatory Compliance and Auditability, Data Masking and Anonymization, SAP Data Custodian

### Community 24 - "Data Tiering"
Cohesion: 0.40
Nodes (5): Data Tiering, Hot Data, Warm Data, Cold Data, SAP HANA Native Storage Extension

## Knowledge Gaps
- **165 isolated node(s):** `Avoid Extensions When Possible`, `Released SAP Remote API`, `Released SAP Local API`, `Released SAP Extension Point`, `Contract C0 Extend` (+160 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **6 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Clean Core Integration` connect `Clean Core Integration` to `Clean Core Business Processes`, `Clean Core Level A`, `Released SAP APIs`, `Governance and Maturity`, `Clean Core Operations`, `SAP Business Data Cloud`, `RISE with SAP Methodology Dashboard`?**
  _High betweenness centrality (0.277) - this node is a cross-community bridge._
- **Why does `Clean Core Extensibility` connect `Clean Core Extensibility` to `Clean Core Integration`, `Clean Core Level A`, `Released SAP APIs`, `Technical Debt Reduction`, `Governance and Maturity`, `Clean Core Operations`, `Clean Core Extensibility Governance`, `RISE with SAP Methodology Dashboard`, `SAP Application Extension Methodology`, `Create Custom UI Extension Task`, `Extension End-to-End Process`?**
  _High betweenness centrality (0.182) - this node is a cross-community bridge._
- **Why does `Clean Core Data` connect `Clean Core Data` to `Clean Core Integration`, `Governance and Maturity`, `Clean Core Operations`, `Data Quality`, `Data Volume Improvement Potential`, `Data Strategy`, `SAP Business Data Cloud`, `RISE with SAP Methodology Dashboard`, `Data Protection`, `SAP Business AI`?**
  _High betweenness centrality (0.142) - this node is a cross-community bridge._
- **Are the 9 inferred relationships involving `Clean Core Integration` (e.g. with `API Policy` and `SAP S/4HANA Cloud Private Edition`) actually correct?**
  _`Clean Core Integration` has 9 INFERRED edges - model-reasoned connections that need verification._
- **Are the 5 inferred relationships involving `Clean Core Operations` (e.g. with `Clean Core Measurement Framework` and `Clean Core Business Processes`) actually correct?**
  _`Clean Core Operations` has 5 INFERRED edges - model-reasoned connections that need verification._
- **Are the 5 inferred relationships involving `Released SAP APIs` (e.g. with `INT-08 SAP S/4HANA Integration Readiness` and `API-Managed Connectivity`) actually correct?**
  _`Released SAP APIs` has 5 INFERRED edges - model-reasoned connections that need verification._
- **Are the 6 inferred relationships involving `Clean Core Extensibility` (e.g. with `SAP Fiori Elements` and `Technical Debt Reduction`) actually correct?**
  _`Clean Core Extensibility` has 6 INFERRED edges - model-reasoned connections that need verification._