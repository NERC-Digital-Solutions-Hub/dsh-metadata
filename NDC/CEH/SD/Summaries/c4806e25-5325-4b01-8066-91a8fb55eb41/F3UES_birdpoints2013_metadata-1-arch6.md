# F3UES_birdpoints2013 Data Description

## Overview
- Data from the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project, within the Biodiversity and Ecosystem Service Sustainability (BESS) framework.
- Aimed to characterise variation in breeding bird fauna across urban forms in Bedford, Luton, and Milton Keynes, and to investigate detectability at different times of day.
- Also records the number of people observed during each observation period.

## Survey Organisation
- Design and implementation led by Gavin Siriwardena and Kate Plummer (British Trust for Ornithology).
- Contact details provided for follow-up.

## Survey Methods
- Bird surveying: Point count method at predefined survey points. Each “tile” (500m × 500m) contains four survey points; each tile surveyed six–seven times between May and August 2013.
- Timing: Morning counts (06:00–10:00) collected in May–June to measure morning abundance; otherwise, monthly visits (10:00–18:00) for afternoon abundance.
- Data collection: At each point, a 10-minute observation; birds seen or heard within 10 m were recorded, with counts broken into two-minute intervals across distance bands (0–20 m, 20–40 m, 40–60 m, 60–100 m, 100–200 m). Birds were categorized as singing, non-singing, or in flight; a best estimate was used when counts differed from the sum of recorded birds.
- Survey location: 116 tiles randomly selected from a 500m × 500m grid within Bedford, Luton, and Milton Keynes; four points per tile, ≥200 m apart and ≥100 m from tile edges; some points were inaccessible and not surveyed.
- People observations: Number of people seen within 200 m of the survey point, categorized by activity/type (e.g., children, dog walking, working).
- Other incidental observations: Opportunistic counts of mammals and butterflies near survey points.
- Survey conditions: Start time, wind (Beaufort 0–6), rain (none/light/shower), cloud cover, visibility, and noise levels recorded; surveys not conducted in heavy rain or high winds.
- Data handling: Multiple inputters digitally entered field data; dataset was error-checked and validated.

## Data Structure and Key Variables
- Two linked dataframes:
  - FU3ES_birdpoints2013_obsdata.csv: Bird observations for each 10-minute point count.
  - FU3ES_birdpoints2013_surveydata.csv: Additional survey details for each 10-minute observation.
- Key identifier: pcid (unique point count id; format year_tile_visit_point) used to merge the two dataframes.
- Data types and fields:
  - Observations dataframe: spcode (two-letter BTO species code), species (common name), approach, bestest, and numerous count variables by two-minute intervals (mins 1–2, 3–4, 5–6, 7–8, 9–10) across distance bands (20, 40, 60, 100, 200 m) for singing/non-singing and in flight.
  - Survey details dataframe: city, observer, tile, visit, point, month, tod (time of day: am/pm), date, time, wind, rain, cloud, vis, temp, noise; counts of people by category (children, commuting, cycling, dogwalking, exercise, leisure, parentchild, shopping, working, walking, other); opportunistic counts for butterflies and several mammals.
- Supporting data: Tile center coordinates (OSGB 1936) in F3UES_birdsurvey_tile_locations.csv (tile, city, easting, northing).
- Glossary: Table 4 provides a comprehensive mapping of two-letter species codes to common bird names (extensive list of species codes included).

## Data Quality and Notes
- Missing data represented as NA.
- Some survey points were inaccessible and not surveyed.
- Data consolidated from multiple inputters with validation steps to ensure consistency.

## Potential Uses for Data Support
- Build data products enabling self-serve exploration of urban bird patterns (e.g., dashboards combining bird counts with environmental/temporal variables).
- Integrate bird observations with survey conditions and urban form metrics to analyze detection probabilities, species richness, and abundance across time of day and distance.
- Support policy or planning analyses in urban biodiversity by providing a ready-to-merge dataset (pcid as the linking key) with rich metadata and a species code glossary.