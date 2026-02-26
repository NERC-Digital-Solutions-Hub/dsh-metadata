# A database of radionuclide biological halflife values for wildlife

## Overview
- Describes the data structure for the Beresford et al. (2015) database of radionuclide biological half-life values in wildlife, hosted in the NERC Environmental Information Data Centre.
- The dataset comprises two metadata tables that define ecological and biological half-life data and their associated fields, units, and references.

## Data structure

- Wildlife_ecological_halflife_metadata.csv
  - Entry_ID: Database ID code
  - Organism_name_common_English: Common English name
  - Organism_name_Latin: Latin name
  - IAEA TRS wildlife group: Wildlife categorisation aligned with IAEA (2014)
  - Organism_dimensions_Length_m: Length of organism
  - Live_weight_kg: Live weight
  - Radionuclide: Radionuclide studied
  - Compartment_whole organism_specific tissue: Tissue studied
  - Study_information: Type/info of study
  - Length_of_study_days: Study duration
  - Temperature_degrees_Centigrade: Temperature during study
  - Ecological_half_life_days_T1/2a: Ecological half-life for first loss component
  - Ecological_half_life_days_T1/2b: Ecological half-life for second loss component
  - Reference: Source reference (see supporting information for full details)
  - Notes: Any relevant notes

- Wildlife_biological_halflife_metadata.csv
  - Entry_ID: Database ID code
  - Organism_name_common_English: Common English name
  - Organism_name_Latin: Latin name
  - Wildlife_group: Wildlife categorisation (IAEA 2014)
  - Ecosystem: Broad ecosystem type
  - Radionuclide: Radionuclide studied
  - Live_weight_kg: Live weight
  - Developmental_stage: Developmental stage
  - Compartment: Tissue studied
  - Experiment_type: Type of study (e.g., administration method)
  - Length_of_study_days: Study duration
  - Temperature_degrees_Centigrade: Temperature during study
  - Biological_half_life_days_T1/2a: Biological half-life for first loss component
  - Biological_half_life_days_T1/2b: Biological half-life for second loss component
  - Biological_half_life_days_T1/2c: Biological half-life for third loss component
  - Biological_half_life_days_T1/2d: Biological half-life for fourth loss component
  - Fraction_released_during_process_a: Fraction released during first process
  - Fraction_released_during_process_b: Fraction released during second process
  - Fraction_released_during_process_c: Fraction released during third process
  - Fraction_released_during_process_d: Fraction released during fourth process
  - Measurement_interval_d: Number of measurements between observations
  - Changeover_time_t_days: Intersection time of first and second biological half-lives (log scale)
  - Changeover_time_t2_days: Intersection time of second and third biological half-lives (log scale)
  - Percentage_retained_at_time_t: Percentage of initial activity retained at time t
  - Time_t_days: Time at which Percentage_retained_at_time_t is observed
  - Organism_dimensions_Length_m: Length of organism
  - Organism_dimensions_Width_m: Width of organism
  - Organism_dimensions_Depth_m: Depth of organism
  - Sex: Organism sex
  - Elimination_rate_per_day: Rate of elimination (per day)
  - Reference: Source reference (see supporting information for full details)
  - Notes: Any relevant notes

## Relevance for data leadership

- End-to-end data governance
  - Clear metadata definitions enable discoverability, data quality assessment, and reuse across studies.
  - Explicit field-level descriptions (units, tissue, study information, references) support provenance and traceability.
- Standardization and interoperability
  - Alignment with IAEA wildlife group taxonomy (IAEA TRS 2014) facilitates cross-referencing with other datasets.
  - Common core fields (e.g., Organism, Radionuclide, weight, temperature, study duration) support aggregation and comparative analyses.
- Research usability and stewardship
  - Metadata supports understanding study conditions (temperature, developmental stage, tissue/compartment) critical for reproducibility.
  - References point to full source material (Ecological_halflife_references.rtf, Biological_halflife_references.rtf) and primary publication (Beresford et al., 2015).
- Data quality and lifecycle considerations
  - The two-table structure distinguishes ecological and biological half-life data, clarifying data origin and application contexts.
  - Fields related to measurements, changeover times, and fractions released enable nuanced modeling of loss processes.

## Practical considerations for implementation

- Data discovery and access
  - Ensure metadata fields are populated consistently to aid filtering and searchability within data catalogs.
- Data quality and standards
  - Maintain unit consistency, keep taxonomy aligned with IAEA categories, and preserve provenance through references.
- Gaps and coordination
  - Recognize potential data gaps in granularity or in certain species/radionuclides; consider community data standards to improve coordination across studies.

## Why this matters for a Data Leader

- Demonstrates a robust metadata-focused data model designed for cross-study integration, governance, and reuse.
- Provides a concrete example of structuring complex, multi-component biological data (ecological and biological half-lives) with clear provenance and study context.
- Highlights the importance of referencing supporting information and maintaining standardized classifications to enable collaboration across data networks.