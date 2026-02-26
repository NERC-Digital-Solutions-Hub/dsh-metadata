# Description Location of lightning strikes in Nyungwe National Park, Rwanda, with associated strike-level and treelevel attributes and photographs.

## Overview
- Documents location and effects of lightning strikes in Nyungwe National Park, Rwanda, linked to strike-level and tree-level data and photos.
- Based on 2022 and 2023 field surveys along a defined trail network, focusing on canopy disturbances indicative of flashover damage.
- Produces standardized outputs (strike-level and tree-level datasets) for environmental monitoring and policy evaluation.

## Sampling regime
- Surveyed 23.3 km of trails near Uwinka station in Nyungwe National Park in June 2022; majority of trails accessible from the station were covered.
- Looked for canopy disturbances (dead/damaged trees in clusters) to identify potential flashover damage with directional patterns.
- Presumptively directly struck trees identified as the canopy tree at the center of observed flashover damage.
- Conducted tree-level surveys for the strike area on trees with diameter at breast height (DBH) > 50 cm within the strike zone.
- A subset of trails were resurveyed in October 2023 to revisit known strike locations and survey new disturbances.
- Photographs were taken at a subset of strike locations, mainly during 2023 resurveys.

## Collection methods and data collection
- Each potential strike assigned a unique StrikeID and location recorded with GPS (WGS84).
- Qualitative confidence of lightning-caused canopy disturbance assessed using patterns referenced to a remote lightning location system from Panama.
- Recorded whether the forest was open canopy or closed canopy, and the topographic position of the strike (ridge, slope, valley).
- For trees in the strike area, counted damage/killed trees by size class: <10 cm, 10–30 cm, 30–50 cm, >50 cm.
- Lagged mortality captured as the number of trees in each size class that were alive in 2022 but dead by 2023.
- For tree-level surveys (selected trees): measured DBH and height where possible; estimated crown dieback (percent leaf-volume loss) and crown loss (percent branch-volume loss).
- 2023 surveys sometimes used size-class estimates instead of exact measurements.
- Trees identified to the finest taxonomic resolution possible.

## Fieldwork instrumentation
- Strike locations recorded with Garmin Etrex 22X handheld GPS.
- Tree DBH measured with 5 m or 10 m diameter tapes.
- Tree height measured with a Nikon Forestry Pro II laser range finder.

## Nature and units of recorded values
- Strike_locations.csv
  - StrikeID: strike-level identifier
  - Longitude, Latitude: decimal degrees (WGS84)

- Strike_surveys.csv
  - StrikeID: strike-level identifier
  - QualitativeAssessment: yes if confident strike, maybe if potential strike with lower confidence
  - YearFound: 2022 or 2023
  - TopoCat: ridge, slope, valley
  - ForestType: open forest or closed canopy
  - Damaged_total, Dead_total: counts of damaged and killed trees
  - Damaged_1-10cm, Dead_1_10cm; LaggedDead_1_10cm
  - Damaged_10-30cm, Dead_10-30cm; LaggedDead_10-30cm
  - Damaged_30-50cm, Dead_30-50cm; LaggedDead_30-50cm
  - Damaged_ov50cm, Dead_ov50cm; LaggedDead_ov50cm
  - Notes: strike-level notes

- Tree_surveys.csv
  - StrikeID: strike-level identifier
  - TreeID: tree-level identifier within strike
  - YearFound: 2022 or 2023
  - Genus, Species: taxonomic identification (genus/species; indeterminate if not identified)
  - DBH: diameter at breast height (cm)
  - TreeHeight: height (m)
  - Dieback_initial: initial dieback percentage
  - CrownForm_initial: index of crown/branch volume remaining
  - Dieback_23, CrownForm_23: 2023 estimates
  - Notes: any tree-level notes

- Photography
  - Photo files linked to strike-level identifiers; filenames prefixed with the StrikeID (e.g., T15_1 for strike T15)

## Quality control and data structure
- Data cross-checked against original field data sheets to ensure accuracy.
- Data structure comprises three linked datasets:
  - Strike_locations.csv (location-level data)
  - Strike_surveys.csv (strike-level metrics)
  - Tree_surveys.csv (tree-level metrics)
- StrikeID serves as the key to join strike-level and tree-level data.
- Photographs are organized and named to correspond with strike identifiers for traceability.

## Usage and data management
- Outputs are stored and uploaded to appropriate data portals to enable reuse and accessibility for environmental monitoring and policy assessment.
- Designed to support analysis of environmental health indicators related to lightning disturbance and to facilitate data integration with other environmental datasets.