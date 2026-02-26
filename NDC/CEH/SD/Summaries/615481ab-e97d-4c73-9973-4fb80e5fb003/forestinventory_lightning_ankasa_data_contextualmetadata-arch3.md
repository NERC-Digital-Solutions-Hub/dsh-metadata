# Forest inventory and lightning strikes data from Ankasa Conservation area, Ghana, from 2018-2021

## Overview of dataset
- Two CSV datasets are described:
  - Forest_inventory_AnkasaGhana_2018_2021.csv: measurements for 2,589 trees and 32 lianas across 50 consecutive 1-ha forest plots in Ankasa Conservation Area; includes tree diameters and living status.
  - Lightning_strikes_Datasummary_Ankasa_2018_2021.csv: subset of trees from the forest inventory that were struck by lightning; includes species, diameter, strike date, post-strike status, and fuse status.
- Study area: wet/moist evergreen forest with high floristic and structural diversity in southwestern Ghana.
- Timeframe: data collected from June 2018 to July 2021, with the 2019 census disrupted by COVID-19.
- Project context: part of the NERC project “Lightning: An invisible driver of tree mortality in the tropics?” (Grant NE/P001564/1).

## Data collection methods
- Sampling design: 50 hectares divided into 50 one-hectare plots; all trees and lianas with diameter at 1.3 m (or above buttresses) ≥ 25 cm measured and tagged per census.
- Lightning detection: each measured tree fitted with a custom Rogowski Coil sensor to detect lightning strikes without harming the tree; quick visual checks of fuse to confirm strike; additional notes on coil/fuse condition and electrical conductivity.
- Variables recorded:
  - Tree status (alive/dead) with detailed sub-codes (e.g., alive broken, hollow, uprooted, fallen, etc.).
  - Post-strike observations including damage to the tree and surrounding area (e.g., canopy gaps, sapling mortality).
- Data quality controls: unit checks, flagging ambiguous values for potential resurvey; unresolved errors flagged for future checks.
- Measurements and notes: POM (point of measurement) set at 130 cm unless adjustments were needed for buttress/deformity; D (diameter) recorded when possible; missing values documented.

## Data structure and key fields
- Forest_inventory_AnkasaGhana_2018_2021.csv:
  - Tree_id, census_date, POM, D (diameter), Tree_status (codes such as A for alive, D for dead with sub-codes for condition).
- Lightning_strikes_Datasummary_Ankasa_2018_2021.csv:
  - Country, Site, Plot, Tree_id, Species, census_strike_date, POM_strike, D_strike, Tree_status_after, Fuse_status, Observations_after.
- Status codes:
  - Alive: various sub-states (e.g., AN, AB, ABH, etc.) indicating health and damage level.
  - Dead: sub-states (e.g., DF, DL, DH, DV, etc.) indicating cause/status post-strike or mortality.
  - Fuse_status and Observations_after capture electrical fuse condition and post-strike field observations.

## Data quality, gaps, and governance
- Noted data limitations:
  - Missing values exist where field records were ambiguous or missing.
  - Some data quality checks rely on potential resurvey if feasible; otherwise errors are flagged for future review.
- Metadata and transparency:
  - Explicit definitions for fields and status codes facilitate interpretation and reuse.
  - Routine quality assurance steps described (unit checks, ambiguity flags, post-survey verification).

## Relevance for monitoring and policy
- Demonstrates integration of disturbance events (lightning) into forest health monitoring alongside standard inventory data.
- Enables tracking of individual-tree mortality and damage pathways, and assessment of lightning as a driver of mortality in tropical forests.
- Supports data governance best practices: clear metadata, data provenance (sensor-based detection), and explicit data quality notes, aiding transparency and future data sharing.
- Potential to inform forest management decisions, resilience planning, and long-term ecological monitoring by providing standardized measures of tree health, damage, and disturbance effects.

## Funding and provenance
- Data collected under the NERC project “Lightning: An invisible driver of tree mortality in the tropics?” (Grant NE/P001564/1).