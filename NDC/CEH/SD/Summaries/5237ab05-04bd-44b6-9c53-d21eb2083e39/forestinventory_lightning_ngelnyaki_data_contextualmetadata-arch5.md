# Forest inventory and lightning strikes data from the Ngel Nyaki forest, Nigeria, from 2018-2021

## Overview of data
- Two CSV datasets:
  - Forest_inventory_NgelNyaki Nigeria_2018_2021.csv: measurements for 2552 trees (and lianas) assessing diameter, living status, and mode of death across a 40-hectare forest plot.
  - Lightning_strikes_Datasummary_NgelNyaki_2018_2021.csv: subset of trees from the above inventory that were struck by lightning, including species, diameter, pre-strike status, strike details, fuse status, and post-strike status.
- Study period and context:
  - Data collected June 2018 to July 2021.
  - Site: Ngel Nyaki Forest Dynamic Plot, south-eastern Nigeria; submontane, high diversity; part of ForestGEO.
  - Part of NERC project: Lightning: An invisible driver of tree mortality in the tropics? (Grant NE/P001564/1).

## Data collection methods and quality
- Field protocol:
  - All trees and lianas with stem diameter at 1.3 m (or above buttresses) ≥25 cm tagged, measured, and recorded for living status and death mode.
  - Missing values exist where field records were ambiguous; quality controls check unit errors and flag ambiguities for resurvey when possible.
  - Rogowski Coil sensors installed on each measured tree to detect lightning strikes non-invasively;safety and integrity checks performed (fuse status, electrical conductivity, general coil condition).
  - Documentation of lightning-related damage to the tree and surrounding vegetation (trunk marks, broken branches, canopy dieback, sapling mortality).
- Data integrity and updates:
  - If a resurvey is not possible, errors are flagged for future checking.
  - Tree_ids link records across datasets; POM (point of measurement) typically 130 cm; D is diameter at POM; if the tree is dead and D isn’t measured, D=0 and POM may be 0.
- Notable data notes:
  - Some values missing or ambiguous; field notes and potential resurvey are used to resolve issues; status codes differentiate between alive/dead and subcategories (e.g., intact, hollow, broken, burned, uprooted, etc.).

## Data structure and definitions
- Forest_inventory_NgelNyaki Nigeria_2018_2021.csv
  - Key columns: Tree_id (origin field tag), census_date (date of measurement), POM (mm; note: defined as 130 cm normally), D (cm; diameter at POM; 0 if not measured due to death), Tree_status (codes for alive or dead with subtypes; e.g., AN, AB, ABD, AD, AH, DL, DF, DS, DV, DU, PD, etc.).
- Lightning_strikes_Datasummary_NgelNyaki_2018_2021.csv
  - Key columns: Country, Site, Plot, Tree_id, Species, census_strike_date (month/year of census when lightning marks observed), POM_strike (cm), D_strike (cm; 0 if not measured due to death), Tree_status_strike (pre-strike status codes), Fuse_status (cumulative fuse condition), Observations_strikes (field notes pre-strike), Tree_status_after (status at latest census post-strike), Observations_after (post-strike observations).
- Units and measurement context:
  - POM: cm (point of measurement, typically 130 cm; adjustments if buttresses/deformities present).
  - D: cm (diameter at current POM; 0 if not measured due to death).
  - Status codes distinguish alive vs. dead and provide nuanced subcategories for health, damage, and cause.

## Practical guidance for data stewardship
- Data linking and integrity:
  - Validate linkage between the two files via Tree_id; cross-check census_dates and census_strike_dates for temporal consistency.
  - Ensure consistency of POM and D values when comparing pre- and post-strike records.
- Metadata and governance:
  - Maintain clear codebooks for Tree_status and Tree_status_strike codes, including all subcategories (e.g., AN, AB, ABD, AD, AH, etc.) and death-related statuses.
  - Document field-note-driven amendments and any resurvey outcomes; flag unresolved ambiguities for future review.
  - Note the dataset’s provenance: part of a published study on lightning as a driver of tree mortality in the tropics; reference the NERC grant for citation and access provenance.
- Data quality and usability:
  - Be mindful of missing values, especially where D is not measured or POM is adjusted; implement consistent handling for 0 values.
  - Provide guidance for data users on interpreting fuse_status and observations related to lightning damage, and how post-strike status was determined.