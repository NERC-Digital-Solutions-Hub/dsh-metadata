# TREE_Northumbria_Gamma_Vegetation

## Overview
- Dataset of gamma spectroscopy measurements from vegetation samples collected in Northumbria.
- Includes species information, sampling site, sample identifiers, and description.
- Contains activity concentrations for K-40 and Cs-137 in both dry mass (DM) and fresh mass (FM), with associated counting errors and minimum detectable activities (MDA).
- Also provides Cs-137 concentration ratios comparing vegetation to soil for both DM and FM, plus related notes.

## Key fields and data structure
- Species and identification
  - Latin_Species_Name (Latin name of species)
  - Common_Species_Name (Common name)
  - Plant_Part_Analysed (plant part analyzed)
- Sampling and context
  - Site (sampling location)
  - CEH_Sample_Identifier (UKCEH radiochemistry lab unique sample ID)
  - CEH_Sample_Description (description of the UKCEH sample)
  - Sampling_Date_Used_As_Decay_Date (date the sample was taken; used as decay date)
- Mass and measurement context
  - Dry_Mass_Of_Sample_Analysed_g (dry mass in grams)
- Radioactivity measurements (K-40)
  - K-40_Bq_per_kg_DM (activity concentration in Bq/kg dry mass)
  - Counting_Error_K-40_Bq_per_kg_DM (two-sigma error, DM)
  - K-40_< (marker for values below MDA in DM)
  - MDA_K-40_Bq_per_kg_DM (minimum detectable activity in DM)
  - K-40_Bq_per_kg_FM (activity concentration in Bq/kg fresh mass)
  - Counting_Error_K-40_Bq_per_kg_FM (two-sigma error, FM)
  - K-40_< (marker for values below MDA in FM)
  - MDA_K-40_Bq_per_kg_FM (minimum detectable activity in FM)
- Radioactivity measurements (Cs-137)
  - Cs-137_Bq_per_kg_DM (activity concentration in Bq/kg DM)
  - Counting_Error_Cs-137_Bq_per_kg_DM (two-sigma error, DM)
  - Cs-137_DM_< (marker for values below MDA in DM)
  - MDA_Cs-137_Bq_per_kg_DM (minimum detectable activity in DM)
  - Cs-137_Bq_per_kg_FM (activity concentration in Bq/kg FM)
  - Counting_Error_Cs-137_Bq_per_kg_FM (two-sigma error, FM)
  - Cs-137_FM_< (marker for values below MDA in FM)
  - MDA_Cs-137_Bq_per_kg_FM (minimum detectable activity in FM)
- Concentration ratios (Cs-137)
  - Cs-137_Concentration_Ratio_DM_< (DM ratio below MDA indicator)
  - Cs-137_Concentration_Ratio_DM (Cs-137 concentration ratio, dry mass; vegetation divided by soil)
  - Cs-137_Concentration_Ratio_FM_< (FM ratio below MDA indicator)
  - Cs-137_Concentration_Ratio_FM (Cs-137 concentration ratio, fresh mass)
  - Notes_Related_to_137Cs_Concentration_Ratio (notes with values 1 or 2)
- General notes
  - General_Notes (notes section; values like 1 or 2)

## Measurement details and interpretation
- Units
  - Concentrations are in Bq per kilogram of dry mass (DM) or fresh mass (FM)
  - Mass reporting in grams (Dry_Mass_Of_Sample_Analysed_g)
- Detection and uncertainty
  - Two-sigma counting errors accompany each activity concentration
  - < markers indicate values below the minimum detectable activity (MDA) for the respective mass basis (DM or FM)
  - MDA fields provide the detection thresholds
- Cs-137 concentration ratios
  - Cs-137_Concentration_Ratio_DM: ratio of vegetation to soil activity concentrations on a dry-mass basis
  - Cs-137_Concentration_Ratio_FM: same ratio but on a fresh-mass basis
  - Formula example: vegetation (Bq/kg DM or FM) divided by soil (Bq/kg DM)
- Metadata usefulness
  - CEH_Sample_Identifier links to UKCEH radiochemistry records
  - Sampling_Date_Used_As_Decay_Date provides temporal context for decay corrections

## Data quality and GIS considerations
- Data may include non-detects (< MDA) requiring careful handling (censoring or imputation in maps)
- Data come from multiple fields and involve different resolutions; ensure consistent joins via Site or CEH_Sample_Identifier
- Important to preserve metadata: species, site, sample description, date, and mass basis (DM vs FM) for accurate visualization
- Concentration ratios offer a means to map bioaccumulation relative to soil background

## Practical GIS usage
- Create map layers for K-40_DM, Cs-137_DM, K-40_FM, Cs-137_FM concentrations by Site
- Generate ratio maps for Cs-137_Concentration_Ratio_DM and Cs-137_Concentration_Ratio_FM
- Use sample metadata (Species, Site, Sampling_Date_Used_As_Decay_Date) for pop-ups and filtering
- Represent non-detects with appropriate symbology (e.g., censored values) and document MDA thresholds in legend
- Include notes fields (Notes_Related_to_137Cs_Concentration_Ratio, General_Notes) to explain data caveats or methodological details

## Definitions and notes
- K-40 and Cs-137: radionuclide activity concentrations measured in dry and fresh mass
- MDA: minimum detectable activity
- Concentration Ratio: vegetation-to-soil activity ratio, expressed for DM and FM
- CEH_Sample_Identifier: UKCEH radiochemistry laboratory unique sample ID
- Sampling_Date_Used_As_Decay_Date: date used as reference for decay corrections