# TREE_Northumbria_Gamma_Fungi

## Overview
- A radiochemical dataset of fungal samples from Northumbria, focused on gamma-emitting isotopes K-40 and Cs-137.
- Includes sample metadata (species, site, mass, date) and both dry-mass and fresh-mass activity concentrations, along with detection limits, counting errors, and concentration ratios to soil.
- Designed to support map-based data visualizations and spatial analysis in GIS.

## Key fields and meanings

- Sample metadata
  - Latin_Species_Name: Latin name of the fungal species.
  - CEH_Sample_Identifier: UKCEH Radiochemistry Laboratory unique sample ID.
  - Site: Sampling site.
  - Mass_of_Sample_analysed_g: Mass of the sample analysed (in grams).
  - Sampling_Date_Used_As_Decay_Date: Sample date used as decay date.
  - Fresh_Mass_Dry_Mass_Ratio: Ratio of fresh mass to freeze-dried mass.

- Measurements (dry mass, Bq/kg_DM)
  - K-40_Bq_per_kg_DM: K-40 activity concentration in Bq per kg dry mass at sampling.
  - Counting_Error_K-40_Bq_per_kg_DM: Two-sigma counting error for K-40 in DM.
  - MDA_K-40_Bq_per_kg_DM: Minimum detectable activity for K-40 in DM.
  - K-40_<: < marker indicating that the value is below the MDA_K-40_Bq_per_kg_DM.
  - Cs-137_Bq_per_kg_DM: Cs-137 activity concentration in Bq per kg dry mass at sampling.
  - Counting_Error_Cs-137_Bq_per_kg_DM: Two-sigma counting error for Cs-137 in DM.
  - Cs-137_<: < marker indicating the value is below the MDA_Cs-137_Bq_per_kg_DM.
  - MDA_Cs-137_Bq_per_kg_DM: Minimum detectable activity for Cs-137 in DM.

- Measurements (fresh mass, Bq/kg_FM)
  - K-40_Bq_per_kg_FM: K-40 activity concentration in Bq per kg fresh mass at sampling.
  - Counting_Error_K-40_Bq_per_kg_FM: Two-sigma counting error for K-40 in FM.
  - K40_<: < marker indicating the value is below the MDA_K-40_Bq_per_kg_FM.
  - MDA_K-40_Bq_per_kg_FM: Minimum detectable activity for K-40 in FM.
  - Cs-137_Bq_per_kg_FM: Cs-137 activity concentration in Bq per kg fresh mass at sampling.
  - Counting_Error_Cs-137_Bq_per_kg_FM: Two-sigma counting error for Cs-137 in FM.
  - Cs-137_<: < marker indicating the value is below the MDA_Cs-137_Bq_per_kg_FM.
  - MDA_Cs-137_Bq_per_kg_FM: Minimum detectable activity for Cs-137 in FM.

- Concentration ratios (fungi vs soil)
  - Cs-137_Concentration_Ratio_Fungi_FM: Concentration ratio (fungi Bq/kg fresh mass divided by soil Bq/kg fresh mass). Note indicates n/a in some fields.
  - Cs-137_Concentration_Ratio_Fungi_DM: Concentration ratio (fungi Bq/kg dry mass divided by soil Bq/kg dry mass). Note indicates n/a in some fields.
  - CR_Notes: Notes about concentration ratios.
  - General_Notes: General notes about the dataset.

## Spatial relevance and GIS-ready structure
- Each record associates lab results with a sampling site and sample identifier, enabling joins to site or polygon point data in GIS.
- Allows creation of map layers for:
  - K-40 and Cs-137 activity (DM and FM) by site or sample.
  - Non-detects represented via MDA markers or set to NODATA/ censored values.
  - Concentration-ratio maps comparing fungi to soil for both DM and FM.

## Data units and interpretation
- Activity concentrations in Bq per kg (dry mass or fresh mass).
- Mass measurements in grams.
- Ratios are dimensionless.
- "<" markers denote values below the reported MDA and should be treated as censored or substituted according to analysis workflow.

## Data quality considerations
- Presence of detection limits (MDAs) and counting errors enables uncertainty quantification in GIS workflows.
- Distinguish between DM (dry mass) and FM (fresh mass) measurements; ensure consistent unit use when visualizing.
- Non-detects require explicit handling in analyses (e.g., substitution, censoring, or masked visualization).

## Practical GIS workflows
- Data integration
  - Join by CEH_Sample_Identifier (and/or Site) to spatial layers containing sampling locations.
- Visualization
  - Create choropleth or symbol maps for K-40 and Cs-137 by DM and FM.
  - Produce separate layers for dry-mass (DM) and fresh-mass (FM) concentrations.
  - Map concentration ratios for fungi vs soil (DM and FM) where data exist.
- Handling non-detects
  - Treat "<" values as censored data; apply consistent rules (e.g., use MDA as floor, or encode as NODATA with separate flag).
- Aggregation and analysis
  - Group by Site or Latin_Species_Name to summarize activity concentrations and uncertainties.
  - Compare fungal concentrations against soil baselines via the concentration ratio fields.
- Data integrity
  - Use CEH_Sample_Identifier to trace back to lab results; verify mass and date fields for temporal analysis.

## Notes on provenance and metadata
- CEH_Sample_Identifier links to UKCEH Radiochemistry laboratory results.
- Sampling_Date_Used_As_Decay_Date provides temporal context for activity measurements.
- General_Notes and CR_Notes capture methodological notes relevant to interpretation and cross-site comparisons.