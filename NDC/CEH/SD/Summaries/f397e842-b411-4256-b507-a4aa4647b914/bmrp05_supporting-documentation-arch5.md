# Sampling regime and collection methods

- Overview
  - The Banded Mongoose Research Project studies a population of wild banded mongooses (Mungos mungo) on the Mweya Peninsula, Queen Elizabeth National Park, Uganda, ongoing since 1995.
  - Populations typically consist of 10–12 social groups with around 20 adults plus offspring; individuals are uniquely marked for identification.
  - Groups are located using radio collars (1–2 individuals per group) and observed by walkers to record group composition, life history, and reproductive behavior; pups are marked and sampled for genetics to determine parentage, enabling analysis of how intergroup conflict influences lifetime reproductive success.

- Field methods and instrumentation
  - Data capture evolved from handheld Psion II data loggers (until 2014) to a bespoke Mongoose 2000 data collection app on Samsung tablets.
  - Data are downloaded and imported into a Microsoft Access database.
  - Radio collars weigh about 30 g with a 20 cm whip antenna.

- Sampling schedule and data collection
  - Groups are visited every 1–3 days for at least 20 minutes; daily visits during pregnancies to record accurate birth dates.
  - Pups are marked around 30 days old and tissue samples (2 mm tail tips) are collected for genetic analyses to determine parentage.
  - Bloodline data (life history, birth dates, group membership, reproductive status) are collected to support parentage inference.

- Calibration
  - Field instruments are calibrated to factory settings.

- Nature and units of recorded values
  - Life history data: individual identities, birth dates, group membership.
  - Reproductive data: dates of female estrus, estrus identities, male mate-guarding identities, pregnant female identities.
  - These data support identifying parentage candidates.

- Analytical methods
  - DNA genotyping uses 43 polymorphic microsatellite markers (full panel) or 35 markers (subset).
  - Parentage assignment conducted with MasterBayes and Colony software.
  - Acceptance thresholds: assignment probability ≥ 0.9 for full panel (43 markers); ≥ 0.95 for subset panel (35 markers).

- Quality control
  - Mongoose 2000 app includes internal data-checks (e.g., an individual must be marked present to collect related behavioral data).
  - Additional quality checks performed in MS Access via queries and bespoke R code to detect inconsistencies, such as multiple death records for a single individual.

- Data structure and storage
  - Data stored in two CSV files:
    - BMRP05_01_genetic_pedigree_dams: maternal parentage assignments (2000–2019) with columns: id, individual identity, dam, assigned mother, assignment probability for dam, msats used (full panel = 43; subset = 35).
    - Paternal pedigree: paternal parentage assignments (2000–2019) with columns: Id, individual identity, sire, assigned father, assignment probability for sire, msats used (full panel = 43; subset = 35).
  - Timeframe for parentage data: January 2000 to March 2019.

- Data availability and governance considerations for data stewards
  - The dataset provides detailed maternal and paternal assignments with probabilities and marker panels, enabling traceable parentage analyses and replication of analyses.
  - Documentation includes data collection instruments, protocols, observation cadence, genetic methods, and QC steps, which support data provenance and reuse.
  - Coordinates and metadata (study location, period, marker panels, software versions) are essential for discovery, interoperability, and future updates or republishing.
  - Users should be aware of the time-limited genetic data (2000–2019) and the need to reference the specific marker panels and software used for replication or reanalysis.