# Banded Mongoose Research Project

## Overview
- Long-running study of a wild banded mongoose population (Mungos mungo) on the Mweya Peninsula, Queen Elizabeth National Park, Uganda, since 1995.
- Population typically comprises 10–12 social groups with about 20 adults per group plus offspring.
- Individuals are uniquely marked and tracked to build genetic pedigrees, enabling analysis of how intergroup conflict affects lifetime reproductive success.

## Sampling regime and collection methods
- Groups are observed every 1–3 days for at least 20 minutes; daily visits during pregnancy to record birth dates.
- Pup marking occurs when they emerge from the communal den (~30 days old); 2 mm tail tissue samples collected for genetic analyses to determine parentage.
- One to two individuals per group fitted with radio collars for group localization; most groups habituated to observers at close proximity.

## Fieldwork instrumentation
- Data recorded with Psion II data loggers (until 2014), then via a bespoke Mongoose 2000 data collection app on Samsung Galaxy Note 10.1 tablets.
- Location and tracking aided by radio collars (~30 g; 20 cm whip antenna).
- Data downloaded and imported into a MS Access database; individuals uniquely identified via marks.

## Calibration steps and values
- Field instruments calibrated to factory settings (standard calibration described, no custom adjustments noted).

## Nature and Units of recorded values
- Life-history data: individual identities, birth dates, group membership, reproductive status (estrus dates, identities of estrous females, male mating guards, pregnant females).
- Purpose: inform and constrain parentage analyses.

## Analytical methods
- DNA genotyped with 43 microsatellite markers (or 35 for a subset).
- Parentage assigned using MasterBayes and Colony software.
- Acceptance criteria: assignment probability ≥ 0.9 (full 43-marker panel) or ≥ 0.95 (subset 35-marker panel).

## Quality control
- Mongoose 2000 app includes internal checks to minimize data collection errors (e.g., presence requirement for recording additional data).
- Data quality checks performed via MS Access queries and bespoke R scripts to detect inconsistencies (e.g., multiple death records for an individual).

## Details of data structure
- Data stored in two CSV files:
  - BMRP05_01_ genetic_pedigree_dams: maternal parentage assignments (2000–2019) with fields such as id, dam, assignment probability, and msats used (full panel = 43; subset = 35).
  - BMRP05_01_ genetic_pedigree_sires: paternal parentage assignments (2000–2019) with fields such as Id, sire, assignment probability, and msats used (full panel = 43; subset = 35).