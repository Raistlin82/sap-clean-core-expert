# Graph Report - .  (2026-07-16)

## Corpus Check
- 51 files · ~170,380 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 476 nodes · 904 edges · 24 communities (18 shown, 6 thin omitted)
- Extraction: 91% EXTRACTED · 9% INFERRED · 0% AMBIGUOUS · INFERRED: 78 edges (avg confidence: 0.81)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- [[_COMMUNITY_Extensibility Governance & ATC Measurement|Extensibility Governance & ATC Measurement]]
- [[_COMMUNITY_Extensibility Model & Levels|Extensibility Model & Levels]]
- [[_COMMUNITY_Clean Integration|Clean Integration]]
- [[_COMMUNITY_Clean Business Processes & Toolchain|Clean Business Processes & Toolchain]]
- [[_COMMUNITY_Governance & Maturity Scoring|Governance & Maturity Scoring]]
- [[_COMMUNITY_Data Volume & Protection|Data Volume & Protection]]
- [[_COMMUNITY_Key User Extensibility Toolset|Key User Extensibility Toolset]]
- [[_COMMUNITY_Clean Operations|Clean Operations]]
- [[_COMMUNITY_AI Custom-Code Modernization|AI Custom-Code Modernization]]
- [[_COMMUNITY_Brownfield Debt Reduction|Brownfield Debt Reduction]]
- [[_COMMUNITY_Data Strategy & Products|Data Strategy & Products]]
- [[_COMMUNITY_Master Data & Data Quality|Master Data & Data Quality]]
- [[_COMMUNITY_Data Governance|Data Governance]]
- [[_COMMUNITY_Application Extension Methodology (AEM)|Application Extension Methodology (AEM)]]
- [[_COMMUNITY_Clean Data Foundation & AI|Clean Data Foundation & AI]]
- [[_COMMUNITY_Data Quality Management|Data Quality Management]]
- [[_COMMUNITY_Governance Boards|Governance Boards]]
- [[_COMMUNITY_Data Quality Index|Data Quality Index]]
- [[_COMMUNITY_Business AI Advisory|Business AI Advisory]]
- [[_COMMUNITY_Released Extension Points|Released Extension Points]]
- [[_COMMUNITY_Discovery Center Missions|Discovery Center Missions]]
- [[_COMMUNITY_Joule ABAP Capabilities|Joule ABAP Capabilities]]
- [[_COMMUNITY_RAP Model|RAP Model]]
- [[_COMMUNITY_Cloud ERP Private Advisory|Cloud ERP Private Advisory]]

## God Nodes (most connected - your core abstractions)
1. `Clean Core Integration` - 37 edges
2. `Clean Core Operations` - 35 edges
3. `Clean Core Extensibility` - 28 edges
4. `Clean Core Business Processes` - 27 edges
5. `Clean Core Data` - 25 edges
6. `ABAP Test Cockpit` - 23 edges
7. `Released SAP APIs` - 22 edges
8. `SAP Cloud ALM` - 22 edges
9. `Governance and Maturity` - 19 edges
10. `Clean Core Extensibility Governance` - 18 edges

## Surprising Connections (you probably didn't know these)
- `Joule` --part_of--> `SAP Business AI`  [INFERRED]
  raw/376-400-governance-system-setup-deployment.md → raw/wp-001-015-clean-core-data-white-paper.md
- `Clean Core Measurement Framework` --measures--> `Clean Core Extensibility`  [INFERRED]
  raw/426-450-governance-system-setup-deployment.md → raw/001-025-introduction-clean-core-principles.md
- `Clean Core Extensibility` --references--> `SAP Fiori Elements`  [INFERRED]
  raw/001-025-introduction-clean-core-principles.md → raw/326-350-aem-and-wrapper-guides.md
- `Extensibility KPIs` --part_of--> `Clean Core Extensibility`  [INFERRED]
  raw/426-450-governance-system-setup-deployment.md → raw/001-025-introduction-clean-core-principles.md
- `Clean Core Extensibility` --conceptually_related_to--> `Technical Debt Reduction`  [INFERRED]
  raw/001-025-introduction-clean-core-principles.md → raw/501-525-brownfield-conversion-runbook.md

