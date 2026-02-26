# TREE_Northumbria_Gamma_Deer

## Overview
- Dataset describing Cs-137 radiochemical measurements in Roe deer tissue as part of monitoring environmental radiological contamination.
- Reflects standardized data capture and reporting processes used by environmental monitoring programs.

## Data structure and key fields
- Species and sample identifiers:
  - Latin_Species_Name: Latin name of the species (Roe deer).
  - CEH_Sample_description: UKCEH sample description.
  - CEH_Sample_code: UKCEH Radiochemistry Laboratory unique sample identifier.
- Sample specifics:
  - Tissue: Tissue type analysed (Roe deer tissue).
  - Site: Sampling site.
  - Fresh_Mass_Of_Sample_Analysed_g: Fresh mass of sample in grams.
  - Sampling_date_Used_As_Decay_date: Date the sample was taken and used as its decay date.
- Measurement data:
  - Cs-137_Bq_per_kg_FM: Activity concentration of Cs-137 in Bq/kg fresh mass.
  - Counting_Error_Cs-137_Bq_per_kg_DM: Two-sigma counting error for Cs-137 in Bq/kg dry mass.
  - MDA_Cs-137_Bq_per_kg_FM: Minimum detectable activity concentration in Bq/kg fresh mass.
  - Cs-137_Concentration_Ratio_FM: Cs-137 concentration ratio (fresh mass activity in muscle / soil dry mass activity).
  - Cs-137_<: Indicator for values reported as less than the stated MDA.
  - CR_Notes: Notes related to concentration ratio.
- General metadata:
  - Units fields indicate measurement units (e.g., Bq per kg FM or DM). Several fields are marked n/a where not applicable.

## Data quality, measurement details, and interpretation
- Units specified for key measurements:
  - Fresh mass and activity: Bq per kg fresh mass (FM).
  - Dry mass: Bq per kg dry mass (DM).
- Data flags and limits:
  - MDA fields indicate the minimum detectable activity.
  - “<” markers denote concentrations below the detection limit, paired with MDA values.
- Measurement reliability:
  - Counting error captured as two-sigma uncertainty for Cs-137 in dry mass.
- Ratios:
  - Cs-137 Concentration Ratio (FM) compares muscle activity to soil dry mass activity.

## Provenance, processing, and storage
- Origin:
  - Data derived from UKCEH Radiochemistry Laboratory with a unique sample identifier.
- Processing:
  - Assumed standard QA, cleaning, and transformation procedures consistent with environmental monitoring practices.
- Outputs and formats:
  - Data intended for inclusion in standard outputs (reports, maps, charts) and storage/upload to appropriate data portals.

## Use in environmental monitoring
- Enables tracking of Cs-137 contamination in wildlife over time.
- Supports comparative analyses across sites and years by providing standardised activity concentrations and associated uncertainties.
- Facilitates assessment of environmental health and policy performance when integrated with broader monitoring datasets.

## Data sharing and accessibility
- Emphasises access to underlying data used to create final outputs.
- Designed for integration with other datasets and availability through monitoring portals or repositories.

## Key challenges and opportunities
- Increasing dataset value:
  - Combine Cs-137 deer data with other relevant environmental datasets to support broader analyses beyond single-use applications.
- Data accessibility:
  - Ensure underlying data remains accessible to researchers and policymakers to enhance scrutiny and reuse.