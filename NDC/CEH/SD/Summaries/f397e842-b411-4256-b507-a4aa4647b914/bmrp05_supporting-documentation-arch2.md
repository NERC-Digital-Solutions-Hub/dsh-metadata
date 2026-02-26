# Sampling regime and collection methods

- Overview
  - The Banded Mongoose Research Project studies wild banded mongooses (Mungos mungo) on the Mweya Peninsula, Queen Elizabeth National Park, Uganda, ongoing since 1995.
  - The population typically comprises 10–12 social groups with about 20 adults plus offspring per group.
  - The aim is to determine lifetime reproductive success and how exposure to intergroup conflict affects it, using genetic pedigree data.

- Population and setting
  - Location: Mweya Peninsula, Queen Elizabeth National Park, Uganda (0°12′ S, 29°54′E).
  - Long-term monitoring of group membership, life history, and reproductive behavior across social groups.

- Sampling regime and life-history data collection
  - Individual marking and identification:
    - Adults marked with fur shave patches; pups marked with dye marks.
    - Regular trapping every two months to maintain marks.
  - Group locating and tracking:
    - One to two individuals per group fitted with radio collars (≈30 g; 20 cm antenna).
    - Groups located via radio telemetry; most groups habituated to observers within <5 m.
  - Field observations:
    - Groups visited every 1–3 days for ≥20 minutes to record group composition, life history, and reproductive behavior.
    - Daily visits when females are pregnant to record birth dates accurately.
  - Genetic sampling:
    - When pups emerge (~30 days old), pups are trapped to mark and collect a 2 mm tail-tip tissue sample for genetic analyses to determine parentage.
    - Pedigree data used to assess how intergroup conflict exposure influences lifetime reproductive success.

- Fieldwork instrumentation
  - Data capture:
    - Psion II data loggers used until 2014.
    - Since 2014, a bespoke Mongoose 2000 data collection app on Samsung Galaxy tablets.
  - Data management:
    - Data downloaded and imported into MS Access databases.
  - Equipment specifics:
    - Radio collars: ~30 g, from Sirtrack Ltd; antenna: 20 cm whip from Biotrack Ltd.
  - Calibration:
    - Field instruments calibrated to factory settings.

- Nature and units of recorded values
  - Life-history data: individual identities, birth dates, group membership.
  - Reproductive data: female oestrus dates, identities of females in oestrus, male mate-guarding identities, pregnant female identities.
  - Purpose: inform parentage candidates and longitudinal reproductive analyses.

- Analytical methods
  - Genetic analysis:
    - DNA genotyping using 43 polymorphic microsatellite markers (full panel) or 35 markers (subset panel).
    - Parentage assigned with MasterBayes and Colony software.
    - Acceptance criteria:
      - Full panel: assignment probability ≥ 0.9.
      - Subset panel: assignment probability ≥ 0.95.
  - Purpose: robust maternal and paternal pedigree assignments to relate to intergroup conflict exposure.

- Quality control
  - Data collection checks in the Mongoose 2000 app (e.g., an individual must be marked present in group composition to record behavioral data).
  - Data quality checks performed in MS Access and bespoke R code to detect inconsistencies (e.g., multiple death records for a single individual).

- Details of data structure
  - Data stored in two CSV files:
    - (1) BMRP05_01_genetic_pedigree_dams
      - Content: maternal parentage assignments to individuals exposed to intergroup conflict (Jan 2000–Mar 2019).
      - Columns:
        - id (individual identity)
        - dam (mother identity)
        - assigmentprobs_dam (marginal probability that maternal assignment is correct)
        - msats.used (panel: full 43 or subset 35)
    - (2) BMRP05_01_genetic_pedigree_sires
      - Content: paternal parentage assignments to individuals exposed to intergroup conflict (Jan 2000–Mar 2019).
      - Columns:
        - Id (individual identity)
        - sire (father identity)
        - assigmentprobs_sire (marginal probability that paternal assignment is correct)
        - msats.used (panel: full 43 or subset 35)

- Relevance for environmental monitoring and data access
  - Standardized, long-term dataset enabling assessment of environmental health and policy performance over time through monitoring of genetic pedigree and reproductive success.
  - Clear data provenance, calibration, quality control, and data storage practices (MS Access, structured CSVs) support reproducibility and auditability.
  - Highlights the challenge of increasing dataset value by integrating with additional data and facilitating access to underlying data for broader use.