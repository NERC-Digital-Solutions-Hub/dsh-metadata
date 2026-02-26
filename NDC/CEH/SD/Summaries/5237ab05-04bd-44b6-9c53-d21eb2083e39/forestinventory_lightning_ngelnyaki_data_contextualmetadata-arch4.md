# Forest inventory and lightning strikes data from the Ngel Nyaki forest, Nigeria, from 2018-2021

## Overview
- Datasets from a 40-hectare forest dynamic plot at Ngel Nyaki, south-eastern Nigeria (submontane, elevation 1,588–1,690 m).
- Time frame: June 2018 – July 2021.
- Part of the NERC project Lightning: An invisible driver of tree mortality in the tropics? (Grant NE/P001564/1).
- Data assets include:
  - Forest_inventory_NgelNyaki_Nigeria_2018_2021.csv: measurements on 2,552 individual trees and their living status or mode of death.
  - Lightning_strikes_Datasummary_NgelNyaki_2018_2021.csv: subset of trees that were struck by lightning (23 strikes recorded).
- ForestGEO network affiliation; data collected as part of ongoing census and monitoring activities.

## Data content
- Forest_inventory file:
  - Records stem diameter (D) and status for each tree with a Tag/Tree_id across census dates.
  - Includes trees and lianas meeting a minimum size criterion (stem diameter at 1.3 m ≥ 25 cm or buttressed/deformed cases).
  - Status codes indicate alive or dead, with multiple sub-statuses (e.g., broken, hollow, dying productivity, fallen, uprooted, vanished, presumed dead, etc.).
- Lightning_strikes file:
  - Contains trees identified in the main inventory that experienced lightning strikes.
  - Includes species, diameter at strike, status before strike, fuse condition, and post-strike status.
  - Records span the same time period and site as the main inventory; 23 observed lightning strikes across trees.

## Data collection and methods
- Field procedures:
  - Complete tagging and measurement of all qualifying trees in each census.
  - Notes on living status and death modes (e.g., uprooted, standing, hollow, broken).
  - Custom Rogowski Coil sensors installed to detect lightning strikes without damaging trees; supplementary field notes on coil condition and fuse status.
  - Electrical conductivity recorded; post-strike observations documented (tree and surroundings: canopy gaps, sapling mortality, etc.).
- Quality controls:
  - Checks for unit errors; ambiguous values flagged and cross-checked with field notes or resurvey when possible.
  - If resurvey not possible, errors flagged for future review.
- Data completeness and issues:
  - Missing values exist due to ambiguous field records or unmeasured diameters (e.g., if tree dead).
  - POM (point of measurement) generally set at 130 cm; adjustments made for buttressed or deformed stems.
  - Post-strike data rely on census dates and fuse observations to determine strike impact.

## Data structure and fields
- Forest_inventory_NgelNyaki_Nigeria_2018_2021.csv:
  - Tree_id: original tag number.
  - census_date: date of field measurement.
  - POM: point of measurement (cm); typically 130 cm, adjusted for buttress/deformity; 0 if dead and not measured.
  - D: diameter (cm) at POM; 0 if dead and not measured.
  - Tree_status: coded alive/dead statuses (e.g., AN, AB, ABD, etc.).
- Lightning_strikes_Datasummary_NgelNyaki_2018_2021.csv:
  - Country, Site, Plot, Tree_id, Species.
  - census_strike_date: date/month/year of census when tree had lightning marks.
  - POM_strike: diameter measurement at strike date (cm).
  - D_strike: diameter at strike date (cm); 0 if not measured due to dead tree.
  - Tree_status_strike: status at census prior to strike (same coding as Tree_status).
  - Fuse_status: fuse condition at strike date.
  - Observations_strikes: notes from field prior to strike.
  - Tree_status_after: status at latest census after strike.
  - Observations_after: post-strike observations.

## Data quality, limitations, and governance
- Strengths for data governance:
  - Clear linkage between pre-strike and post-strike status for mortality analyses.
  - Standardized status codes enabling comparability across censuses and with other ForestGEO data.
  - Detailed metadata on measurement protocols, including POM adjustments and sensor deployment.
- Limitations and caveats:
  - Missing values where field notes were ambiguous or measurements were not possible.
  - Potential data gaps due to resurvey constraints or unresolved ambiguities in field records.
  - Some status categories depend on interpretation of field observations (e.g., “presumed dead,” “lost,” or “vanished”).
- Relevance to data leadership considerations:
  - Highlights importance of robust metadata, standardized status coding, and explicit documentation of data collection methods.
  - Illustrates challenges of data completeness in long-term ecological datasets and the need for clear provenance and quality checks.
  - Demonstrates how linked datasets (inventory + strike data) can support investigations into drivers of mortality (lightning) in tropical forests.

## Access, provenance, and usage notes
- Data are provided as two CSV files accompanying the study.
- Data provenance includes field journals, Rogowski Coil sensor data, and standard ForestGEO census procedures.
- Suitable for analyses on lightning as a mortality driver, tree survival analysis, diameter and status progression, and cross-site comparisons within ForestGEO networks.
- Users should account for missing values, measurement adjustments (POM), and the coding scheme for living/dead statuses when conducting analyses.