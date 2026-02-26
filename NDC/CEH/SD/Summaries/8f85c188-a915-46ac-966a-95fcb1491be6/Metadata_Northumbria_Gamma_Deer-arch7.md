# TREE_Northumbria_Gamma_Deer

## Overview
- Data dictionary describing measurements of Cs-137 activity in roe deer samples collected at sampling sites (Northumbria area) for gamma-ray analysis.
- Focuses on the relationship between sample characteristics (species, tissue, mass) and radiometric results (Bq/kg) with associated quality metrics.
- Designed to be used in GIS contexts to map and analyse spatial patterns of Cs-137 contamination in deer.

## Key Variables (with purpose)
- Latin_Species_Name: Latin name of the species (Roe deer).  
- CEH_Sample_description: UKCEH sample description (description of the sample provenance or type).  
- Tissue: Tissue type analysed from Roe deer.  
- CEH_Sample_code: UKCEH Radiochemistry Laboratory unique sample identifier (traceability).  
- Site: Sampling site (location name or identifier).  
- Fresh_Mass_Of_Sample_Analysed_g: Fresh mass of the sample analysed (in grams).  
- Sampling_date_Used_As_Decay_date: Date the sample was taken and used as the decay date for activity calculations.  
- Cs-137_Bq_per_kg_FM: Activity concentration of Cs-137 in becquerels per kilogram fresh mass at the day of sampling.  
- Counting_Error_Cs-137_Bq_per_kg_DM: Two-sigma counting error of Cs-137 in Bq per kilogram dry mass (measurement uncertainty).  
- Cs-137 <: Marker indicating a value is below a detection threshold (non-detect).  
- MDA_Cs-137_Bq_per_kg_FM: Minimum detectable activity concentration of Cs-137 in Bq per kilogram fresh mass.  
- Cs-137_Concentration_Ratio_FM: Cs-137 concentration ratio for fresh mass (dimensionless); muscle concentration divided by soil dry-mass concentration.  
- CR_Notes: Notes related to the concentration ratio (context or caveats).

## Units and Measurements
- Concentrations: Bq per kg (both fresh mass and dry mass).  
- Mass: grams (g) for fresh mass of sample.  
- Date: sampling/decay date.  
- Ratio: dimensionless (concentration ratio).  
- Uncertainty: two-sigma counting error (Bq/kg_DM).  
- Non-detect indicators: “<” markers used with MDA and related fields.

## Spatial and GIS Considerations
- Site provides geographic context for mapping; no explicit coordinates in the field list, so spatial analysis relies on linking Site to a geospatial gazetteer or external site layer.  
- Relevant for creating map-based visualisations of Cs-137 distribution across sampling locations and tissue types, with attributes including species, sample details, and radiometric results.

## Data Quality and Provenance
- Includes traceability through CEH sample codes and site-specific sampling dates.  
- Provides measurement uncertainty (Counting_Error) and detection limits (MDA) to inform interpretation and filtering in analyses.  
- Presence of non-detect indicators (<) requires handling in GIS workflows (e.g., censoring or imputation).  
- Notes field (CR_Notes) captures contextual information for concentration ratios.  

## Suggested GIS Workflows
- Join dataset to a spatial layer of sampling sites using Site as the key; create point features with attributes from the variables above.  
- Visualise Cs-137_Bq_per_kg_FM as a graduated symbol or choropleth by site; separate layers can show fresh mass and tissue type.  
- Use MDA and Counting_Error to style or filter data (e.g., exclude non-detects or indicate uncertainty).  
- Compute or display Cs-137_Concentration_Ratio_FM to compare fresh-mass muscle concentrations to dry-mass soil baselines where applicable.  
- Ensure date fields are parsed as proper date types for temporal analyses (e.g., trend mapping over sampling periods).