## Hyperedges (group relationships)
- **Clean Core Level Model Forms A/B/C/D** — clean_core_level_concept, clean_core_level_a, clean_core_level_b, clean_core_level_c, clean_core_level_d [EXTRACTED 1.00]
- **Level A Clean Extension Pattern** — clean_core_level_a, abap_cloud_development_model, sap_build, released_sap_apis, on_stack_extensibility, side_by_side_extensibility [EXTRACTED 1.00]
- **Wrapper Access Pattern for Non-Released Objects** — abap_cloud_development_model, abap_cloud_wrappers, non_released_sap_objects, atc_exemptions, standard_abap_software_component, clean_core_level_b, clean_core_level_c, clean_core_level_d [EXTRACTED 1.00]
- **On-Stack Side-by-Side Selection Pattern** — decision_tree_best_extensibility_option, on_stack_extensibility, side_by_side_extensibility, key_user_extensibility, developer_extensibility [EXTRACTED 1.00]
- **SAP AEM Three Phase Pattern** — sap_application_extension_methodology, assess_extension_use_case, assess_extension_technology, define_extension_target_solution, extension_target_solution_diagram [EXTRACTED 1.00]
- **Clean Core Governance and System Setup Pattern** — clean_core_measurement_framework, governance_and_maturity, extensibility_kpis, ext_sys_01_automated_code_checks, ext_sys_02_exemption_process, ext_sys_03_abap_cloud_software_component, ext_sys_04_usage_data_collection, ext_sys_05_sap_btp_account_side_by_side [EXTRACTED 1.00]
- **Post-Conversion Debt Reduction Program** — technical_debt_reduction, unused_custom_code_retirement, sql_code_pushdown_performance_optimization, sap_fiori_adoption, sap_btp_replatforming, abap_test_cockpit [EXTRACTED 1.00]
- **Clean Extensibility Level ATC Mapping** — clean_extensibility_levels, clean_core_level_a, clean_core_level_b, clean_core_level_c, clean_core_level_d, usage_of_apis_check, critical_statements_check [EXTRACTED 1.00]
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

## Communities (24 total, 6 thin omitted)

### Community 0 - "Extensibility Governance & ATC Measurement"
Cohesion: 0.05
Nodes (66): ABAP Call Monitor, ABAP Cloud, ABAP_CLOUD_DEVELOPMENT_DEFAULT, ABAP_CLOUD_DEVELOPMENT_DEFAULT Check Variant, ABAP Cloud Language Version, ABAP Test Cockpit, ABAP Test Cockpit on SAP BTP, Allowed Enhancement Technologies Check (+58 more)

### Community 1 - "Extensibility Model & Levels"
Cohesion: 0.06
Nodes (62): ABAP Cloud Development Model, ABAP Cloud - Technical Use Cases and Recommended Technologies, ABAP Cloud Wrappers, ABAP for Cloud Development, ATC Exemption Browser, ATC Exemptions, BTP First Strategy, Changelog for SAP Objects (+54 more)

### Community 2 - "Clean Integration"
Cohesion: 0.07
Nodes (52): ABAP_CLOUD_READINESS Check Variant, ABAP Development Tools API State, Adoption of Integrated Toolchain for Integration Requirement Process, Agile Decision-Making and Operational Risks, API-Led Integration Strategy, Center of Excellence, Clean Core Integration, Clean Core Level Verification (+44 more)

### Community 3 - "Clean Business Processes & Toolchain"
Cohesion: 0.06
Nodes (51): Alignment to Clean Core, Alignment to SAP S/4HANA Target Architecture, Application Lifecycle Management, Business Capability Map, Business Process Management, Business Process Master List, Business Process Owner, Clean Core Business Processes (+43 more)

### Community 4 - "Governance & Maturity Scoring"
Cohesion: 0.07
Nodes (38): Adopt Clean Core Requirements, ATC Check Results Export File, Clean Core Data Index, Clean Core Extensibility Index, Clean Core Integration Index, Clean Core KPIs, Clean Core Maturity Rating Scale, Clean Core Measurement Framework (+30 more)

### Community 5 - "Data Volume & Protection"
Cohesion: 0.08
Nodes (32): Clean Core Culture, Clean Core Data Strategy, Cold Data, Custom Table Footprint, DAT-04 Data Volume Efficiency Management, DAT-05 Data Protection Setup, Data Access and Authorization Controls, Data Archiving (+24 more)

### Community 6 - "Key User Extensibility Toolset"
Cohesion: 0.10
Nodes (29): ABAP Language Version for Key Users, ABAP Web Editor, Adapt UI, Analytics Extensibility, Core Data Services, Custom Analytical Queries, Custom Business Logic, Custom Business Objects App (+21 more)

### Community 7 - "Clean Operations"
Cohesion: 0.11
Nodes (29): ABAP Unit Tests, Age of Feature Pack Stack, Age of Support Package Stack, CI/CD Pipeline, Clean Core Operations, Customer Center of Expertise, DevOps, Embed Secure Operations (+21 more)

### Community 8 - "AI Custom-Code Modernization"
Cohesion: 0.10
Nodes (24): ABAP MCP Server, Agent-Led Toolchain, AI Fix Confidence Score, AI-Generated Fix Proposals, AI-Generated Fixes, AI Units, Base AI, Custom Code Assistant (+16 more)

