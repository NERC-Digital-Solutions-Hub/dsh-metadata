# F3UES_birdpoints2013.zip dataset

## Overview and aim
- Part of the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project within the Biodiversity and Ecosystem Service Sustainability (BESS) framework.
- Objective: characterise variation in breeding bird fauna across urban forms in Luton, Bedford, and Milton Keynes, defined by green space versus sealed built cover; also assess birds detectable at times of day when people are more active, recording observer presence.

## Project and contact information
- Survey design and implementation led by Gavin Siriwardena and Kate Plummer (British Trust for Ornithology, BTO).
- Contact: gavin.siriwardena@bto.org; kate.plummer@bto.org
- Funding: grant NE/J015067/1; project page: http://bess-urban.group.shef.ac.uk/

## Survey organization and timing
- Survey period: May–August 2013.
- Area: Bedford, Luton, Milton Keynes, UK.
- Tile-based design: 500 m × 500 m tiles; 116 tiles randomly selected using stratified design.
- Survey points per tile: four points per tile, located ≥ 200 m apart and ≥ 100 m from tile edges; some points inaccessible and excluded from survey.

## Survey methods and data collection
- Birds
  - Method: 10-minute point counts at predefined survey points.
  - Frequency: tiles visited six or seven times; two visits between 06:00–10:00 (May–June) for morning abundances; remaining visits monthly between 10:00–18:00 for afternoon abundances.
  - During each visit: record all birds within 10 m (potential disturbance) and then conduct a 10-minute observation, splitting counts into distance bands (0–20 m, 20–40 m, 40–60 m, 60–100 m, 100–200 m) and by singing vs non-singing, plus birds in flight.
  - Best estimate: when total present differed from the sum of recorded counts.
- People and other wildlife
  - Observers counted people within 200 m during the 10-minute period, categorized by activity (e.g., children, dog walking, working).
  - Opportunistic, non-target observations of mammals and butterflies recorded (not core survey aims).
- Conditions and quality control
  - Weather data captured: wind (Beaufort 0–6), rain (none/light/shower), cloud cover, visibility, and noise.
  - Surveys not conducted in heavy rain or high winds.
  - Data input consolidated by multiple staff; dataset was error-checked and validated.

## Data structure and accessibility
- Two linked dataframes in the dataset:
  - FU3ES_birdpoints2013_obsdata.csv: bird observation counts for each 10-minute point count.
  - FU3ES_birdpoints2013_surveydata.csv: survey details for each 10-minute point count.
- Unique identifier (pcid) links the two dataframes (format: year_tile_visit_point).
- Missing data denoted as NA.
- Data are organized with extensive variables:
  - Bird data include spcode (2-letter species code), species name, and detailed counts by minute blocks (mins 1–2, 3–4, 5–6, 7–8, 9–10), distance bands (20–200 m) and categories (singing, non-singing, in flight).
  - Survey data include city, observer, tile, visit, point, month, time of day (am/pm), date, start time, weather metrics (wind, rain, cloud, visibility, noise), and counts by activity categories (children, commuting, cycling, dogwalking, exercising, leisure, parent/child, shopping, working, walking, other) plus opportunistic counts (butterfly, cat, deer, fox, rabbit, rat, squirrel).
- Supporting data: tile locations with OSGB 1936 coordinates (F3UES_birdsurvey_tile_locations.csv).
- Species glossary: Table 4 provides codes and common names for all species observed, including a comprehensive list of British birds (e.g., BTO codes like BT Blue Tit, CH Chaffinch, etc.).
- Data formats: two CSV files within the F3UES_birdpoints2013.zip dataset; associated metadata describes variables and coding.

## Data management and use for monitoring
- Data were created to be stored and uploaded to appropriate portals, aligned with standardised approaches for environmental monitoring.
- Outputs anticipated as clear formats (reports, maps, and charts) to support scrutiny of environmental health and policy performance over time.
- Aimed to increase the value of the datasets by enabling integration with other data sources and to provide access to underlying data for broader reuse.

## Practical notes for analysts
- Spatial scope defined by 116 tiles; some survey points were inaccessible and omitted.
- Data include both observed birds (with detailed spatial-temporal counts) and observer/environmental context (weather, human activity).
- The dataset enables analyses of:
  - Variation in breeding bird presence across urban form and times of day.
  - Detectability differences by distance bands and singing vs non-singing behavior.
  - Relationship between human activity and bird detections.
- A robust key (pcid) allows merging bird observations with survey details for integrated analyses.