# A database of radionuclide biological halflife values for wildlife

- This document describes the data structure for the Beresford et al. (2015) database of radionuclide biological half-life values for wildlife, hosted by the NERC Environmental Information Data Centre. It specifies two metadata CSV files that define the fields, descriptions, units, and semantics used to catalogue ecological and biological half-life study data.

## Metadata file: Wildlife_ecological_halflife_metadata.csv

- Key fields and semantics
  - Entry_ID: Database ID code
  - Organism_name_common_English / Organism_name_Latin: Common and Latin names
  - IAEA TRS wildlife group: Wildlife categorisation aligned with IAEA (2014)
  - Organism_dimensions_Length_m, Live_weight_kg: Size and weight descriptors
  - Radionuclide: Studied radionuclide/element
  - Compartment_whole organism_specific tissue: Tissue or organ studied
  - Study_information: Type of study / methodological notes
  - Length_of_study_days, Temperature_degrees_Centigrade: Study duration and ambient temp
  - Ecological_half_life_days_T1/2a, Ecological_half_life_days_T1/2b: Ecological half-life components
  - Reference: Source reference (see supporting information for full details)
  - Notes: Additional context or caveats

- Purpose
  - Provides the metadata schema to describe ecological half-life studies, enabling consistent understanding of study design, tissue compartments, and loss components.

## Metadata file: Wildlife_biological_halflife_metadata.csv

- Key fields and semantics
  - Entry_ID: Database ID code
  - Organism_name_common_English / Organism_name_Latin: Common and Latin names
  - Wildlife_group, Ecosystem: Wildlife categorisation and ecosystem context
  - Radionuclide: Studied radionuclide/element
  - Live_weight_kg, Organism_dimensions_Length_m / Width_m / Depth_m: Size descriptors
  - Developmental_stage, Sex: Biological state of the organism
  - Compartment: Tissue studied
  - Experiment_type: Type of study (e.g., administration methodology)
  - Length_of_study_days, Temperature_degrees_Centigrade: Study duration and ambient temp
  - Biological_half_life_days_T1/2a, T1/2b, T1/2c, T1/2d: Biological half-life components
  - Fraction_released_during_process_a/b/c/d: Proportion lost in each component
  - Measurement_interval_d: Interval between measurements
  - Changeover_time_t_days, Changeover_time_t2_days: Intersections of half-life components on log scale
  - Percentage_retained_at_time_t, Time_t_days: Retention metrics over time
  - Elimination_rate_per_day: Rate of elimination (per day)
  - Reference: Source reference (see supporting information for full details)
  - Notes: Additional context or caveats

- Purpose
  - Documents the metadata required to describe biological half-life studies, including multiple loss components, measurement schedules, and retention dynamics.

## Data governance and stewardship implications

- Standardization and interoperability
  - Use of consistent field names, descriptions, and units to enable cross-study comparability.
  - Alignment with IAEA wildlife grouping to facilitate taxonomy compatibility.

- Provenance and references
  - Each entry links to original references; full reference details are provided in supporting information files referenced by the metadata.

- Data quality and completeness
  - Metadata fields define required descriptors (names, weights, tissue/compartment, study type, durations, temperatures, half-life components, fractions, measurements, retention, and elimination rates).
  - Encourages complete metadata capture by data creators to support discoverability and reuse.

- Versioning, updates, and sharing
  - Clear documentation of study information, updates, and notes supports traceability and data updates.
  - Datasets can be uploaded to appropriate portals and catalogues with consistent metadata.

- User needs and discoverability
  - Metadata captures key descriptors (organism, radionuclide, tissue, life stage, ecosystem) to support filtering, discovery, and reuse by data users and decision-makers.

## How this aligns with the Data Stewards archetype

- Enables reliable data governance for large datasets by providing a clear metadata structure that ensures accurate description, discoverability, and interoperability.
- Supports data creators in meeting standards for metadata, units, and provenance.
- Facilitates sharing while respecting references and notes, and documents updates or embargo considerations via described fields and supporting information links.
- Aids in handling diverse systems and formats by defining a consistent schema for ecological and biological half-life data.