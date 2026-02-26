# Data description for Intergroup contests in banded mongooses (Mungos mungo) on the Mweya peninsula, Uganda, 2000-2019

- Purpose and scope
  - Datasets relevant to analyses on the outcomes of intergroup contests in banded mongooses (Mungos mungo) on the Mweya peninsula, Uganda, from 2000 to 2019.
  - Designed to support analyses described by accompanying README.doc using R.
  - Includes life-history data, morphological data (size, weight), genetic pedigree data, and contest-outcome data; also contains outputs of original analyses for validation.

- Data contents and structure
  - Life-history data for individual mongooses (e.g., birth, death, age, sex, group membership).
  - Morphological measurements (size, weight) and reproductive status (e.g., pregnancy).
  - Genetic pedigree data documenting familial relationships (dam, sire, and ancestry).
  - Data on contest outcomes between groups (e.g., focal and rival groups, winners, dates, eviction events).
  - Outputs of original analyses to facilitate checking results.
  - Numerous datasets with descriptive names and detailed column metadata, including:
    - weights and pregnancy status (e.g., combined_field_capture_weight_data_wpregnant)
    - pedigree and parentage assignments (e.g., final 2020 complete pedigree; full parentage assignments to 2016)
    - life history time series (e.g., Lifehistory_20210525)
    - pre-imputation and post-imputation datasets related to group contests and guarding
    - oestrus and guarding-related variables
  - Key data fields typically include: date (numeric and formatted), pack (group) ID, individual ID, sex, weight, age (in days on weighing date), birth date, pregnancy status, event IDs (e.g., eviction), and various contest-related codes.

- Data collection and instrumentation
  - Field data collected near-daily on groups and members; contest data recorded as feasible during sampling.
  - Weight and morphological data collected at regular intervals via trapping or weighing on a scale.
  - Data capture tools include hand recording, Psion Walkabout devices, and a bespoke tablet-based system.
  - Pedigree data obtained from field blood samples and subsequent genetic analyses (lab-based).

- Calibration, quality, and documentation
  - Equipment regularly calibrated; calibration details available via www.socialis.org or pagreen@ucsb.edu.
  - Units are self-explanatory or documented in the data dictionary columns (col_explanation) for each dataset.
  - Quality control conducted by a six-person Ugandan field team with over 75 years of combined experience; analytical quality checks included in the R code documenting model fit and data checks.
  - Data description emphasizes reproducibility and the presence of outputs from original analyses for validation purposes.

- Analytical methods and reproducibility
  - All analyses referenced are based on large-field datasets and are described in associated R code (README and code files linked to the data).
  - The dataset collection and metadata are designed to support transparent, standardised analyses and cross-checking of outputs.

- Data management and access considerations
  - The collection includes comprehensive metadata and a structured set of datasets to support data provenance and reproducibility.
  - Calibration and contact information provided to facilitate data validation and reuse.
  - Data are designed to be stored and uploaded to appropriate portals; outputs are included to aid verification of analyses.

- Applicability for environment-monitoring analytics
  - Provides high-frequency, longitudinal data on social and ecological interactions (intergroup contests, group dynamics, life-history traits) in a natural population.
  - Suitable for time-series analyses, monitoring of population/social dynamics, and evaluation of factors influencing contest outcomes and fitness over two decades.
  - Rich pedigree and genetic data enable integrated ecological and genetic analyses, enhancing understanding of environmental and social drivers of animal behavior.