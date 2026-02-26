# TREE_Northumbria_Gamma_Soil

## Purpose and context
- Dataset of soil radiochemistry measurements from UKCEH Radiochemistry Laboratory.
- Supports environmental monitoring by recording activity concentrations of K-40 and Cs-137 in soil, enabling assessment of environmental radioactivity over time.

## Key identifiers and metadata
- CEH_Sample_Identifier: UKCEH unique sample identifier.
- CEH_Sample_Description: description of the sample.
- Site: sampling site.
- Sampling_Date_Used_As_Decay_Date: date used as the decay date for calculations.
- Mass_of_Sample_Analysed_g: mass of the sample analysed (in grams).
- Fresh_Mass_Dry_Mass_Ratio: ratio of fresh mass to freeze-dried mass.

## Measurements and units
- K-40_Bq_per_kg_DM: activity concentration of potassium-40 in Bq per kg dry mass at the sampling day.
- Counting_Error_K-40_Bq_per_kg_DM: two-sigma counting error for K-40.
- K-40_<: indicator that the reported value is below the MDA (minimum detectable activity).
- MDA_K-40_Bq_per_kg_DM: minimum detectable activity concentration for K-40 in Bq/kg dry mass.

- Cs-137_Bq_per_kg_DM: activity concentration of cesium-137 in Bq per kg dry mass.
- Counting_Error_Cs-137_Bq_per_kg_DM: two-sigma counting error for Cs-137.
- Cs-137_<: indicator that the reported value is below the MDA.
- MDA_Cs-137_Bq_per_kg_DM: minimum detectable activity concentration for Cs-137 in Bq/kg dry mass.

## Data quality, handling, and interpretation
- “Not measured” indicates the activity concentration was below the MDA.
- “<” markers denote concentrations below the specified MDA values.
- Data are measured and reported in Bq per kg dry mass, standardised for comparability.

## Data management and outputs
- Data should be stored and uploaded to the appropriate portals.
- Outputs from the dataset can be used in reports, maps, and charts for transparent presentation of environmental radiochemical status.

## How this supports environmental monitoring (Analysts perspective)
- Provides a standardised, auditable dataset for environmental radiochemistry, allowing monitoring of K-40 and Cs-137 against standards over time.
- Facilitates verification of environmental health and policy performance through clear metadata, quality assurance, and explicit measurement uncertainties.
- Enables trend analysis and spatial-temporal comparisons when combined with other monitoring data.

## Key challenges and opportunities
- Increasing the value of the datasets by integrating with other relevant data sources (avoiding single-use data).
- Ensuring easy access to underlying data used to generate final outputs for broader use and scrutiny.