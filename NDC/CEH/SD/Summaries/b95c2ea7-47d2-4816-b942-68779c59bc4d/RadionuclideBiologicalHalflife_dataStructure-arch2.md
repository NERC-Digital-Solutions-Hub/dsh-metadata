# A database of radionuclide biological halflife values for wildlife

## Overview
- A data resource compiling radionuclide biological and ecological half-life values for wildlife.
- Created as part of the NERC Environmental Information Data Centre (2015) under Beresford et al.
- Contains metadata describing two related datasets: ecological half-life values (T1/2a, T1/2b) and biological half-life values (up to T1/2d) across wildlife and radionuclides.
- Intended to support standardized reporting, cross-study comparisons, and integration with other environmental monitoring data.
- Includes references to supporting information with full source details.

## Dataset structure and fields

### Ecological half-life dataset (Wildlife_ecological_halflife_metadata.csv)
- Entry_ID: Database ID code.
- Organism_name_common_English: Common English name of the organism.
- Organism_name_Latin: Latin scientific name.
- IAEA TRS wildlife group: Wildlife categorisation compatible with IAEA (2014).
- Organism_dimensions_Length_m: Length of the organism (m).
- Live_weight_kg: Live weight (kg).
- Radionuclide: Radionuclide or element studied.
- Compartment_whole organism_specific tissue: Tissue studied.
- Study_information: Information on the type of study.
- Length_of_study_days: Study duration (days).
- Temperature_degrees_Centigrade: Temperature during study (°C).
- Ecological_half-life_days_T1/2a: Ecological half-life for the first loss component (days).
- Ecological_half-life_days_T1/2b: Ecological half-life for the second loss component (days).
- Reference: Source reference (see supporting information for full details).
- Notes: Any relevant notes from source references.

### Biological half-life dataset (Wildlife_biological_halflife_metadata.csv)
- Entry_ID: Database ID code.
- Organism_name_common_English: Common English name of the organism.
- Organism_name_Latin: Latin scientific name.
- Wildlife_group: Wildlife categorisation compatible with IAEA (2014).
- Ecosystem: Broad ecosystem type.
- Radionuclide: Radionuclide or element studied.
- Live_weight_kg: Live weight (kg).
- Developmental_stage: Developmental stage of the organism.
- Compartment: Tissue studied.
- Experiment_type: Type of study (usually administration methodology).
- Length_of_study_days: Study duration (days).
- Temperature_degrees_Centigrade: Temperature during study (°C).
- Biological_half-life_days_T1/2a: Biological half-life for first loss component (days).
- Biological_half-life_days_T1/2b: Biological half-life for second loss component (days).
- Biological_half-life_days_T1/2c: Biological half-life for third loss component (days).
- Biological_half-life_days_T1/2d: Biological half-life for fourth loss component (days).
- Fraction_released_during_process_a/b/c/d: Fraction of initial activity lost during each component (dimensionless).
- Measurement_interval_d: Interval between measurements (days).
- Changeover_time_t_days: Intersection time between first and second components on a log scale (days).
- Changeover_time_t2_days: Intersection time between second and third components on a log scale (days).
- Percentage_retained_at_time_t: Percentage of initial activity retained at time t.
- Time_t_days: Time at which the above percentage is observed (days).
- Organism_dimensions_Length_m/Width_m/Depth_m: Dimensions of the organism (m).
- Sex: Organism sex.
- Elimination_rate_per_day: Rate of radionuclide elimination (per day).
- Reference: Source reference (see supporting information for full reference details).
- Notes: Any relevant notes from source references.

## Common metadata concepts and data quality
- Entry_ID functions as a unique identifier for each record across both datasets.
- Standardised organism descriptors (common name and Latin name) facilitate cross-study aggregation.
- Taxonomic and ecological context (wildlife group, ecosystem) support stratified analyses.
- Radionuclide-specific fields enable comparison of different radionuclides across species and tissues.
- Study-related fields (length, temperature, compartment, experiment type) provide context for interpreting half-life values.
- References and notes point to source literature and any caveats or clarifications.

## Data use for environmental monitoring and analysis
- Enables consistent assessment of radionuclide behaviour in wildlife populations over time.
- Supports categorisation and comparison of ecological and biological half-lives across species, tissues, and conditions.
- Facilitates quality assurance by documenting study design and measurement parameters.
- Can be integrated with other environmental datasets to evaluate ecosystem exposure and health against regulatory or policy standards.
- Intended to be stored and uploaded to appropriate data portals to support transparency and reuse.

## Access, quality, and dissemination considerations
- Data are drawn from established sources, with metadata designed to aid verification and reproducibility.
- Standardised field definitions support automated analysis workflows and cross-dataset queries.
- Key challenges for analysts include enhancing the value of these datasets through integration with additional environmental data and ensuring easy access to underlying data used to generate the outputs.
- Full reference details are provided in the linked supporting information (Ecological_halflife_references.rtf and Biological_halflife_references.rtf).