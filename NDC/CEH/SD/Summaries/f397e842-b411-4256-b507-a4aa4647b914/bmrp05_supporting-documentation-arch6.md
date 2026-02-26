# Sampling regime and collection methods

- Study setting and population
  - Wild banded mongooses (Mungos mungo) on Mweya Peninsula, Queen Elizabeth National Park, Uganda.
  - Long-term study since 1995; typically 10–12 social groups, ~20 adults per group plus offspring.
  - Individuals uniquely marked for identification; radio collars fitted to 1–2 individuals per group to aid location.
  - Groups visited every 1–3 days (20+ minutes) to record group composition, life history, and reproductive behavior; daily visits during pregnancy for accurate birth dating.
  - Pups marked at ~30 days; tail tissue sampled (2 mm) for genetic analyses to determine parentage; pedigree used to assess impact of intergroup conflict on lifetime reproductive success.

- Field instrumentation and data capture
  - Field data recorded with Psion II data loggers (until 2014) and later via a bespoke Mongoose 2000 app on Galaxy tablets.
  - Data downloaded and imported into a database (MS Access).
  - Radio collars: ~30 g with a 20 cm whip antenna.
  - Calibration: field instruments calibrated to factory settings.

- Data types, units, and collection details
  - Life history data: individual identities, birth dates, group membership, reproductive status (dates of estrus, estrus identities, male mate-guarding identities, pregnant female identities).
  - Reproductive data collection supports accurate birth dates and maternal/paternal assignments.
  - Genetic samples: tail tissue from pups for parentage analysis; DNA genotyped using microsatellite markers.

- Analytical methods for parentage
  - Genotyping: 43 microsatellite markers (full panel) or 35 markers (subset panel).
  - Parentage assignment: MasterBayes and Colony programs.
  - Acceptance criteria: maternal assignments with probability ≥ 0.9 (full panel) or ≥ 0.95 (subset); paternal assignments with probability ≥ 0.9 (full panel) or ≥ 0.95 (subset).
  - Data linkage: genetic pedigree used to determine parentage and examine effects of intergroup conflict on lifetime reproductive success.

- Quality control and data validation
  - Built-in checks in the Mongoose 2000 app to enforce data collection rules (e.g., presence required to record certain behavioral data).
  - Data quality checks using MS Access queries and bespoke R code to detect inconsistencies (e.g., multiple death records for an individual).

- Data structure and access
  - Data stored in two CSV files:
    - BMRP05_01_ genetic_pedigree_dams: maternal parentage assignments (2000–2019) with fields including id, dam, assignment probability, and microsatellites panel used.
    - BMRP05_01_ genetic_pedigree_sires: paternal parentage assignments (2000–2019) with fields including Id, sire, assignment probability, and microsatellites panel used.
  - Fields include: individual identity, dam/sire identity, assignment probabilities, and microsatellite panel used (full = 43; subset = 35).

- Data use and purpose
  - Pedigree data and parentage assignments underpin analyses of reproductive success and the influence of intergroup conflict.
  - Longitudinal data collection supports understanding life history and social dynamics within and between groups.