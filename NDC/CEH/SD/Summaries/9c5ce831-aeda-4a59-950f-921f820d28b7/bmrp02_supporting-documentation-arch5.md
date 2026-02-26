# Sampling regime and collection methods

## Overview
- Long-term study of a wild population of banded mongooses (Mungos mungo) on the Mweya Peninsula, Queen Elizabeth National Park, Uganda.
- Ongoing since 1995; typical groups 10–12 across distinct territories; groups ~20 adults plus offspring.
- Individual identification via fur shave marks (adults) or dye marks (pups); regular trapping every two months for mark maintenance.
- Most groups located using radio collars and observed by walking teams; data collected on group composition, life history, reproduction, and cooperative behavior.
- Reproduction is highly synchronized within groups; paternal and maternal assignments determined via genetic pedigree data.

## Study design and data scope
- Experimental manipulation: early-life provisioning of pregnant females to induce feeding vs. non-feeding controls.
- Split-plot design across 34 breeding attempts in 7 groups from 2013–2016.
- Provisioned females receive an average of 50 g egg per day (randomized across 0, 50, or 100 g and time of day) from 2–4 days after pregnancy confirmation until birth.
- Each manipulated breeding attempt followed by an unmanipulated control breeding attempt to ensure effects dissipate before next manipulation.
- Sample sizes: 101 fed female pregnancies and 97 non-fed pregnancies; resulting in 50 treatment pups and 50 control pups.
- Pedigree-based maternity assignments with 90% assignment probability.

## Data collection methods and timing
- Field data captured with a bespoke app (Mongoose 2000) on tablets; data imported into MS Access.
- Routine measurements include individual weights (weekly for pups; periodic for adults), reproductive status, escorting behavior, and social interactions.
- Pups are tagged and sampled for genetics; DNA genotyped with a 43-marker microsatellite panel.
- Pups begin escorting around 30 days old; focal follows and 20-minute observation blocks record feeding, escorting, and social interactions.
- Weight measurements obtained via portable scales; pups and adults are weighed during specified windows.

## Field instruments, calibration, and data integrity
- Instruments: data collection app (Mongoose 2000), Samsung Galaxy tablets, MS Access database; portable electronic scales; radio collars; ultrasound machines for pregnancy confirmation.
- Calibration: field instruments calibrated to factory settings.
- Data integrity: internal checks in Mongoose 2000; cross-validation and quality control using MS Access queries and bespoke R code to detect data inconsistencies (e.g., multiple death records).

## Experimental design and variables
- Experimental manipulations focus on provisioning status (fed vs. non-fed) of pregnant females; unmanipulated litters serve as controls.
- Key analytic variables include:
  - Female condition and weight changes: pre-pregnancy baseline, during pregnancy, post-pregnancy, and escorting period.
  - Escorting behavior: male and female escorting across the escorting period; proportion of visits with escorting.
  - Allocation of escorting to pups: escorting effort directed to each pup by fed vs. non-fed mothers and by sex of escort.
  - Pup growth and condition: pup weights, age at weighing, litter-level variance in weight, and relative within-litter variance.
  - Escorting rate and social dynamics: rate of escorting feeds per hour and proximity measures (nearest neighbour status).
  - Survival outcomes: survival to 90 days, 180 days, and 365 days, with end ages recorded where applicable.
- Data include both individual-level and dyadic relationships (e.g., relatedness between pups and adult escorts).

## Data structure and contents
- Data stored in 15 CSV files capturing a range of measures, including:
  - Female weight change from pre-pregnancy baseline to birth, post-pregnancy, and escorting period.
  - Maternal weight change to post-pregnancy.
  - Female escorting effort across the escorting period (by age, escort index, frequency).
  - Male escorting effort across the escorting period.
  - Amount of escorting directed toward each pup by fed vs. non-fed mothers and by sex of escort.
  - Pup weights and associated metadata (pup ID, group, litter, sex, age, weight, treatment category).
  - Pairwise relatedness data for pup-adult dyads.
  - Relative within-litter variance in pup weight.
  - Amount of escorting received by pups (esc index, frequency, and feeding rate metrics).
  - Pup survival data to 90 days, 180 days, and 365 days with end ages recorded.
- Example content highlights:
  - Datasets link to experimental treatment groups (T = fed, C = non-fed, R = unmanipulated litter) and breeding attempt identifiers.
  - Detailed pedigree and relatedness fields assist in genetic parentage assignments and social structure analyses.
  - Observational and event-level fields (esc.freq, feeds.rate, nn.str) support fine-grained behavioral analyses.

## Data management, governance, and access
- Data are managed through a centralized workflow with standardized identifiers for packs, groups, litters, and individuals.
- Experimental design and randomization are clearly documented to enable reproducible analyses of provisioning effects.
- Metadata-rich structure supports discovery, interoperability, and reuse across researchers and platforms.
- Governance considerations for Data Stewards:
  - Maintain clear data provenance and versioning, including how and when data were collected, processed, and cleaned.
  - Ensure appropriate handling of controlled experimental data and solution to potential sharing restrictions (e.g., unmanipulated litters vs. manipulated litters).
  - Preserve data schemas and file-level descriptions to facilitate integration with other datasets and catalogues.
  - Establish data sharing policies that respect any embargoes or proprietary aspects of breeding trials and genetic data.
  - Implement ongoing data quality checks and audits to detect anomalies like inconsistent survival records or misaligned lineage data.

## Key considerations for Data Stewards
- Alignment with user needs: dataset is designed to support research on provisioning effects, social dynamics, and offspring survival in cooperative breeders, with rich metadata to facilitate reuse.
- Standards and interoperability: consistent use of identifiers and standardized field naming across 15 CSV files; documented variable definitions and categories.
- Update and maintenance: structured approach to updating after each breeding season; ensure archival of previous versions and documentation of changes.
- Documentation and discoverability: extensive in-file descriptions and external metadata outlining experimental design, instrumentation, and analytical methods to support data discovery and reuse.