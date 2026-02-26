# TREE_Northumbria_ICPMS_Toad_FM_Concentration_Ratio

## Overview
- Dataset of concentration ratios for toads relative to surrounding soil, calculated as Fresh Mass Toad (FM) divided by Dry Mass Soil.
- Measurements collected using ICPMS (implied by title) and linked to CEH sample codes/descriptions.
- Captures taxonomic identifiers, sampling context, and preparatory notes to support reuse and cross-study comparability.

## Key fields and Metadata
- Taxonomy and naming
  - Latin_Species_Name
  - Common_Species_Name
- Sampling context
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Code
  - CEH_Sample_Description
  - Notes (preparation of toads)
- Data provenance for ratio calculation
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Concentration ratios (element-by-element)
  - I_Concentration_Ratio, Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio
- Unit/definition notes
  - Units are shown as n/a in the metadata
  - Explanations describe the ratio as Fresh Mass Toad (whole body) divided By Dry Mass Soil

## Data collection and processing
- Samples come from defined sites with associated CEH codes/descriptions.
- For each toad sample, a co-located soil sample is used to compute the concentration ratio.
- Notes include preparation details for toads to support interpretation and reproducibility.

## Data quality and interoperability
- Metadata currently lists units as n/a and provides explanations, indicating a need for:
  - Standardized units across all concentration ratio fields
  - Clear, machine-readable data types and validation rules
  - Complete metadata for all fields to improve discoverability
- Potential inconsistencies in field labeling (e.g., minor typographical issues) should be resolved for interoperability.

## Access, sharing, and maintenance
- Intended workflow involves uploading datasets to relevant portals and catalogues; dataset should be maintained with updates when new samples are collected.
- Clear lineage from field collection through to ratio calculation should be documented to support auditing and reuse.

## Governance considerations and recommendations for Data Stewards
- Standardize units and data types across all concentration ratio fields to enable aggregation and cross-study analyses.
- Strengthen metadata completeness:
  - Ensure explicit units (e.g., mg/kg, dimensionless, etc.) where applicable
  - Provide precise explanations for each field (especially concentration ratios)
- Enforce data quality checks:
  - Validate presence of co-located soil sample for each ratio
  - Verify consistency between CEH sample codes/descriptions and associated metadata
- Improve data lineage documentation:
  - Capture methods for sample collection, preparation, and ratio calculation
  - Record any transformations or cleaning steps applied to raw data
- Implement versioning and change logs to track updates and corrections
- Align with common data standards for ecological and contaminant data to enhance discoverability and reuse across networks of datasets.