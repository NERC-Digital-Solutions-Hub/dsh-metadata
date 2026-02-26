# TREE_Northumbria_Gamma_Frogspawn

## Overview
- Radiochemical dataset for frogspawn samples from Northumbria, incorporating taxonomic details, sampling site, and UKCEH identifiers.
- Captures activity concentrations of K-40 and Cs-137 in both dry mass (DM) and fresh mass (FM), with associated uncertainties and detection limits.
- Includes sample metadata such as sampling date (used as decay date) and sample mass (dry mass analysed in grams).
- Provides concentration ratios and notes to support cross-media comparisons (e.g., frogspawn vs filtered water).

## Key data fields and meanings
- Taxonomy and site
  - Latin_Species_Name, Common_Species_Name
  - Site
  - CEH_Sample_Identifier, CEH_Sample_Description
- Sampling and sample mass
  - Sampling_Date_Used_As_Decay_Date
  - Dry_Mass_Of_Sample_Analysed_g
- Potassium-40 (K-40) measurements
  - K-40_Bq_per_kg_DM (activity in Bq/kg dry mass)
  - Counting_Error_K-40_Bq_per_kg_DM (two-sigma counting error)
  - K-40_< (indicator if value is below detection)
  - MDA_K-40_Bq_per_kg_DM (minimum detectable activity for DM)
  - K-40_Bq_per_kg_FM (activity in Bq/kg fresh mass)
  - Counting_Error_K-40_Bq_per_kg_FM (two-sigma counting error)
  - K-40_< (below detection marker for FM)
  - MDA_K-40_Bq_per_kg_FM (minimum detectable activity for FM)
- Cesium-137 (Cs-137) measurements
  - Cs-137_Bq_per_kg_DM (activity in Bq/kg DM)
  - Counting_Error_Cs-137_Bq_per_kg_DM (two-sigma counting error)
  - Cs-137_DM_< (below detection for DM)
  - MDA_Cs-137_Bq_per_kg_DM (minimum detectable activity for DM)
  - Cs-137_Bq_per_kg_FM (activity in Bq/kg FM)
  - Counting_Error_Cs-137_Bq_per_kg_FM (two-sigma counting error)
  - Cs-137_FM_< (below detection for FM)
  - MDA_Cs-137_Bq_per_kg_FM (minimum detectable activity for FM)
- Cs-137 concentration ratios
  - Cs-137_Concentration_Ratio_DW_<, FM (ratio in Bq/kg FM; below detection)
  - Cs-137_Concentration_Ratio_DM (ratio of DM frogspawn activity to DM activity in another medium)
  - Cs-137_Concentration_Ratio_FM_<, FM (ratio; below detection)
  - Cs-137_Concentration_Ratio_FM (ratio; DM activity in frogspawn divided by FM activity in filtered water)
  - Notes_Related_To_Cs-137_Concentration_Ratio (general notes)
- Additional notes
  - Notes_Related_To_Cs-137_Concentration_Ratio (context for the Cs-137 concentration ratios)

## Measurements, units and data quality
- Units
  - Bq per kg DM (dry mass)
  - Bq per kg FM (fresh mass)
  - g (grams) for dry mass analysed
- Detection and uncertainty
  - Two-sigma counting errors accompany activity values
  - MDA fields indicate the minimum detectable activity for each mass type
  - "<" markers denote concentrations below the MDA
- Data completeness and formats
  - Some fields indicate not measured or not applicable, reflecting detection limits or unavailable data
  - Ratios and notes provide context for interpreting cross-media comparisons

## How this data supports analysis and data products
- Enables self-serve exploration of:
  - Comparison of natural K-40 vs radiocesium Cs-137 across samples, masses, and sites
  - Cross-media analysis (frogspawn DM vs FM, and comparisons with filtered water)
  - Temporal analysis using the Sampling_Date_Used_As_Decay_Date
- Facilitates dashboard development:
  - Filter by species, site, and sample identifiers
  - Visualize activity concentrations with error bars and detection-limit indicators
  - Compare Cs-137 concentration ratios and interpret below-detection cases
- Supports data quality assessment:
  - Highlight instances with MDA-only values or missing measurements
  - Use counting errors to convey measurement precision

## Considerations for analysis
- Handle "<" values as below-detection and interpret using corresponding MDA
- Carefully manage multiple mass types (DM vs FM) when aggregating or comparing
- Use Cs-137 concentration ratios to assess relative radiocesium uptake between frogspawn and water samples
- Account for incomplete data and variable formats across records; rely on CEH_Sample_Identifier for traceability

## End-to-end data use pointers
- Start with metadata to query by site and species
- Pull K-40 and Cs-137 measurements for DM and FM, including errors and MDAs
- Compute derived metrics (e.g., concentration ratios) using the provided ratio fields and notes
- Build dashboards or reports that flag non-detects and highlight samples with robust measurements for reliable insights