# Sampling regime and collection methods

## Overview
- Study of wild banded mongooses (Mungos mungo) on Mweya Peninsula, Queen Elizabeth National Park, Uganda (0°12′ S, 29°54′E).
- Ongoing since 1995; typically 10–12 social groups occupying distinct territories.
- Groups ~20 adults plus offspring; individuals uniquely marked for long-term observation.
- Data collected to determine how intergroup conflict affects lifetime reproductive success via genetic pedigree.

## Fieldwork and instrumentation
- Data collection tools: Psion II data loggers (until 2014) and a bespoke Mongoose 2000 app on Samsung Galaxy Note tablets; data stored in MS Access.
- Identification marks: adults with fur shave patches; pups with dye marks; regular trapping every two months.
- Radio collars: 1–2 individuals per group (≈30 g, 20 cm antenna) for group localization.
- Observer approach: most groups habituated to observers (within <5 m).

## Calibration and measurement
- Field instruments calibrated to factory settings.

## Nature and units of recorded values
- Life history data: individual identities, birth dates, group membership.
- Reproductive status: female estrus dates and identities, male mate-guarding identities, pregnant female identities.
- Used to inform parentage candidates.

## Data collection schedule and procedures
- Group visits: every 1–3 days for at least 20 minutes.
- Daily visits during pregnancy for accurate birth dating.
- Pup marking and sampling: pups emerge around 30 days; tissue samples (2 mm tail tip) collected for genetic analyses to determine parentage.

## Analytical methods
- DNA genotyping: 43 microsatellite markers (or 35 for a subset).
- Parentage assignment: MasterBayes and Colony.
- Acceptance thresholds: assignment probability ≥0.9 (full panel) or ≥0.95 (subset panel).

## Quality control
- Mongoose 2000 app includes internal checks (e.g., presence requirement to collect behavioral data).
- Data quality assurance via MS Access queries and bespoke R code to detect errors (e.g., multiple death records).

## Data structure
- Two CSV files:
  - maternal (dam) parentage (January 2000 – March 2019):
    - Columns: id, individual identity, dam, maternal assignment, assignmentprob_dam, msats.used (full panel = 43; subset = 35)
  - paternal (sire) parentage (January 2000 – March 2019):
    - Columns: Id, individual identity, sire, paternal assignment, assignmentprob_sire, msats.used (full panel = 43; subset = 35)