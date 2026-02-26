# A database of radionuclide biological halflife values for wildlife

## Overview
- Describes the data structure for a database of radionuclide biological and ecological half-life values for wildlife (2015).
- Based on Beresford et al. (2015) and hosted at the NERC Environmental Information Data Centre.
- Includes two metadata CSV files detailing the fields, descriptions, and units used in the underlying data tables.

## Data structure (metadata files)
- Wildlife_ecological_halflife_metadata.csv
  - Key fields include: Entry_ID, Organism_name_common_English, Organism_name_Latin, IAEA TRS wildlife group, Organism_dimensions_Length_m, Live_weight_kg, Radionuclide, Compartment_whole organism_specific tissue, Study_information, Length_of_study_days, Temperature_degrees_Centigrade, Ecological_half-life_days_T1/2a, Ecological_half-life_days_T1/2b, Reference, Notes.
  - Each field has a Description and Units (where applicable; some fields are n/a).
  - Captures ecological half-life information (T1/2a and T1/2b) and contextual metadata for the study.

- Wildlife_biological_halflife_metadata.csv
  - Key fields include: Entry_ID, Organism_name_common_English, Organism_name_Latin, Wildlife_group, Ecosystem, Radionuclide, Live_weight_kg, Developmental_stage, Compartment, Experiment_type, Length_of_study_days, Temperature_degrees_Centigrade, Biological_half-life_days_T1/2a, Biological_half-life_days_T1/2b, Biological_half-life_days_T1/2c, Biological_half-life_days_T1/2d, Fraction_released_during_process_a-d, Measurement_interval_d, Changeover_time_t_days, Changeover_time_t2_days, Percentage_retained_at_time_t, Time_t_days, Organism_dimensions_Length_m, Width_m, Depth_m, Sex, Elimination_rate_per_day, Reference, Notes.
  - Each field includes a Description and Units (where applicable).
  - Documents biological half-life components (T1/2a–T1/2d), transfer dynamics, and related measurement context.

## How this supports GIS work
- Provides standardized attributes for wildlife and radionuclides that can be joined to spatial data (species distributions, habitats, ecosystems).
- Enables mapping of:
  - Species-specific traits (weight, size, developmental stage, sex) as covariates in spatial models.
  - Environmental contexts (ecosystem type, temperature) relevant to radionuclide retention and transfer.
  - Radionuclide-specific half-life parameters and tissue compartments for spatial risk assessments.
- Clear units and field descriptions facilitate correct data scaling and integration with other GIS layers.

## Practical considerations for GIS specialists
- Ensure consistent data standards across datasets and harmonize units (e.g., kg, m, d, °C) before analysis.
- Use Entry_ID to link these metadata fields to the corresponding study records in spatial analyses.
- Be mindful of context-dependent values (ecological vs biological half-lives; temperature and tissue studied) when modeling across landscapes.
- Leverage Reference and Notes for traceability and to understand study-specific conditions.

## Access and references
- Original dataset: Beresford, N.A. et al. (2015). A database of radionuclide biological halflife values for wildlife. NERC Environmental Information Data Centre. DOI: http://doi.org/10.5285/b95c2ea7-47d2-4816-b942-68779c59bc4d
- Supporting references:
  - Ecological_halflife_references.rtf (for ecological half-life references)
  - Biological_halflife_references.rtf (for biological half-life references)