# TREE_Northumbria_Gamma_Frogspawn

## Purpose and scope
- A radiochemical dataset for frogspawn samples containing activity concentrations of K-40 and Cs-137.
- Measurements provided in both dry mass (DM) and fresh mass (FM) units.
- Includes sample identifiers, species names, sampling site, description, and sampling/decay dates.
- Also includes concentration ratios comparing frogspawn to filtered water and related notes.

## Data fields and units (highlights)
- Species and site identifiers:
  - Latin_Species_Name, Common_Species_Name
  - Site
  - CEH_Sample_Identifier, CEH_Sample_Description
  - Sampling_Date_Used_As_Decay_Date
- Sample mass:
  - Dry_Mass_Of_Sample_Analysed_g
- Potassium-40 (K-40):
  - K-40_Bq_per_kg_DM with Counting_Error_K-40_Bq_per_kg_DM and K-40_< (less-than marker)
  - MDA_K-40_Bq_per_kg_DM (minimum detectable activity)
  - K-40_Bq_per_kg_FM with Counting_Error_K-40_Bq_per_kg_FM and K-40_< (FM)
  - MDA_K-40_Bq_per_kg_FM
- Cesium-137 (Cs-137):
  - Cs-137_Bq_per_kg_DM with Counting_Error_Cs-137_Bq_per_kg_DM and Cs-137_DM_< and MDA_Cs-137_Bq_per_kg_DM
  - Cs-137_Bq_per_kg_FM with Counting_Error_Cs-137_Bq_per_kg_FM and Cs-137_FM_< and MDA_Cs-137_Bq_per_kg_FM
- Cs-137 concentration ratios:
  - Cs-137_Concentration_Ratio_DM_<, FM (ratio in Bq per kg DM between frogspawn and filtered water)
  - Cs-137_Concentration_Ratio_FM_< (ratio in Bq per kg FM between frogspawn and filtered water)
- Notes:
  - Notes_Related_To_Cs-137_Concentration_Ratio (general notes on the ratios)
- Descriptions explain that "<" marks indicate values below the detection limit; MDA denotes minimum detectable activity.

## Data interpretation and GIS relevance
- Units: measurements in Bq per kilogram (DM or FM) depending on field.
- Useful for spatial visualization of radiochemical concentrations at sampling sites:
  - Map K-40 and Cs-137 concentrations by site and mass type (DM vs FM).
  - Create ratio maps comparing frogspawn to filtered water for Cs-137 in both DM and FM contexts.
- Uncertainty and detection:
  - Include two-sigma counting errors as measurement uncertainty.
  - Handle non-detects using the MDA fields and "<" markers in analyses and visualizations.

## Data quality, integration, and challenges
- Data may be distributed across multiple data sources; integration requires careful linking via Site and CEH_Sample_Identifier.
- Potential data issues:
  - Lack of consistent data standards and resolutions.
  - Missing or incomplete data, especially at appropriate resolutions for mapping.
  - Large/complex datasets needing cleaning and transformation before GIS use.
- Practical GIS considerations:
  - Standardize units (DM vs FM) when comparing across sites.
  - Properly encode and visualize non-detects (MDA and "<" values).
  - Use sample dates for temporal mapping and decay consideration.