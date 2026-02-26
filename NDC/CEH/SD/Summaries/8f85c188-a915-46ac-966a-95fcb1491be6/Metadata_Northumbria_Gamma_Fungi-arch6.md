# TREE_Northumbria_Gamma_Fungi

## Overview
- Dataset describing gamma-emitting isotopes K-40 and Cs-137 in soil and fungi.
- Measurements expressed as activity concentration in Bq per kilogram, for both dry mass (DM) and fresh mass (FM).
- Includes sample metadata (Latin species name, UKCEH sample identifier, sampling site, date, sample mass, and fresh/dry mass ratio).
- Data fields support analysis of fungal uptake versus soil, with concentration ratios and quality indicators.

## Key Variables and Measurements
- Sample identifiers and context
  - Latin_Species_Name: scientific name of fungi.
  - CEH_Sample_Identifier: UKCEH Radiochemistry Laboratory sample ID.
  - Site: sampling location.
  - Sampling_Date_Used_As_Decay_Date: date taken, also used as decay date.
  - Mass_of_Sample_analysed_g: mass analyzed (g).
  - Fresh_Mass_Dry_Mass_Ratio: ratio of fresh mass to dry mass.
- Radioactivity measurements (per mass basis)
  - K-40_Bq_per_kg_DM: K-40 activity in dry mass (Bq/kg_DM).
  - Counting_Error_K-40_Bq_per_kg_DM: two-sigma counting error for K-40_DM.
  - MDA_K-40_Bq_per_kg_DM: minimum detectable activity for K-40 in DM.
  - K-40_Bq_per_kg_FM: K-40 activity in fresh mass (Bq/kg_FM).
  - Counting_Error_K-40_Bq_per_kg_FM: two-sigma counting error for K-40_FM.
  - MDA_K-40_Bq_per_kg_FM: minimum detectable activity for K-40 in FM.
  - Cs-137_Bq_per_kg_DM: Cs-137 activity in dry mass (Bq/kg_DM).
  - Counting_Error_Cs-137_Bq_per_kg_DM: two-sigma counting error for Cs-137_DM.
  - Cs-137_<: < marker indicating concentration below MDA in DM.
  - MDA_Cs-137_Bq_per_kg_DM: MDA for Cs-137 in DM.
  - Cs-137_Bq_per_kg_FM: Cs-137 activity in fresh mass (Bq/kg_FM).
  - Counting_Error_Cs-137_Bq_per_kg_FM: two-sigma counting error for Cs-137_FM.
  - Cs-137_<: < marker indicating concentration below MDA in FM.
  - MDA_Cs-137_Bq_per_kg_FM: MDA for Cs-137 in FM.
- Concentration ratios
  - Cs-137_Concentration_Ratio_Fungi_FM: fungus/fungi ratio of Cs-137 in FM relative to soil Cs-137 in FM.
  - Cs-137_Concentration_Ratio_Fungi_DM: fungus/soil ratio for Cs-137 in DM.
  - CR_Notes: notes on concentration ratio interpretation.
- General notes
  - General_Notes: miscellaneous notes about the dataset.

## Data Quality and Considerations
- Presence of < values (MDA markers) requires careful interpretation when using data for quantitative analysis.
- Some fields contain n/a placeholders, indicating missing or not-applicable data.
- Data spans multiple sites and potentially multiple fungal species; harmonisation may be needed for cross-dataset comparisons.
- Mass basis (DM vs FM) and corresponding units must be aligned when aggregating or comparing measurements.

## Potential Data Products and Insights
- Dashboards and self-serve tables by:
  - Isotope (K-40 vs Cs-137) and mass basis (DM vs FM).
  - Site, sample, and Latin species name (fungus type).
  - Comparison of fungal versus soil contamination via concentration ratios.
- Pivot analyses:
  - Activity concentrations by site, species, and date.
  - Ratios of Cs-137 in fungi versus soil across samples.
  - Distribution of MDAs and measurement uncertainties (counting errors).
- Data quality checks:
  - Flagging < values and missing data.
  - Verifying consistency between DM and FM measurements.

## Provenance and Scope
- Data provided with sample identifiers and radiochemical analyses by UKCEH Radiochemistry Laboratory.
- Part of the TREE_Northumbria_Gamma_Fungi data context, enabling exploration of fungal uptake of gamma-emitting radionuclides.