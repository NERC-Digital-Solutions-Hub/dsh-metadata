# A database of radionuclide biological halflife values for wildlife

## Overview
- Describes the data structure for a database of radionuclide biological halflife values for wildlife (Ber esford et al., 2015; NERC Environmental Information Data Centre).
- Two metadata tables accompany the dataset:
  - Wildlife_ecological_halflife_metadata.csv
  - Wildlife_biological_halflife_metadata.csv
- Purpose: facilitate data discovery, consistency, comparability across studies, and transparent data provenance for environmental radiological monitoring and framework development.
- Each metadata entry includes clear field definitions, units, and descriptive notes, with references to source materials (and links to full references in supporting information).

## Wildlife ecological half-life metadata.csv
- Entry_ID: Database ID code for the record.
- Organism_name_common_English / Organism_name_Latin: Common and Latin names of the organism.
- IAEA TRS wildlife group: Wildlife categorisation aligned with IAEA (2014).
- Ecosystem: Broad ecosystem type.
- Live_weight_kg: Organism live weight.
- Radionuclide: Studied radionuclide or element.
- Compartment_whole organism_specific tissue: Tissue studied (whole organism or specific tissue).
- Study_information: Details on the study type and context.
- Length_of_study_days: Duration of the study (days).
- Temperature_degrees_Centigrade: Temperature during the study (°C).
- Ecological_half_life_days_T1/2a / Ecological_half_life_days_T1/2b: Ecological half-lives for the first and second loss components (days).
- Reference: Source reference (see supporting information for full details).
- Notes: Relevant notes from source references.

## Wildlife biological half-life metadata.csv
- Entry_ID: Database ID code for the record.
- Organism_name_common_English / Organism_name_Latin: Common and Latin names of the organism.
- Wildlife_group: Wildlife categorisation compatible with IAEA (2014).
- Ecosystem: Broad ecosystem type.
- Radionuclide: Studied radionuclide or element.
- Live_weight_kg: Organism live weight.
- Developmental_stage: Developmental stage of the organism.
- Compartment: Tissue studied.
- Experiment_type: Type of study (usually administration methodology).
- Length_of_study_days: Study duration (days).
- Temperature_degrees_Centigrade: Temperature during the study (°C).
- Biological_half_life_days_T1/2a / T1/2b / T1/2c / T1/2d: Biological half-lives for up to four components (days).
- Fraction_released_during_process_a / b / c / d: Fraction of initial activity lost during each component (dimensionless).
- Measurement_interval_d: Number of measurements during the study; interval between measurements (days).
- Changeover_time_t_days / Changeover_time_t2_days: Intersections of successive half-life components on a log scale (days).
- Percentage_retained_at_time_t: Percentage of initial activity retained at a given time.
- Time_t_days: Time at which the above percentage is observed (days).
- Organism_dimensions_Length_m / Width_m / Depth_m: Physical dimensions of the organism.
- Sex: Organism sex.
- Elimination_rate_per_day: Rate of elimination of radionuclide/element (per day).
- Reference: Source reference (see supporting information for full reference details).
- Notes: Any relevant notes from source references.

## Data provenance and references
- Primary source: Beresford, N.A. et al. (2015). A database of radionuclide biological halflife values for wildlife.
- Repository: NERC Environmental Information Data Centre.
- Supporting information includes full reference details (Biological_halflife_references.rtf and Ecological_halflife_references.rtf).

## Implications for monitoring frameworks
- The metadata structure supports standardized data collection and reporting across species, radionuclides, and study designs.
- Facilitates data quality assurance, metadata completeness, and provenance tracking essential for governance.
- Enables robust cross-study comparisons for environmental health monitoring and policy evaluation.
- Highlights the need for accessible data, consistent units, and clear documentation to overcome common barriers (data gaps, access, silos, and metadata inadequacies).