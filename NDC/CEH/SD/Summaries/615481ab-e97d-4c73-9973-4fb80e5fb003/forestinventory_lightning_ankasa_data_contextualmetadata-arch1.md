# Forest inventory and lightning strikes data from Ankasa Conservation area, Ghana, from 2018-2021

## Overview
- Two CSV datasets from Ankasa Conservation Area, southwestern Ghana, covering 2018–2021 (with a COVID-19 interruption in 2019):
  - Forest_inventory_AnkasaGhana_2018_2021.csv: measurements for 2,589 trees and 32 lianas, including diameter and living status, across 50 consecutive 1-hectare plots within a 50-hectare study area.
  - Lightning_strikes_Datasummary_Ankasa_2018_2021.csv: subset of trees from the main inventory that were struck by lightning, including species, diameter, status after strike, fuse status, and post-strike observations (across 4 recorded strikes).
- Part of the NERC project “Lightning: An invisible driver of tree mortality in the tropics?” (Grant NE/P001564/1).

## Study area and sampling design
- Location: Ankasa Conservation Area, southwestern Ghana.
- Area and plots: 50-hectare study area divided into 50 x 1-hectare forest plots.
- Target vegetation: wet and moist evergreen forest with high floristic and structural diversity.
- Sampling threshold: all trees and lianas with stem diameter at 1.3 m (DBH) of ≥25 cm tagged and measured.
- Data categories: tree measurements, living status, and mortality/death modes; lightning-strike subset with detailed strike information.

## Data collection methods
- Lightning detection: every measured tree fitted with a custom Rogowski Coil sensor to record lightning strikes without harming the tree or altering electrical resistance.
- Field notes: recorded tree status (e.g., broken, hollow) and death mode (e.g., uprooted, standing) at each census; documented lightning-related damage in the environment (canopy gaps, sapling mortality).
- Quality controls: unit checks and flagging of ambiguous values; resurvey when possible; missing values annotated for future checks.
- Measurements and status assessments: in each census, notes on coil and fuse condition, with general tree health and damage documented.

## Data structure and key fields
- Forest_inventory_AnkasaGhana_2018_2021.csv
  - Tree_id: original field tag for the stem.
  - census_date: date of measurement (day/month/year).
  - POM: point of measurement for diameter (cm); typically 130 cm but adjusted to avoid buttress/deformity.
  - D: diameter at POM (cm); 0 when dead and diameter not measured.
  - Tree_status: coded status (e.g., A = alive, D = dead) with subcodes:
    - Examples: AN (Alive Normal), AB (Alive Broken), ABH (Alive broken hollow), AUP (Alive uprooted), AH (Alive hollow), DL (Dead by lightning), DS (Dead standing), DV (Vanished), DU (Dead uprooted), PD (Presumed dead), etc.
- Lightning_strikes_Datasummary_Ankasa_2018_2021.csv
  - Country, Site, Plot, Tree_id, Species.
  - census_strike_date: date of census when the tree was found with lightning marks (month/year).
  - POM_strike: diameter measurement point at strike date (cm; typically 130 cm; 0 if not measured).
  - D_strike: diameter at strike date (cm); 0 if dead and not measured.
  - Tree_status_after: status after strike using the same coding scheme as Forest_inventory.
  - Fuse_status: fuse condition at strike date.
  - Observations_after: field observations after the strike.

## Timing, coverage, and data quality notes
- Study window: June 2018 to July 2021; 2019 census interrupted due to COVID-19.
- Data completeness: some missing values due to ambiguous field records; quality checks performed with notes and potential resurvey when feasible.
- Units and definitions: standardised measurement approach (POM around 130 cm; D adjusted for measurement location); explicit coding for alive/dead and post-strike conditions.

## Potential uses for analysts
- Explore relationships between species, diameter, and susceptibility to lightning strikes.
- Assess immediate and short-term mortality and damage patterns following lightning (status after strike, fuse condition, and observations).
- Compare pre-strike and post-strike diameters and health indicators to model resilience or vulnerability.
- Integrate with liana data (from the main inventory) to examine interactions between vegetation structure and lightning effects.
- Support statistical modeling of lightning-driven mortality risks in tropical forests and inform conservation or management decisions.