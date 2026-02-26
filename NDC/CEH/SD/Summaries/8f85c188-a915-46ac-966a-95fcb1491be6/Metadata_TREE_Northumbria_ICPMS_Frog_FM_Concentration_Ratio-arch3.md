# TREE_Northumbria_ICPMS_Bee_FM_Concentration_Ratio

## Purpose and scope
- Dataset documents concentration ratios of bee samples relative to surrounding soil, intended to assess uptake of elements from soil and inform environmental health monitoring.
- Facilitates comparative analysis across sampling sites and times to support policy decisions and monitoring framework development.

## Data structure and key fields
- Biological and site metadata
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - Sample_Details
  - CEH_Sample_Description
  - Notes
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Concentration ratio measurements
  - I_Concentration_Ratio
  - Li_Concentration_Ratio
  - Be_Concentration_Ratio (noted as a 'less than' value in some cases)
  - Na_Concentration_Ratio
  - Mg_Concentration_Ratio
  - Al_Concentration_Ratio
  - P_Concentration_Ratio
  - K_Concentration_Ratio
  - Ca_Concentration_Ratio
  - Ti_Concentration_Ratio
  - V_Concentration_Ratio
  - Cr_Concentration_Ratio
  - Mn_Concentration_Ratio
  - Fe_Concentration_Ratio
  - Co_Concentration_Ratio
  - Ni_Concentration_Ratio
  - Cu_Concentration_Ratio
  - Zn_Concentration_Ratio
  - As_Concentration_Ratio
  - Se_Concentration_Ratio (noted as a 'less than' value in some cases)
  - Rb_Concentration_Ratio
  - Sr_Concentration_Ratio
  - Mo_Concentration_Ratio
  - Ag_Concentration_Ratio
  - Cd_Concentration_Ratio
  - Cs_Concentration_Ratio
  - Ba_Concentration_Ratio
  - Tl_Concentration_Ratio
  - Pb_Concentration_Ratio
  - U_Concentration_Ratio (noted as a 'less than' value in some cases)
- Notes on measurement
  - All concentration ratios are defined as Fresh Mass Bee (wholebody) concentration divided by Dry Mass Soil
  - Units are not applicable (n/a)
  - Some columns include marker indicators for less-than values (e.g., <Be, <Se, <U)

## Measurement definition and purpose
- Concentration_Ratio = Bee’s Fresh Mass concentration / Soil’s Dry Mass concentration
- Enables assessment of metal/metalloid transfer from soil to bees, informing environmental exposure and risk assessments.

## Data provenance, metadata, and governance
- Metadata fields capture species, site, sampling date, sampling and sample description, and notes to support traceability.
- The dataset is structured to allow quality assurance, data cleaning, transformation, and clear presentation (reports, charts, dashboards).
- Emphasizes the potential for sharing underlying data and requires appropriate data governance, openness, and standards at the data source.

## Data quality challenges and considerations for monitoring frameworks
- Potential lack of data or data of insufficient quality for some elements or sites.
- Access barriers and data silos within/between organizations that may hinder data integration.
- Public sharing requirements for datasets that can impede data reuse.
- Inadequate metadata can hinder verification against requirements; data formats may require transformation.
- Communication of complex findings and maintaining up-to-date datasets require governance and clear metadata.

## Relevance to monitoring frameworks and policy
- Provides a structured, multi-site, multi-element dataset to monitor environmental health through pollinator exposure.
- Supports trend analysis, cross-site comparisons, and policy evaluation of soil-to-biota contamination pathways.
- Facilitates evidence-based reporting to stakeholders via dashboards and visualizations.

## Practical considerations for authors of monitoring frameworks
- Align data collection with clear metadata standards to enhance reuse and governance.
- Plan for data sharing, while addressing any access constraints and confidentiality considerations.
- Establish or strengthen data pipelines for QA, cleaning, transformation, and dissemination.
- Include transparent documentation of less-than values and any sampling limitations.

## Recommendations for implementation in monitoring programs
- Adopt standardized metadata schemas and consistent ratio definitions across datasets.
- Ensure open data practices where possible, with clear data governance to facilitate reuse.
- Implement regular metadata audits and updates to maintain data quality and usability.
- Develop dashboards and reports that clearly communicate concentration-ratio findings to policymakers and stakeholders.