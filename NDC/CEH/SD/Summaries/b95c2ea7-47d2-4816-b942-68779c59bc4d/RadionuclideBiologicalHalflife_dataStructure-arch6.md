# A database of radionuclide biological halflife values for wildlife

## Overview
- Compiles a database of radionuclide biological half-life values for wildlife, drawing from Beresford et al. (2015) and hosted by the NERC Environmental Information Data Centre.
- Defines metadata schemas for two related datasets: ecological half-lives and biological half-lives across wildlife species and radionuclides.
- Aims to support data discovery, verification, transformation, and reuse for analysis and policy-relevant work.

## Data structure and purpose (Data Support perspective)
- Provides structured metadata to describe each entry (database IDs, organisms, radionuclides, tissues, study details, and references).
- Enables researchers to locate and compare half-life estimates across species, ecosystems, and study conditions.
- Facilitates data cleaning, transformation, and combination into user-friendly products (e.g., dashboards, pivot tables) for end users to self-serve analyses.
- Includes guidance on data provenance (references) and notes to support quality assurance and future updates.

## Wildlife_ecological_halflife_metadata.csv
- Entry_ID: Database ID code.
- Organism_name_common_English / Organism_name_Latin: Common and Latin names of the organism.
- IAEA TRS wildlife group: Wildlife categorisation compatible with IAEA systems.
- Organism_dimensions_Length_m / Live_weight_kg: Physical attributes of the organism.
- Radionuclide: The radionuclide or element studied.
- Compartment_whole organism_specific tissue: Tissue/compartment studied within the whole organism.
- Study_information: Context and type of study.
- Length_of_study_days: Duration of the ecological study.
- Temperature_degrees_Centigrade: Temperature during the study (where noted).
- Ecological_half_life_days_T1/2a / Ecological_half_life_days_T1/2b: Ecological half-life components (two loss components) in days.
- Reference: Source reference (full details in supporting information).
- Notes: Additional notes from sources.

## Wildlife_biological_halflife_metadata.csv
- Entry_ID: Database ID code.
- Organism_name_common_English / Organism_name_Latin: Common and Latin names of the organism.
- Wildlife_group / Ecosystem: Wildlife categorisation and ecosystem type.
- Radionuclide: The radionuclide or element studied.
- Live_weight_kg: Organism live weight.
- Developmental_stage / Sex: Biological characteristics of the organism.
- Compartment: Tissue studied.
- Experiment_type: Type of study (e.g., administration methodology).
- Length_of_study_days: Study duration.
- Temperature_degrees_Centigrade: Temperature during the study.
- Biological_half-life_days_T1/2a / T1/2b / T1/2c / T1/2d: Biological half-life components (up to four components) in days.
- Fraction_released_during_process_a / b / c / d: Fraction of initial activity released during each component.
- Measurement_interval_d: Interval between measurements within the study.
- Changeover_time_t_days / Changeover_time_t2_days: Intersections of regression lines on a log scale for successive half-lives.
- Percentage_retained_at_time_t / Time_t_days: Retention metrics at specified times.
- Organism_dimensions_Length_m / Width_m / Depth_m: Body dimensions.
- Sex: Organism sex.
- Elimination_rate_per_day: Rate of elimination of radionuclide per day.
- Reference: Source reference (full details in supporting information).
- Notes: Additional notes from sources.

## Data quality, access, and reuse considerations
- Data may be patchy and come from diverse formats and systems; requires careful data cleaning and harmonisation.
- Verification with topic experts is advisable when combining different study types or units.
- References point to supporting information for full citation details; provenance supports traceability and reproducibility.
- Outputs (dashboards, reports) should include clear unit conventions and data lineage to promote reuse and reduce misinterpretation.

## How this supports data work in practice
- Enables discovery of wildlife radionuclide half-life data across ecological and biological contexts.
- Supports building data products that allow end users to explore and compare half-life estimates without needing deep data wrangling.
- Encourages transparency and re-use by documenting study contexts, methodologies, and references.
- Provides a foundation for advocating better data creation and standardisation in future research.