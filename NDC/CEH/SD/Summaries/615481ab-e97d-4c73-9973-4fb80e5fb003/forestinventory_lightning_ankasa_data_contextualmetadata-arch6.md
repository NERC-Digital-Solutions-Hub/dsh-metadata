# Forest inventory and lightning strikes data from Ankasa Conservation area, Ghana, from 2018-2021

## Overview
- Two CSV datasets from Ankasa Conservation Area, southwestern Ghana, covering 2018–2021.
- Forest_inventory_AnkasaGhana_2018_2021.csv: measurements for 2,589 trees and 32 lianas across 50 consecutive 1-ha plots; includes diameter at breast height (D) and living status or mortality status.
- Lightning_strikes_Datasummary_Ankasa_2018_2021.csv: subset of trees from the forest inventory that were struck by lightning; includes species, diameter, post-strike status, fuse status, and strike observations; records of 4 lightning events.
- Data collected under the NERC project Lightning: An invisible driver of tree mortality in the tropics? (Grant NE/P001564/1); 2019 census partly disrupted by COVID-19.

## Data files and content
- Forest_inventory_AnkasaGhana_2018_2021.csv
  - Columns include: Tree_id, census_date, POM (point of measurement in cm, typically 130 cm), D (diameter in cm), Tree_status (codes for alive or dead with detailed subcategories such as Alive Normal, Alive Uprooted, Dead by various causes, etc.).
  - Captures living status, death mode, and diameter for each tree (and similarly for 32 lianas).
- Lightning_strikes_Datasummary_Ankasa_2018_2021.csv
  - Columns include: Country, Site, Plot, Tree_id, Species, census_strike_date, POM_strike, D_strike, Tree_status_after, Fuse_status, Observations_after.
  - Details species-level strike information, post-strike tree status, fuse condition, and field observations after the strike.

## Data collection methods
- Sampling design: 50-ha area subdivided into 50 x 1-ha forest plots; census activities across campaigns.
- Inclusion criteria: measured and tagged all trees and lianas with stem diameter ≥25 cm at 1.3 m height (or above buttresses); recorded living status or death mode.
- Quality controls: checks for unit consistency; ambiguous values flagged for reviewing field notes or resurvey; resurvey pursued when possible; otherwise errors flagged for future checks.
- Lightning detection: all measured trees equipped with a Rogowski Coil sensor to detect lightning strikes non-invasively; visual checks of fuse and electrical conductivity recorded; post-strike damage documented (e.g., trunk marks, canopy changes, sapling mortality).

## Data structure and notable fields
- Forest_inventory_AnkasaGhana_2018_2021.csv
  - Key fields: Tree_id, census_date, POM, D, Tree_status (detailed coding for alive/dead and subcategories such as hollow, broken, uprooted, etc.).
- Lightning_strikes_Datasummary_Ankasa_2018_2021.csv
  - Key fields: Country, Site, Plot, Tree_id, Species, census_strike_date, POM_strike, D_strike, Tree_status_after, Fuse_status, Observations_after.
- Both datasets include column definitions and codes, with explicit status coding for various alive/dead and damage/mortality conditions.

## Data quality and limitations
- Missing values: present where field records were ambiguous or not recorded; some values could not be resolved via resurvey.
- Interrupted data collection: 2019 census partially disrupted by COVID-19, affecting continuity.
- Data quality checks exist (unit validation, field note cross-checks) but researchers should account for potential inconsistencies in legacy field records.

## Potential uses and applications (Data Support perspective)
- Facilitates analysis of lightning-driven mortality within a tropical forest context, including species- and size-specific responses.
- Enables examination of how diameter, health status, and post-strike outcomes relate to mortality and canopy dynamics.
- Supports cross-dataset analyses to explore correlations between pre-strike conditions (D, status) and post-strike outcomes (Tree_status_after, fuse condition, subsequent observations).
- Provides a baseline dataset for long-term forest dynamics in the Ankasa moist/wet evergreen forest, useful for policy support, conservation planning, and data products for end users.