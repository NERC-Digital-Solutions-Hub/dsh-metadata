# Forest inventory and lightning strikes data from Ankasa Conservation area, Ghana, from 2018-2021

## Overview
- Study area: Ankasa Conservation Area, southwestern Ghana, with wet/moist evergreen forest and high diversity.
- Purpose: Data collection to investigate tree mortality and responses, including the role of lightning as a driver.
- Timeframe: Field campaigns from June 2018 to July 2021; 2019 census disrupted by the COVID-19 pandemic.
- Projects: Part of the NERC project “Lightning: An invisible driver of tree mortality in the tropics?” (Grant NE/P001564/1).

## Datasets and contents
- Forest_inventory_AnkasaGhana_2018_2021.csv
  - 50 consecutive 1-hectare forest plots within a 50-ha area.
  - Measurements for 2,589 trees and 32 lianas.
  - Variables include stem diameter, measurement point (POM), and living/dead status (Tree_status) with coded classifications.
  - Focus on trees with DBH ≥ 25 cm at 1.3 m (or above buttresses) and notes on status (e.g., broken, hollow).
- Lightning_strikes_Datasummary_Ankasa_2018_2021.csv
  - Subset of the forest inventory: trees that were struck by lightning.
  - Includes species, diameter, and status after strike, plus fuse status.
  - Records from 4 lightning strike events.
  - Data collected June 2018–July 2021; 2019 census interrupted.

## Data collection methods
- Plot design and census
  - 50-ha area divided into 50 x 1-ha plots.
  - In each census, all trees and lianas ≥25 cm DBH (or 1.3 m height with buttress considerations) tagged and measured; living status and mode of death recorded.
  - Quality controls: unit checks, review of field notes, and resurvey if needed; unresolved ambiguities flagged for future checks.
- Lightning detection
  - Each measured tree fitted with a Rogowski Coil sensor to record lightning strikes non-invasively.
  - Visual verification of fuse status and periodic checks of coil condition and electrical conductivity.
  - Documentation of lightning-related damage (e.g., trunk marks, broken branches, canopy dieback) and post-strike status.

## Data structure and column details
- Forest_inventory_AnkasaGhana_2018_2021.csv
  - Tree_id: field tag number for the stem.
  - census_date: date of field measurement.
  - POM: point of measurement for diameter (cm), typically 130 cm unless adjusted.
  - D: diameter (cm) at POM; 0 if dead and not measured.
  - Tree_status: status code (A = alive, D = dead) with secondary codes indicating condition (e.g., AN, AB, AH, AUP, AD, etc.) and mixtures (e.g., AL, DL, DV, etc.).
- Lightning_strikes_Datasummary_Ankasa_2018_2021.csv
  - Country, Site, Plot: location identifiers.
  - Tree_id: field tag number for the stem.
  - Species: taxonomic identification.
  - census_strike_date: date when lightning strike was observed.
  - POM_strike: diameter measurement at strike date.
  - D_strike: diameter at POM_strike; 0 if dead and not measured.
  - Tree_status_after: status at the census after the strike (same coding system as Forest_inventory).
  - Fuse_status: fuse condition at the census after the strike.
  - Observations_after: notes about observations following the lightning event.

## Data quality and limitations
- Missing values exist where field records were ambiguous or missing; some diameters may be zero if trees were dead and not re-measured.
- 2019 census disruption due to COVID-19 affects temporal continuity.
- Quality controls focus on unit consistency, verification against field notes, and potential resurvey where feasible.

## Potential uses for environmental monitoring and analysis
- Quantify lightning-related tree mortality and damage across species and diameter classes.
- Compare pre- and post-strike status to assess short-term impacts and potential delayed mortality.
- Integrate with other ecological data to explore drivers of mortality and canopy dynamics in tropical forests.
- Enable cross-dataset analysis by linking individual trees in the inventory to lightning strike outcomes.