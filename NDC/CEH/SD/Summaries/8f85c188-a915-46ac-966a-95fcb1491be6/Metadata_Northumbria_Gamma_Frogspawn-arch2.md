# TREE_Northumbria_Gamma_Frogspawn

## Overview
- Dataset documenting radiochemical measurements in frogspawn to monitor environmental radiological health at Northumbria.
- Aims to produce standardized outputs (e.g., activity concentrations) for assessment of environmental health and policy performance over time.
- Data are intended to be stored and uploaded to appropriate data portals with clear sample identifiers.

## Data Content and Metadata
- Species and site information:
  - Latin_Species_Name, Common_Species_Name
  - Site (sampling location)
  - CEH_Sample_Identifier (UKCEH unique sample ID)
  - CEH_Sample_Description (UKCEH radiochemistry lab description)
  - Sampling_Date_Used_As_Decay_Date (sampling date used as decay date)
- Sample and mass details:
  - Dry_Mass_Of_Sample_Analysed_g
- Radionuclide measurements (activity concentrations):
  - K-40_Bq_per_kg_DM (Bq/kg dry mass)
  - K-40_Bq_per_kg_DM, Counting_Error_K-40_Bq_per_kg_DM
  - K-40_< (flag for below detection)
  - MDA_K-40_Bq_per_kg_DM (minimum detectable activity for K-40 in DM)
  - K-40_Bq_per_kg_FM (Bq/kg fresh mass)
  - K-40_Bq_per_kg_FM, Counting_Error_K-40_Bq_per_kg_FM
  - K-40_< (below detection marker for FM)
  - MDA_K-40_Bq_per_kg_FM
  - Cs-137_Bq_per_kg_DM, Counting_Error_Cs-137_Bq_per_kg_DM
  - Cs-137_DM_<, MDA_Cs-137_Bq_per_kg_DM
  - Cs-137_Bq_per_kg_FM, Counting_Error_Cs-137_Bq_per_kg_FM
  - Cs-137_FM_<, MDA_Cs-137_Bq_per_kg_FM
  - Cs-137_Bq_per_kg_DM and related MDA markers use consistent "less than" semantics
- Derived and ratio metrics:
  - Cs-137_Concentration_Ratio_DW_<, FM
  - Cs-137_Concentration_Ratio_DM, FM
  - Cs-137_Concentration_Ratio_FM_<, FM
  - Notes_Related_To_Cs-137_Concentration_Ratio
- General notes and interpretation:
  - Notes_Related_To_Cs-137_Concentration_Ratio provides context for ratio calculations

## Measurements and Units
- Units include Bq per kg (dry mass or fresh mass) for K-40 and Cs-137.
- Two-sigma counting errors accompany activity concentrations.
- Minimum detectable activity (MDA) values accompany measurements to indicate detection limits.
- Some entries use “<” markers to denote concentrations below detection limits.

## Data Quality Assurance and Handling
- Data are validated against established sources (e.g., UKCEH radiochemistry standards) and include QA markers like decay-date alignment with sampling.
- Clear handling of non-detects via MDA fields and “<” indicators.
- Includes sample identifiers and lab descriptions to support traceability.

## Derived Metrics and Ratios
- Cs-137 concentration ratios compare activity between frogspawn and water matrices (DM and FM contexts) to assess transfer and bioaccumulation.
- Ratio entries include notes to aid interpretation and indicate when values are not available (n/a) or below detection.

## Data Accessibility and Use
- Data are structured for upload to relevant environmental data portals.
- The standardized format supports time-series analysis for environmental monitoring and policy performance evaluation.

## Notes and Definitions
- Several fields labeled as “<” indicate concentrations below the minimum detectable activity.
- Notes fields provide additional context for Cs-137 concentration ratios and related interpretations.
- The dataset ties radiochemical measurements to specific sampling sites, specimens, and collection dates for longitudinal monitoring. 

## Relevance to Environmental Monitoring
- Enables consistent reporting of radiological status in frogspawn over time.
- Facilitates comparison across sites and dates, contributing to evaluation of environmental health and regulatory outcomes.
- Encourages data integration by explicitly naming sample identifiers, mass bases (DM/FM), and derived ratios to enhance dataset value beyond single-use analyses.