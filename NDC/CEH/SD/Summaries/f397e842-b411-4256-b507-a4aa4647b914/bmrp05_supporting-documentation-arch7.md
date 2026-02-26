# Sampling regime and collection methods

- Context and population
  - Banded Mongoose Research Project studying Mungos mungo on the Mweya Peninsula, Queen Elizabeth National Park, Uganda (0°12′ S, 29°54′E).
  - Long-term study since 1995; typically 10–12 social groups with around 20 adults per group plus offspring.
  - Individuals uniquely marked for identification; groups located via radio collars in some individuals and observers habituated to humans.

- Field data collection workflow
  - Regular trapping every two months.
  - Groups visited every 1–3 days (at least 20 minutes) to record group composition, life history, and reproductive behaviour.
  - Daily visits during pregnancy to record accurate birth dates; pups marked at ~30 days and tissue samples collected for genetics to determine parentage.
  - Genetic pedigree used to assess how intergroup conflict exposure affects lifetime reproductive success.

- Instrumentation and data capture
  - Early data capture: Psion II data logger (LZ model) until 2014.
  - Later data capture: bespoke Mongoose 2000 app on Samsung Galaxy Note tablets; data downloaded and imported into MS Access database.
  - Individuals equipped with radio collars (~30 g) with a 20 cm whip antenna.

- Calibration and measurement
  - Field instruments calibrated to factory settings.

- Data content and units
  - Life history data: individual identities, birth dates, group membership.
  - Reproductive data: female estrus dates and identities, male mate-guarding identities, pregnant female identities.
  - Purpose: inform candidate parentage for genetic analyses.

- Analytical methods
  - DNA genotyped with 43 polymorphic microsatellite markers (or 35 for a subset).
  - Parentage assigned using MasterBayes and Colony software.
  - Acceptance criteria: assignment probability ≥ 0.9 for full-panel (43 markers); ≥ 0.95 for subset panel (35 markers).

- Quality control and data integrity
  - Mongoose 2000 app includes internal checks to minimize data collection errors (e.g., requiring presence in group for recording certain data).
  - Data quality checks performed via MS Access queries and custom R code to detect inconsistencies (e.g., multiple death records for an individual).

- Data structure and availability
  - Data stored in two CSV files:
    - BMRP05_01_ genetic_pedigree_dams: maternal parentage assignments (2000–2019) with fields such as id, dam, assignmentprobs_dam, msats.used (full panel = 43; subset = 35).
    - BMRP05_01_ genetic_pedigree_sires: paternal parentage assignments (2000–2019) with fields such as Id, sire, assignmentprobs_sire, msats.used (full panel = 43; subset = 35).
  - Key columns for maternal assignments: id, individual identity, dam, individual identity of assigned mother, assigmentprobs_dam, msats.used.
  - Key columns for paternal assignments: Id, individual identity, sire, individual identity of assigned father, assigmentprobs_sire, msats.used.
  - Timeframe: January 2000 to March 2019.

- Spatial context and GIS relevance
  - Groups occupy distinct territories; locations can be inferred via radio telemetry data and observer records.
  - Spatial analysis potential includes mapping group territories, movement patterns, and linking spatial data with life history and genetic parentage to study reproductive success and intergroup interactions.

- Data use considerations for GIS specialists
  - Data integration requires merging life-history, reproductive status, and genetic pedigree with spatial coordinates from telemetry and field observations.
  - Multiple data sources and formats (MS Access, CSV) necessitate careful data cleaning and standardization.
  - Temporal coverage spans nearly two decades, enabling longitudinal spatial analyses of territory use and demographic outcomes.