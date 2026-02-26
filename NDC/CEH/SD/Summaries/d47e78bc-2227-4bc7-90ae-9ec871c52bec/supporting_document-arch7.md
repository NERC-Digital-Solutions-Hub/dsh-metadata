# Location of lightning strikes in Nyungwe National Park, Rwanda, with associated strike-level and treelevel attributes and photographs.

## Overview
- Document describes the location of lightning strikes in Nyungwe National Park, Rwanda, with associated strike-level and tree-level attributes and photographs.
- Study covered 23.3 km of trails around Uwinka station in June 2022; some trails resurveyed in October 2023.
- Focus on canopy disturbances indicative of flashover damage and identification of presumptive direct-strike trees for detailed surveys.
- Data collected include strike locations, strike-level surveys, and tree-level surveys, with accompanying photographs.

## Sampling regime
- Walking 23.3 km of trails, largely on trails accessible from Uwinka station, June 2022; majority of accessible trails surveyed.
- Canopy disturbances (clusters of dead/damaged trees) inspected for visual flashover damage patterns.
- If a tree showed potential flashover damage to two or more neighbors, it and nearby trees (DBH > 50 cm within the strike area) surveyed in detail.
- Subset of trails resurveyed in October 2023; existing strike locations revisited and new disturbances surveyed.
- Photographs taken at a subset of locations, mostly during 2023 resurveys.

## Collection methods
- Each potential strike assigned a unique StrikeID; GPS location recorded.
- Qualitative confidence assigned whether canopy disturbance is due to lightning, using damage-pattern references from remote lightning location data (Panama) for assessment.
- Recorded counts by size class (<10 cm, 10-30 cm, 30-50 cm, >50 cm) for damaged and dead trees; noted open vs. closed canopy and topographic position (ridge, slope, valley).
- For tree-level surveys: crown dieback percentage and crown loss (branch volume loss) estimated; tree height and DBH measured (or estimated in 2023); species identified to finest taxonomic resolution possible.

## Fieldwork instrumentation
- Strike locations recorded with Garmin Etrex 22X handheld GPS.
- DBH measured with 5 m or 10 m diameter tapes.
- Tree height measured with a Nikon Forestry Pro II laser range finder.

## Nature and units of recorded values
- Strike_locations.csv
  - StrikeID
  - Longitude (decimal, WGS84)
  - Latitude (decimal, WGS84)
- Strike_surveys.csv
  - StrikeID
  - QualitativeAssessment (Yes = confident strike; Maybe = potential strike with lower confidence)
  - YearFound (2022 or 2023)
  - TopoCat (ridge, slope, valley)
  - ForestType (open forest or closed canopy)
  - Damaged_total
  - Dead_total
  - Damaged_1-10cm
  - Dead_1_10cm
  - LaggedDead_1_10cm
  - Damaged_10-30cm
  - Dead_10-30cm
  - LaggedDead_10-30cm
  - Damaged_30-50cm
  - Dead_30-50cm
  - LaggedDead_30-50cm
  - Damaged_ov50cm
  - Dead_ov50cm
  - LaggedDead_ov50cm
  - Notes
- Tree_surveys.csv
  - StrikeID
  - TreeID
  - YearFound (2022 or 2023)
  - Genus
  - Species
  - DBH (cm)
  - TreeHeight (m)
  - Dieback_initial (percent leaf-volume loss; estimated to nearest 5%)
  - CrownForm_initial (0–5 scale; 5 = nearly fully intact)
  - Dieback_23 (2023 dieback estimate)
  - CrownForm_23 (2023 crown form estimate)
  - Notes
- Additional structure
  - Each StrikeID uniquely identifies a strike event; TreeSurveys linked via TreeID within StrikeID.
  - Photograph files are prefixed with the strike-level identifier (e.g., T15_1 for strike T15).

## Data structure and linkage
- Strike_locations.csv provides geographic coordinates for each strike.
- Strike_surveys.csv provides strike-level metrics and contextual factors (topography, forest type, damage counts by size class).
- Tree_surveys.csv provides tree-level measurements nested under StrikeID and TreeID.
- Photographs are stored with filenames that begin with the corresponding StrikeID, enabling visual association with survey data.

## Quality control and provenance
- Data input cross-checked against original field data sheets to ensure accuracy.

## Usage notes for GIS applications
- Geospatial mapping: join Strike_locations.csv with Strike_surveys.csv on StrikeID; further join to Tree_surveys.csv by StrikeID and TreeID to map tree-level damages.
- Temporal analysis: distinguish 2022 vs. 2023 findings using YearFound and Dieback/CrownForm changes.
- Classification: use TopoCat and ForestType to analyze spatial patterns of damage relative to terrain and canopy openness.
- Data enrichment: photographs linked via StrikeID can be used for visual validation of strike classifications and damage patterns.