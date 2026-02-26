# TREE_Northumbria_Gamma_Frogspawn

## Scope and Purpose
- RadiochemicalData set for frogspawn samples, detailing gamma-emitting radionuclides measured in Northumbria samples.
- Contains identifiers, sampling details, mass measurements, activity concentrations, and derived ratios to support correlation, reporting, and forecasting analyses.
- Uses sampling date as the decay date reference where applicable.

## Data Structure and Key Variables
- Taxonomic and sampling identifiers:
  - Latin_Species_Name, Common_Species_Name
  - Site
  - CEH_Sample_Identifier (UKCEH unique sample ID)
  - CEH_Sample_Description (UKCEH Radiochemistry Laboratory description)
- Sampling metadata:
  - Sampling_Date_Used_As_Decay_Date
  - Dry_Mass_Of_Sample_Analysed_g
- Radionuclide activity concentrations (per mass):
  - K-40_Bq_per_kg_DM (per kg dry mass)
  - K-40_Bq_per_kg_FM (per kg fresh mass)
  - Cs-137_Bq_per_kg_DM (per kg dry mass)
  - Cs-137_Bq_per_kg_FM (per kg fresh mass)
- Uncertainties and detection limits:
  - Counting_Error_K-40_Bq_per_kg_DM
  - Counting_Error_K-40_Bq_per_kg_FM
  - Counting_Error_Cs-137_Bq_per_kg_DM
  - Counting_Error_Cs-137_Bq_per_kg_FM
  - MDA_K-40_Bq_per_kg_DM (Minimum Detectable Activity for K-40 DM)
  - MDA_K-40_Bq_per_kg_FM (Minimum Detectable Activity for K-40 FM)
  - MDA_Cs-137_Bq_per_kg_DM (Minimum Detectable Activity for Cs-137 DM)
  - MDA_Cs-137_Bq_per_kg_FM (Minimum Detectable Activity for Cs-137 FM)
- Detection flags and qualifiers:
  - K-40_<, Cs-137_DM_<, Cs-137_FM_< (indicates values below detection; "<" marker relates to corresponding MDA fields)
- Concentration ratios (Cs-137):
  - Cs-137_Concentration_Ratio_DM (ratio of Cs-137 per kg DM frogspawn to per kg FM in filtered water)
  - Cs-137_Concentration_Ratio_FM (ratio related to Cs-137 activity concentrations in frogspawn vs filtered Water)
  -Cs-137_Concentration_Ratio_DW_<, FM_< (indicate below-detection qualifiers for ratios)
- Notes:
  - Notes_Related_To_Cs-137_Concentration_Ratio (general notes for ratio interpretation)

## Measurements, Units, and Detection Limits
- Mass and dates:
  - Dry_Mass_Of_Sample_Analysed_g: grams (dry mass)
  - Sampling_Date_Used_As_Decay_Date: date reference for decay calculations
- Activity concentrations:
  - Units: Bq per kg DM (dry mass) and Bq per kg FM (fresh mass)
  - K-40 and Cs-137 activity concentrations are provided separately for DM and FM
- Uncertainty:
  - Counting_Error values are two-sigma uncertainties accompanying activity concentrations
- Detection limits:
  - MDA fields provide the minimum detectable activity for each radionuclide/mass basis
  - "<" markers indicate values below detection, tied to the corresponding MDA field
- Ratios:
  - Cs-137 concentration ratios quantify uptake comparisons between frogspawn and water matrices

## Ratios and Derived Metrics
- Cs-137_Concentration_Ratio_DM and Cs-137_Concentration_Ratio_FM quantify how Cs-137 activity in frogspawn relates to activity in the associated mass or water context.
- Notes field provides context for ratio interpretation and any caveats.

## Data Quality, Gaps, and Considerations
- Several fields indicate “Not measured” or n/a, reflecting incomplete measurements in some samples.
- Detection limits (MDAs) and "<" qualifiers are critical for interpreting non-detections and for downstream statistical handling.
- The dataset integrates both dry mass and fresh mass bases, requiring careful alignment when comparing across samples or studies.

## Potential Analyses for Analysts
- Correlation analyses between K-40 and Cs-137 concentrations within frogspawn, on both DM and FM bases.
- Cross-sample comparisons by Site or Species to identify spatial or biological patterns.
- Handling of left-censored data due to MDAs (treating < values appropriately in statistical models).
- Evaluation of Cs-137 uptake by comparing Cs-137_Concentration_Ratio_DM/FM across samples and linking to environmental water data (filtered water context).
- Data provenance and traceability checks using CEH_Sample_Identifier and CEH_Sample_Description to ensure reproducibility.