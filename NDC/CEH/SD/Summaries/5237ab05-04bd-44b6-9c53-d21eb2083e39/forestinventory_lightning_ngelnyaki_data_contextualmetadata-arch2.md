# Forest inventory and lightning strikes data from the Ngel Nyaki forest, Nigeria, from 2018-2021

## Overview
- Datasets from a 40-hectare area of Ngel Nyaki Forest Dynamic Plot in south-eastern Nigeria, part of the Smithsonian ForestGEO network.
- Timeframe: June 2018 to July 2021.
- Aim: document tree and liana stem diameters, living status, and lightning-induced mortality to study environmental health and drivers of tree mortality.
- Two linked datasets:
  - Forest_inventory_NgelNyaki Nigeria_2018_2021.csv: measurements on 2552 individual trees (diameter, live/dead status, and related notes).
  - Lightning_strikes_Datasummary_NgelNyaki_2018_2021.csv: subset of trees struck by lightning, with species, diameter, pre- and post-strike status, and fuse information.
- Funding: NERC project “Lightning: An invisible driver of tree mortality in the tropics?” (Grant NE/P001564/1).

## Data sets and contents
- Forest_inventory_NgelNyaki Nigeria_2018_2021.csv
  - Measurements for trees and lianas with stem diameter 25 cm or greater at 1.3 m, within the 40-ha plot.
  - Includes tree_id, census_date, POM (point of measurement) in mm, D (diameter in cm at POM), and Tree_status (codes for Alive/Dead with sub-statuses).
  - Provides living status notes (e.g., broken, hollow) and death mode (e.g., uprooted, standing).
- Lightning_strikes_Datasummary_NgelNyaki_2018_2021.csv
  - Subset of trees from the main inventory that were struck by lightning (23 strikes recorded).
  - Includes country, site, plot, tree_id, species, census_strike_date, POM_strike, D_strike, Tree_status_strike, Fuse_status, Observations_strikes, Tree_status_after, Observations_after.
  - Documents pre-strike status, strike observations, fuse condition, and post-strike status.

## Data collection methods
- Study site: Ngel Nyaki Forest Dynamic Plot (submontane, elevation 1,588–1,690 m).
- Census protocol: tagged and measured all stems with DBH ≥ 25 cm at 1.3 m, noting living status and death mode; 40-ha plot within ForestGEO network.
- Lightning detection: each tree measured with a custom Rogowski Coil sensor to detect lightning strikes non-invasively; visual checks of fuse status and trunk/branch damage; electrical conductivity measured.
- Quality controls: checks for unit errors, flagging ambiguous values for review against field notes; resurvey when possible; missing values flagged for future checking.
- Documentation of outcomes: recorded tree-specific lightning damage and environmental impacts (e.g., canopy gaps, sapling mortality).

## Data structure and key fields
- Forest_inventory_NgelNyaki Nigeria_2018_2021.csv
  - Tree_id: stem tag number
  - census_date: date of field measurement
  - POM: Point of measurement (cm), typically 130 cm; used to determine D
  - D: Diameter at POM (cm). If dead and diameter not measured, D = 0
  - Tree_status: alive or dead with coded sub-statuses (e.g., A for Alive, D for Dead; second letter combinations indicate condition such as AN, AB, ABD, AH, AL, DL, DF, DV, DU, etc.)
- Lightning_strikes_Datasummary_NgelNyaki_2018_2021.csv
  - Country, Site, Plot: location identifiers
  - Tree_id: field tag number
  - Species: taxonomic identification
  - census_strike_date: month/year when the tree showed lightning marks
  - POM_strike: diameter measurement point at strike date
  - D_strike: diameter at POM_strike (cm); 0 if not measured due to death
  - Tree_status_strike: status before strike (same coding as Tree_status)
  - Fuse_status: fuse condition at strike date
  - Observations_strikes: field observations prior to strike
  - tree_status_after: status after the strike (same coding as Tree_status)
  - Observations_after: observations after strike

## Quality and limitations
- Data include missing values where field records were ambiguous or resurvey was not possible.
- For dead trees where diameter was not measured, D is recorded as 0.
- POM may be adjusted from 130 cm to avoid buttress or deformity.
- Data are suitable for analyzing lightning-driven mortality and environmental health trends, with explicit status codes enabling standardized interpretation across time.

## Relevance for environmental monitoring
- Provides standardized, monotemporal records of tree health and lightning-related damage within a long-running ForestGEO plot.
- Enables cross-comparison of pre- and post-strike conditions, and tracking of canopy and regeneration impacts (e.g., sapling mortality, canopy gaps).
- Data quality controls and explicit metadata facilitate integration with other environmental datasets and long-term monitoring efforts.
- Supports investigation into how environmental drivers (like lightning) contribute to forest dynamics and mortality rates.

## Access and provenance
- Datasets produced as part of a formal field study within the Ngel Nyaki Forest Dynamic Plot, Nigeria.
- Data collection and processing described with quality assurance steps and measurement conventions, enabling re-use in environmental monitoring analyses and policy-relevant reporting.