### Community 9 - "Brownfield Debt Reduction"
Cohesion: 0.12
Nodes (17): Analytical Apps, Brownfield Clean Core Journey, Clean Core Compliant Partner Solutions, Event Management, Greenfield Clean Core Approach, LOB Solutions, OPS-03 Continuous Improvement for an Enduring Clean Core, Post-Conversion Retire Renovate Innovate Strategy (+9 more)

### Community 10 - "Data Strategy & Products"
Cohesion: 0.17
Nodes (15): Business-Aligned Data Strategy, DAT-02 Data Governance Setup, Data Architecture and Integration, Data Democratization, Data Mesh and Data Fabric, Data Monetization, Data Product, Data Product Economy (+7 more)

### Community 11 - "Master Data & Data Quality"
Cohesion: 0.16
Nodes (14): Accuracy, Completeness, Consistency, Data Quality, Get Clean, Get Data Clean, INT-06 Integration Lifecycle Management, Keep Data Clean (+6 more)

### Community 12 - "Data Governance"
Cohesion: 0.22
Nodes (9): DAT-01 Data Strategy Setup, DAT-03 Data Quality Management, Data Catalog, Data Governance, Data Governance Board, Data Ownership and Stewardship, Data Policies and Compliance, Maturity of Data Governance Setup (+1 more)

### Community 13 - "Application Extension Methodology (AEM)"
Cohesion: 0.29
Nodes (8): Assess Extension Technology, Assess Extension Use Case, Define Extension Target Solution, Extension Architecture, Extension Target Solution Diagram, Extension Technology Mapping, SAP Application Extension Methodology, Technical Extension Building Blocks

### Community 14 - "Clean Data Foundation & AI"
Cohesion: 0.40
Nodes (6): Applications-Data-AI Flywheel, Clean Core Data, Clean Core Data Foundation, Data Framework, SAP Business AI, System of Records and Transaction

### Community 15 - "Data Quality Management"
Cohesion: 0.33
Nodes (6): Data Anomalies and Error Management, Data Cleansing and Enrichment, Data Profiling and Assessment, Data Quality Management, Data Standardization and Harmonization, SAP Information Steward

### Community 16 - "Governance Boards"
Cohesion: 0.33
Nodes (6): EXT-GOV-01 Governance Process for Extensions, Key Decision Document Template, PRO-04 Process Deviations Management, Solution Standardization Board, SSB Design Review Process, Steering Committee

### Community 17 - "Data Quality Index"
Cohesion: 0.40
Nodes (5): Business Partner Data Quality, Data Quality Index, FI Data Quality, Material Master Data Quality, SAP MaxAttention

## Knowledge Gaps
- **142 isolated node(s):** `Avoid Extensions When Possible`, `Released SAP Remote API`, `Released SAP Local API`, `Released SAP Extension Point`, `Contract C0 Extend` (+137 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **6 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Clean Core Extensibility` connect `Extensibility Model & Levels` to `Extensibility Governance & ATC Measurement`, `Clean Integration`, `Governance & Maturity Scoring`, `Clean Operations`, `Brownfield Debt Reduction`, `Application Extension Methodology (AEM)`, `Governance Boards`?**
  _High betweenness centrality (0.280) - this node is a cross-community bridge._
- **Why does `Clean Core Operations` connect `Clean Operations` to `Extensibility Model & Levels`, `Clean Integration`, `Clean Business Processes & Toolchain`, `Governance & Maturity Scoring`, `Brownfield Debt Reduction`, `Clean Data Foundation & AI`, `Governance Boards`?**
  _High betweenness centrality (0.179) - this node is a cross-community bridge._
- **Why does `Clean Core Data` connect `Clean Data Foundation & AI` to `Governance & Maturity Scoring`, `Data Volume & Protection`, `Clean Operations`, `Data Strategy & Products`, `Master Data & Data Quality`, `Data Governance`, `Governance Boards`, `Data Quality Index`?**
  _High betweenness centrality (0.171) - this node is a cross-community bridge._
- **Are the 2 inferred relationships involving `Clean Core Integration` (e.g. with `Clean Core Measurement Framework` and `Clean Core Operations`) actually correct?**
  _`Clean Core Integration` has 2 INFERRED edges - model-reasoned connections that need verification._
- **Are the 5 inferred relationships involving `Clean Core Operations` (e.g. with `Clean Core Measurement Framework` and `Clean Core Business Processes`) actually correct?**
  _`Clean Core Operations` has 5 INFERRED edges - model-reasoned connections that need verification._
- **Are the 6 inferred relationships involving `Clean Core Extensibility` (e.g. with `Clean Core Measurement Framework` and `SAP Fiori Elements`) actually correct?**
  _`Clean Core Extensibility` has 6 INFERRED edges - model-reasoned connections that need verification._
- **Are the 3 inferred relationships involving `Clean Core Business Processes` (e.g. with `Clean Core Measurement Framework` and `Clean Core Operations`) actually correct?**
  _`Clean Core Business Processes` has 3 INFERRED edges - model-reasoned connections that need verification._