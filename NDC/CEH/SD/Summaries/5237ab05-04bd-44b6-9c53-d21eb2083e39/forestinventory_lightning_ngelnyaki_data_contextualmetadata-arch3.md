# Forest inventory and lightning strikes data from the Ngel Nyaki forest, Nigeria, from 2018-2021

## Overview
- Two CSV datasets documenting tree inventory and lightning-strike events in a 40-hectare Forest Dynamic Plot at Ngel Nyaki, south-eastern Nigeria.
- Timeframe: June 2018 to July 2021.
- Purpose: support understanding of lightning as a driver of tree mortality in tropical forests; part of the Smithsonian ForestGEO network.
- Funded by the NERC project “Lightning: An invisible driver of tree mortality in the tropics?” (Grant NE/P001564/1).

## Data included
- Forest_inventory_NgelNyaki Nigeria_2018_2021.csv
  - Measurements of stems (trees and lianas) and their living status across 2552 individual trees.
  - Includes diameter measurements and status codes (e.g., alive, dead) at a standardized point of measurement.
- Lightning_strikes_Datasummary_NgelNyaki_2018_2021.csv
  - Subset of trees from the main inventory that were struck by lightning (23 observed strikes).
  - Details per strike: species, diameter at strike, pre-strike status, fuse status, and post-strike status.

## Site and data collection details
- Location: Ngel Nyaki Forest Dynamic Plot, submontane forest, elevation 1,588–1,690 m, Nigeria; part of ForestGEO.
- Plot extent: 40 hectares; census records for stems with DBH ≥ 25 cm at 1.3 m height (POM).
- Methods:
  - All tagged trees and lianas measured and classified for living status and damage mode.
  - Rogowski Coil sensors deployed to detect lightning events non-invasively; fuse status observed to confirm strikes.
  - Additional notes on tree condition (e.g., trunk marks, canopy gaps) and surrounding impacts (e.g., sapling mortality).
- Data quality practices:
  - Missing values acknowledged where field records were ambiguous.
  - Quality checks for units; ambiguous values flagged and checked against field notes or resurveyed when possible.

## Data structure and fields
- Forest_inventory_NgelNyaki Nigeria_2018_2021.csv
  - Key columns include: Tree_id, POM (mm), D (cm) (diameter at POM), Tree_status (codes for alive/dead with subcategories), census_date, and related measurement details.
  - D = 0 if the tree is dead and diameter was not measured; POM adjusted (commonly 130 cm) to avoid buttress/deformity.
- Lightning_strikes_Datasummary_NgelNyaki_2018_2021.csv
  - Key columns include: Country, Site, Plot, Tree_id, Species, census_strike_date, POM_strike, D_strike, Tree_status_strike, Fuse_status, Observations_strikes, Tree_status_after, Observations_after.
  - Tree_status codes mirror the alive/dead coding from pre-strike assessments; fuse_status records the fuse condition at strike time.

## Data quality, limitations and governance
- Data issues:
  - Missing values and some ambiguities in field notes requiring follow-up or resurvey where feasible.
  - Potential barriers to data sharing and need for clear metadata to enable reuse across datasets.
- Governance and stewardship:
  - Data collected under a formal research program with explicit quality controls and documentation of data collection procedures.
  - Metadata and provenance are embedded in the dataset descriptions, aiding transparency and reproducibility.

## Relevance for monitoring frameworks
- Demonstrates a structured approach to long-term environmental monitoring, integrating:
  - Standardized measurement protocols (POM, D, status codes) and consistent data capture.
  - Detection of external stressors (lightning) alongside outcome indicators (mortality, status after strike).
  - Data quality assurance procedures and governance considerations (handling missing values, transparency of methods).
- Useful for informing policy and decision-making on forest health, resilience, and vulnerability to extreme events in tropical forests.