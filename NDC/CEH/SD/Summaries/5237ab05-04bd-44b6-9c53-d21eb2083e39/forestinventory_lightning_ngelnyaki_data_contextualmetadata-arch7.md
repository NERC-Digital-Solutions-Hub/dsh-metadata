# Forest inventory and lightning strikes data from the Ngel Nyaki forest, Nigeria, from 2018-2021

## Overview
- Location: Ngel Nyaki Forest Dynamic Plot, south-eastern Nigeria; 40-hectare submontane ForestGEO site.
- Timeframe: June 2018 – July 2021.
- Datasets:
  - Forest_inventory_NgelNyaki Nigeria_2018_2021.csv: measurements on 2552 trees and lianas; diameter at 1.3 m; living status or death status.
  - Lightning_strikes_Datasummary_NgelNyaki_2018_2021.csv: subset of trees that experienced lightning strikes; includes species, diameter, strike date, fuse status, and post-strike status. Contains records for 23 lightning strikes.
- Project context: Part of the NERC project “Lightning: An invisible driver of tree mortality in the tropics?” (Grant NE/P001564/1).

## Data files and contents
- Forest_inventory_NgelNyaki Nigeria_2018_2021.csv
  - Tree-level data for each measured stem: Tree_id, census_date, POM (point of measurement, cm), D (diameter, cm), Tree_status (codes for alive/dead and variants).
  - Coverage: 2552 trees; status notes include alive, dead, broken, hollow, uprooted, etc.
- Lightning_strikes_Datasummary_NgelNyaki_2018_2021.csv
  - Per-strike data linked to trees: Country, Site, Plot, Tree_id, Species, census_strike_date, POM_strike, D_strike, Tree_status_strike, Fuse_status, Observations_strikes, Tree_status_after, Observations_after.
  - Strikes: 23 recorded events; includes pre-strike and post-strike statuses and fuse condition.

## Data collection methods
- Plot and tree census
  - All trees and lianas with DBH ≥ 25 cm tagged and measured at 1.3 m; notes on living status and damage.
  - Measurements include diameter adjustments (POM) to avoid buttress/deformity; status annotations such as alive/dead and sub-statuses.
- Lightning detection
  - Each tree installed with a Rogowski Coil sensor to detect lightning strikes non-destructively.
  - Visual checks of fuse and electrical conductivity recorded; post-strike damage documented (e.g., trunk marks, canopy gaps, sapling mortality).
- Data quality
  - Quality controls include unit checks; ambiguous values flagged for review against field notes or resurvey when feasible.
  - Missing values are acknowledged; unresolved issues flagged for future surveys.

## Data structure and coding
- Forest_inventory...csv
  - Key fields: Tree_id, census_date, POM, D, Tree_status (codes such as A for alive, D for dead; second letter combinations indicate condition: AN, AB, ABH, ABD, AD, ADH, AF, AH, AR, AL, DB, DF, DS, DV, DU, etc.).
  - POM typically 130 cm unless adjusted for buttress/deformity; if dead and diameter not measured, POM = 0.
- Lightning_strikes...csv
  - Key fields: Country, Site, Plot, Tree_id, Species, census_strike_date, POM_strike, D_strike, Tree_status_strike, Fuse_status, Observations_strikes, Tree_status_after, Observations_after.
  - Status codes for trees before strike (Tree_status_strike) and after strike (Tree_status_after) follow the same code conventions as the inventory data.

## Temporal, spatial, and usage considerations for GIS
- Temporal scope: census data (2018–2021) and lightning strike events within the same period.
- Spatial aspect
  - Data are per-tree within a fixed 40-ha plot; there are no explicit geographic coordinates in the CSVs.
  - To map trees, you will need the plot geometry and a spatial index (e.g., map or field notes tying Tree_id to location).
  - Potential to create layers: tree status points, and lightning-strike event points (linked by Tree_id where applicable).
- Data integration for GIS
  - Join by Tree_id between the two datasets to link pre-strike status, diameter, and post-strike outcomes with lightning observations.
  - Use POM and D for spatially aware symbolization of tree size and condition.
  - Decode status codes to categorize trees (e.g., alive vs. dead, lightning-damaged vs. non-damaged).
- Quality and limitations
  - Missing values and potential unit errors may require cleaning before GIS work.
  - Only 23 lightning-strike records; analyses of lightning-driven mortality will be constrained by sample size.
  - No direct coordinates; rely on plot-level georeferencing from field maps or project shapefiles.

## Practical GIS applications
- Map distribution of living and dead trees across the 40-ha plot.
- Visualize locations of trees struck by lightning and associated post-strike outcomes.
- Assess spatial relationships between lightning events, canopy damage, and subsequent tree mortality.
- Integrate with other ForestGEO datasets for multi-layer environmental analyses.

## Provenance and access
- Project attribution: NERC grant NE/P001564/1; “Lightning: An invisible driver of tree mortality in the tropics?”
- Data are organized as two CSV files with defined field codes and documented data collection methods.