# A database of radionuclide biological halflife values for wildlife

## Overview
- A structured database of radionuclide biological half-life values for wildlife, supporting ecological and biological half-life analyses.
- Based on Beresford et al. (2015) and hosted in the NERC Environmental Information Data Centre.
- Includes two metadata CSV files that describe the structure, fields, and meanings of records for ecological and biological half-life data, with references to full sources.

## Data structure and contents

- Wildlife_ecological_halflife_metadata.csv
  - Core fields include: Entry_ID, Organism_name_common_English, Organism_name_Latin, IAEA TRS wildlife group, Organism_dimensions_Length_m, Live_weight_kg, Radionuclide, Compartment_whole organism_specific tissue, Study_information, Length_of_study_days, Temperature_degrees_Centigrade, Ecological_half-life_days_T1/2a, Ecological_half-life_days_T1/2b, Reference, Notes.
  - Captures ecological half-life components and study context for the whole organism or specific tissues.

- Wildlife_biological_halflife_metadata.csv
  - Core fields include: Entry_ID, Organism_name_common_English, Organism_name_Latin, Wildlife_group, Ecosystem, Radionuclide, Live_weight_kg, Developmental_stage, Compartment, Experiment_type, Length_of_study_days, Temperature_degrees_Centigrade, Biological_half-life_days_T1/2a, Biological_half-life_days_T1/2b, Biological_half-life_days_T1/2c, Biological_half-life_days_T1/2d, Fraction_released_during_process_a/b/c/d, Measurement_interval_d, Changeover_time_t_days, Changeover_time_t2_days, Percentage_retained_at_time_t, Time_t_days, Organism_dimensions_Length_m/Width_m/Depth_m, Sex, Elimination_rate_per_day, Reference, Notes.
  - Documents biological half-life values across multiple loss components and the related modeling/experimental details.

- Both metadata files include units specifications, reference pointers, and notes to aid data traceability and reuse.

## Key fields and their purpose
- Organism and taxonomy fields (common name, Latin name, wildlife group) enable cross-species comparisons.
- Radionuclide field specifies the studied radionuclide or element.
- Biological vs ecological halves:
  - Ecological half-lives: T1/2a, T1/2b (two-component loss modeling for the whole organism or tissue).
  - Biological half-lives: up to T1/2d (four potential loss components) with associated fractions released (a–d) and changeover times.
- Study context: study length, temperature, development stage, compartment studied, experiment type, and measurement intervals.
- Temporal and dose-related details: Time_t_days, Percentage_retained_at_time_t, Changeover_time_t_days, Changeover_time_t2_days, Elimination_rate_per_day.
- Physical attributes: live weight and organism dimensions (Length, Width, Depth).
- Quality and provenance: Reference field with source citations; Notes for study-specific caveats.

## Source and access
- Source: Beresford, N.A. et al. (2015), A database of radionuclide biological halflife values for wildlife.
- Repository: NERC Environmental Information Data Centre.
- Full references available in supporting information linked to the dataset.

## How analysts can use this data
- Identify correlations between ecological/biological half-lives and organism traits (weight, size, ecosystem) and radionuclide properties.
- Build predictive models of half-life by species, tissue, and temperature, using multi-component (two to four) loss frameworks.
- Compare ecological half-lives (environment-driven depletion) with biological half-lives (internal/body processing) across taxa.
- Conduct meta-analyses or data integration by harmonizing units and metadata using the provided fields and references.
- Track data provenance and replicate analyses by citing the Reference fields and notes; leverage measurement intervals and changeover times for model validation.

## Data quality, standards, and challenges (analyst perspective)
- Data may vary in scale, locality, and completeness; careful alignment of units and taxonomic names is essential.
- Heterogeneous study designs (compartment choices, administration methods, temperatures) require careful harmonization for cross-study comparisons.
- Access to underlying datasets and exact study details is mediated by references and supporting information; ensure proper sourcing when aggregating.
- Potential gaps at local or finer scales; some data may be dispersed across sources or within the supporting information.