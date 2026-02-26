# TREE_Northumbria_Gamma_Soil

## Overview
- A soil gamma radiation dataset associated with UKCEH radiochemistry lab sample identifiers.
- Captures sample description, site, and date used as the decay date, plus mass measurements and ratios.
- Records activity concentrations for K-40 and Cs-137 in Bq per kilogram dry mass, including counting uncertainty and minimum detectable activity (MDA).
- Uses markers for values below MDA and notes when measurements were not taken.

## Key fields and data definitions
- CEH_Sample_Identifier: UKCEH Radiochemistry Laboratory unique sample identifier.
- CEH_Sample_Description: UKCEH sample description.
- Site: Sampling site.
- Mass_of_Sample_Analysed_g: Mass of the sample analysed (grams).
- Sampling_Date_Used_As_Decay_Date: Date the sample was taken and used as the decay date.
- Fresh_Mass_Dry_Mass_Ratio: Ratio of fresh mass to freeze-dried mass for the soil.
- K-40_Bq_per_kg_DM: Activity concentration of K-40 in Bq/kg dry mass at the day of sampling.
- Counting_Error_K-40_Bq_per_kg_DM: Two-sigma counting error for K-40 (Bq/kg DM).
- K-40_<: Marker indicating a concentration is below the MDA (not detected).
- MDA_K-40_Bq_per_kg_DM: Minimum detectable activity concentration for K-40 (Bq/kg dry mass).
- Cs-137_Bq_per_kg_DM: Activity concentration of Cs-137 in Bq/kg dry mass.
- Counting_Error_Cs-137_Bq_per_kg_DM: Two-sigma counting error for Cs-137 (Bq/kg DM).
- Cs-137_<: Marker indicating a concentration is below the MDA (not detected).
- MDA_Cs-137_Bq_per_kg_DM: Minimum detectable activity concentration for Cs-137 (Bq/kg dry mass).

## Measurements and units
- Isotopes measured: K-40 and Cs-137.
- Units:
  - Activity concentrations: Bq per kg dry mass (Bq/kg DM).
  - Mass: grams (g).
- Data handling:
  - Values may be reported as exact measurements or as "<" MDA values.
  - Not measured indicates activity concentration was below the respective MDA.

## Data quality and interpretation notes
- Two-sigma counting error reported for each isotope.
- "<" markers indicate concentrations below the MDA (not detected).
- "Not measured" indicates no measurement was recorded for that isotope at the time of analysis.
- Decay-date reference is tied to the sampling date used as the decay date.

## Practical usage for data support
- Data integration:
  - Harmonise units across records (Bq/kg DM, g, ratio).
  - Link CEH_Sample_Identifier with site and description metadata for context.
- Data quality considerations:
  - Handle "<" and "Not measured" values consistently in analyses and visualisations.
  - Consider MDA values when assessing detection capabilities across samples.
- Analytical workflow support:
  - Use mass and fresh/dry ratio to standardise activity concentrations to dry mass.
  - Use Sampling_Date_Used_As_Decay_Date to apply decay corrections if needed.
- Potential data challenges:
  - Patchy data across samples or sites.
  - Variability in data formats between records; ensure consistent field naming and units.