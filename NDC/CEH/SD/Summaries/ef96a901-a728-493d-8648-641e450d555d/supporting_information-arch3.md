# Phenotypic data collected in the experimental infection study of house finches with M. gallisepticum bacterial isolates

## Purpose and scope
- Provides phenotypic data from an experimental infection study to investigate adaptive phenotypic plasticity in a host–pathogen system.
- Aims to test how plasticity influences infection dynamics and contributes to evolution, using a unique repository of M. gallisepticum isolates across an epizootic outbreak.

## Data Access and Citation
- Data are available under the Open Government Licence.
- Access: https://doi.org/10.5285/ef96a901-a728-493d-8648-641e450d555d
- Citation: Bonneaud, C. (2019). Phenotypic data collected in the experimental infection study of house finches with M. gallisepticum bacterial isolates. NERC Environmental Information Data Centre. https://doi.org/10.5285/ef96a901-a728-493d-8648-641e450d555d

## Background and Rationale
- Phenotypic plasticity enables organisms to adjust phenotypes to environmental conditions; believed to influence adaptation and evolution.
- Pathogen plasticity in replication and transmission in response to host defenses is underexplored.
- Uses a long-term pathogen isolate collection from wild house finch epidemics to address how plasticity relates to evolution in infection dynamics.

## Study Design and Methods
- Ethics: Approvals from IACUCs (Auburn University, Arizona State University) and institutional biosafety/authorizations.
- Subjects: Wild house finches (N=171; 93 males, 78 females) captured in Arizona and Alabama; birds acclimated in two aviaries.
- Infection: 53 birds from Alabama and 59 from Arizona inoculated with 1 of 56 M. gallisepticum isolates (spanning 1994–2015) via 20 μL eye inoculation.
- Procedures:
  - Pre-screening for absence of prior M. gallisepticum infection.
  - Random assignment to isolates; birds housed in pairs for inoculated subjects.
  - Monitoring of clinical signs, body mass, and pathogen metrics over time.
  - Euthanasia at study end per licensing.
- Data collection included serology, PCR for infection status, and confirmation of isolate growth; isolates stored with glycerol at -80°C.

## Measurements and Data Collected
- Clinical phenotype: eye lesion severity in both eyes (0–5 scale) at multiple days post-inoculation (3, 6, 8, 14, 21, 25, 28, 34).
- Morphometrics: body mass at -7, 0, 3, 8, 14, 21, 28, 34 days relative to inoculation.
- Pathogen detection and load:
  - Conjunctival/tracheal swabs for M. gallisepticum DNA by PCR (infection status).
  - Quantitative PCR to measure pathogen load (MG load) at days 8, 14, 21, 28.
  - Non-infected controls tested with PCR at multiple timepoints.
- Time-resolved data points include both infected and non-infected birds, enabling longitudinal analyses of plastic responses.

## Data Structure and Variables
- Key identifiers: Unique bird ID; population origin (AO: Auburn/Opelika; GT: Greater Tempe); sex; pathogen isolate year.
- Phenotypic measures across time:
  - Mass_d-7, Mass_0, Mass_d3, Mass_d8, Mass_d14, Mass_d21, Mass_d28, Mass_d34 (grams).
  - Eye lesion scores for right/left eyes at multiple days (e.g., RE_score.d3, LE_score.d3, etc. up to d34; scale 0–5).
- Infection metrics:
  - MG_PCR_d8, MG_PCR_d14, MG_PCR_d21, MG_PCR_d28 (0 = no, 1 = yes).
  - Pload_8, Pload_14, Pload_21, Pload_28 (cell copies; MG load).
  - PCR_2t … PCR_35t (PCR status for non-infected birds at various days; 0 = no, 1 = yes).
- Data notes:
  - Missing measurements indicated; data types and units specified for each variable.
  - Comprehensive data dictionary accompanies the dataset.

## Data Governance and Reuse
- Encourages open data use with clear licensing and citation requirements.
- Study conducted under established ethics approvals and data quality practices (screening, standardised scoring, and molecular assays).
- Metadata and data dictionaries are provided to facilitate verification, transformation, and integration for monitoring and policy-relevant analyses.

## References
- Luttrell et al. (1996); Roberts et al. (2001, 2001); Kollias et al. (2004) – foundational methods and context cited for infection and phenotypic assessment.