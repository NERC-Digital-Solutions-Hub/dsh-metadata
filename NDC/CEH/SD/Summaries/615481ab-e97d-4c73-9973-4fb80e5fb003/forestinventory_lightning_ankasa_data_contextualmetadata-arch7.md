# Forest inventory and lightning strikes data from Ankasa Conservation area, Ghana, from 2018-2021

## Overview
- Two CSV datasets from the Ankasa Conservation Area, Ghana (2018–2021) detailing forest inventory and lightning strikes.
- Forest_inventory_AnkasaGhana_2018_2021.csv: measurements on 2,589 trees and 32 lianas across 50 one-hectare plots in a wet/moist evergreen forest with high diversity.
- Lightning_strikes_Datasummary_Ankasa_2018_2021.csv: subset of trees from the above inventory that were struck by lightning; includes species, diameter, post-strike status, fuse status, and observations. Data cover 4 lightning strikes; data collection occurred June 2018–July 2021, with 2019 census interrupted by COVID-19. Part of the NERC project “Lightning: An invisible driver of tree mortality in the tropics?” (Grant NE/P001564/1).

## Data contents

- Forest_inventory_AnkasaGhana_2018_2021.csv
  - Tree_id: original field tag number for the stem
  - census_date: date of field measurement
  - POM: point of measurement (cm); typically 130 cm but adjusted to avoid buttress/deformity
  - D: diameter (cm) at POM; 0 if dead and not measured
  - Tree_status: alive/dead status codes (e.g., A = alive, D = dead) with subcodes for condition (e.g., AN, AB, AH, AUP, AD, etc.)
- Lightning_strikes_Datasummary_Ankasa_2018_2021.csv
  - Country, Site, Plot: location identifiers
  - Tree_id: original field tag number
  - Species: taxonomic identification
  - census_strike_date: date of census when lightning marks were observed
  - POM_strike: diameter at POM on strike date
  - D_strike: diameter at POM on strike date; 0 if dead and not measured
  - Tree_status_after: status after strike (codes similar to Tree_status)
  - Fuse_status: fuse condition at strike date
  - Observations_after: field observations after strike

## Data collection methods

- Study area: 50-hectare plot area, divided into 50 one-hectare plots.
- Target trees: stems ≥25 cm diameter at 1.3 m (or above buttresses); tagged and measured per census; notes on living status and damage mode (e.g., uprooted, hollow).
- Measurements: diameter and status recorded; missing values flagged and, if possible, resolved via field notes or resurvey.
- Lightning detection: each measured tree installed a Rogowski Coil sensor to detect lightning strikes non-invasively; quick visual checks of fuse to identify strikes; record electrical conductivity and general damage (e.g., trunk marks, canopy dieback).
- Quality control: unit error checks; ambiguous values flagged for review; resurvey attempted when possible.
- Temporal coverage: June 2018–July 2021; 2019 census affected by COVID-19.

## Data structure and field-level details

- Forest_inventory_AnkasaGhana_2018_2021.csv
  - D and POM values linked to measurement position; D=0 when dead and not measured
  - Tree_status uses codes indicating alive/dead and sub-conditions (e.g., AL, ABH, AUP, DL, DS, DH, etc.)
- Lightning_strikes_Datasummary_Ankasa_2018_2021.csv
  - Tree_status_after reflects post-strike condition using the same code scheme
  - Observations_after captures post-strike observations such as damage or mortality indicators

## GIS-relevant considerations

- Spatial linkage: Plot and Tree_id provide a basis to map tree-level attributes and mortality events within the 50-ha study area.
- Temporal analysis: census_date and census_strike_date enable time-series mapping of growth, health status, and lightning-induced mortality.
- Data integration: join Forest_inventory and Lightning_strikes datasets via Tree_id to analyze how lightning events relate to subsequent tree outcomes.
- Attribute-rich mapping: use D, Tree_status, and Fuse_status to create thematic layers (e.g., live vs. dead trees, damage type, post-strike status).

## Quality, limitations, and cautions

- Missing values exist where field records were ambiguous or incomplete; some errors flagged for future review.
- 2019 census disrupted due to the COVID-19 pandemic, affecting continuous temporal coverage.
- Data complexity: multiple status codes require careful interpretation; D=0 when not measured for dead trees.

## Provenance and context

- Collected as part of a broader study on lightning as a driver of tropical tree mortality.
- Sensor-based lightning detection (Rogowski Coil) implemented to identify strike events without harming trees.