# TREE_Northumbria_Gamma_Fungi

## Overview
- Dataset focused on gamma radiochemistry analysis in Northumbria fungi samples.
- Captures sample metadata, mass metrics, decay date reference, and radiological concentrations for K-40 and Cs-137.
- Includes measurements in both dry mass (DM) and fresh mass (FM), with associated counting errors and minimum detectable activities (MDA).
- Provides concentration ratios comparing fungi to soil, plus notes fields for interpretation and general context.

## Key Variables
- Latin_Species_Name: Latin species name.
- CEH_Sample_Identifier: UKCEH Radiochemistry Laboratory unique sample ID.
- Site: Sampling site.
- Mass_of_Sample_analysed_g: Mass of sample analysed (grams).
- Sampling_Date_Used_As_Decay_Date: Date of sampling (also used as decay date).
- Fresh_Mass_Dry_Mass_Ratio: Ratio of fresh mass to dry mass of soil.
- K-40_Bq_per_kg_DM: K-40 activity concentration in Bq/kg dry mass.
- Counting_Error_K-40_Bq_per_kg_DM: Two-sigma counting error for K-40 (DM).
- MDA_K-40_Bq_per_kg_DM: Minimum detectable activity for K-40 (DM).
- K-40_<: Indicator that the value is a "<" (less-than) value for K-40 in DM.
- Cs-137_Bq_per_kg_DM: Cs-137 activity concentration in Bq/kg dry mass.
- Counting_Error_Cs-137_Bq_per_kg_DM: Two-sigma counting error for Cs-137 (DM).
- Cs-137_<: Less-than indicator for Cs-137 in DM.
- MDA_Cs-137_Bq_per_kg_DM: MDA for Cs-137 (DM).
- K-40_Bq_per_kg_FM: K-40 activity concentration in Bq/kg fresh mass.
- Counting_Error_K-40_Bq_per_kg_FM: Two-sigma counting error for K-40 (FM).
- K40_<: Less-than indicator for K-40 in FM.
- MDA_K-40_Bq_per_kg_FM: MDA for K-40 (FM).
- Cs-137_Bq_per_kg_FM: Cs-137 activity concentration in Bq/kg fresh mass.
- Counting_Error_Cs-137_Bq_per_kg_FM: Two-sigma counting error for Cs-137 (FM).
- Cs-137_<: Less-than indicator for Cs-137 in FM.
- MDA_Cs-137_Bq_per_kg_FM: MDA for Cs-137 (FM).
- Cs-137_Concentration_Ratio_Fungi_FM: Fungi-to-soil concentration ratio for Cs-137 (FM).
- Cs-137_Concentration_Ratio_Fungi_DM: Fungi-to-soil concentration ratio for Cs-137 (DM).
- CR_Notes: Concentration ratio notes.
- General_Notes: General notes.

## Measurement Details
- Analytes: Potassium-40 (K-40) and Cesium-137 (Cs-137).
- Bases of quantification: Activity concentrations expressed per kilogram of dry mass (DM) and per kilogram of fresh mass (FM).
- Data quality flags: Includes MDA fields and "<" indicators to denote values below detection thresholds.
- Metadata: Includes sampling date and mass ratios to support decay corrections and normalization.

## Data Quality and Notes
- Some fields are marked as n/a, indicating missing or not applicable data in certain records.
- Concentration ratios enable assessment of fungal uptake relative to soil concentrations.
- General notes and CR notes provide guidance for interpretation and potential caveats in analyses.
- Data challenges in this context may include incomplete fields and the need to handle censored data (below MDA) in analyses.

## How to Use
- Assess correlations between fungal uptake (Cs-137 and K-40) and soil concentrations by using DM and FM values, accounting for decay date and mass basis.
- Compute concentration ratios Cs-137_Concentration_Ratio_Fungi_DM/FM and Cs-137_Concentration_Ratio_Fungi_DM to compare fungal vs soil burdens.
- Address censored data by properly handling "less than" (MDA) values and counting errors in statistical analyses.
- Use sample identifiers, site, and date to align with other datasets (e.g., soil measurements) and enable site-level or temporal trend analyses.
- Leverage notes fields (CR_Notes, General_Notes) to inform interpretation and any data caveats during reporting.