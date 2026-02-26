# Description Location of lightning strikes in Nyungwe National Park, Rwanda, with associated strike-level and treelevel attributes and photographs.

## Overview
- Dataset describing lightning strike occurrences in Nyungwe National Park, Rwanda, with associated strike-level and tree-level damage, plus photographs.
- Fieldwork conducted in 2022 and 2023; 23.3 km of trails surveyed in June 2022 (majority from Uwinka station) with subset resurveys in October 2023.

## Sampling regime
- Surveyed canopy disturbances along trails to identify flashover-type damage (defoliation patterns biased in a directional pattern).
- presumptive directly struck tree identified as the canopy tree at the center of observed flashover damage.
- Conducted tree-level surveys for the struck tree and other trees with diameter at breast height (DBH) > 50 cm within the strike area.
- Subset of trails resurveyed in 2023, revisiting existing strike locations and surveying new disturbances.
- Photographs taken at a haphazard subset of strike locations, mainly during 2023 resurveys.

## Data collection and variables
- Each potential strike assigned a unique StrikeID; locations recorded with GPS (WGS84).
- Qualitative confidence in lightning-caused canopy disturbance assessed from damage patterns, using Panama-based reference damage patterns.
- Recorded counts by tree size classes: <10 cm, 10–30 cm, 30–50 cm, >50 cm; forest type (open vs. closed canopy); topographic position (ridge, slope, valley).
- Tree-level surveys record crown dieback (% leaf volume lost) and crown loss (% branch volume lost), plus tree height and DBH (or estimates in 2023); identification to genus/species where possible.
- For 2023 surveys, size class estimates replaced precise DBH/height for some trees.
- YearFound indicates whether data come from 2022 or 2023 surveys; notes captured at strike and tree levels.

## Data files and structure
- Strike_locations.csv: StrikeID; Longitude (WGS84); Latitude (WGS84).
- Strike_surveys.csv: StrikeID; QualitativeAssessment; YearFound; TopoCat (ridge/slope/valley); ForestType (open/closed); Damaged_total; Dead_total; Damaged_1-10cm; Dead_1-10cm; LaggedDead_1-10cm; Damaged_10-30cm; Dead_10-30cm; LaggedDead_10-30cm; Damaged_30-50cm; Dead_30-50cm; LaggedDead_30-50cm; Damaged_ov50cm; Dead_ov50cm; LaggedDead_ov50cm; Notes.
- Tree_surveys.csv: StrikeID; TreeID; YearFound; Genus; Species; DBH; TreeHeight; Dieback_initial; CrownForm_initial; Dieback_23; CrownForm_23; Notes.
- Relationship: StrikeID links strike-level data to tree-level observations.
- Photographs: files prefixed by strike-level identifier (e.g., T15_1 is photo for strike T15).

## Instrumentation and methods
- Strike locations recorded with Garmin Etrex 22X GPS.
- DBH measured with 5 m or 10 m diameter tapes.
- Tree height measured with Nikon Forestry Pro II laser range finder.
- Damage-pattern-based confidence calibrated against remote lightning location data from Panama.

## Data quality and validation
- Data input cross-checked against original field data sheets.

## Temporal scope
- Data collected in 2022 and 2023; 2023 surveys included re-surveys of existing strike locations and new disturbances.

## Limitations and scope notes
- Surveyed trails represent a subset of Nyungwe’s trails; may not capture all strikes across the park.
- 2023 surveys sometimes rely on size-class estimates rather than exact DBH/height.
- Lightning attribution based on qualitative patterns; some uncertainty remains in strike identification.