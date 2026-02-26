# About the survey

- Purpose: The F3UES project surveys breeding birds to characterize variation across urban forms in Luton, Bedford, and Milton Keynes, with attention to birds detectable at times of day when people are active. Observers also record the number of people observed during each observation period.
- Context: Part of the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) within the Biodiversity and Ecosystem Service Sustainability (BESS) framework.

## Survey design and organization

- Lead and design: Gavin Siriwardena and Kate Plummer of the British Trust for Ornithology (BTO).
- Spatial design: Data collected on 116 tiles defined as 500m × 500m grid cells within the three cities; tiles selected via stratified sampling based on greenspace vs built cover.
- Field setup: Four survey points per tile, located ≥ 200m apart and ≥ 100m from tile edges; some points inaccessible and not surveyed.
- Sampling period: May–August 2013; each tile visited six or seven times.

## Data collection methods

- Bird surveying method:
  - Point count approach: 10-minute counts at each survey point, with random order of points within a tile.
  - Time of day: Two visits between 06:00–10:00 (morning) in May–June; remaining visits between 10:00–18:00 (afternoon).
  - Distance bands: Birds observed within 0–20m, 20–40m, 40–60m, 60–100m, 100–200m, plus in flight; birds recorded as singing, calling, or seen (not singing); observers provide a best estimate if totals differ from summed counts.
  - Data captured: For each observation, species (two-letter code and common name), whether observed during approach, and counts by the distance/time bands.
- People surveying method:
  - Observers counted people within 200m of the survey point, categorized by activity/status (e.g., children, dog walking, working).
- Other observations:
  - Opportunistic records of mammals and butterflies near the survey point; not formal survey aims.
- Environmental conditions:
  - Start time, weather (Beaufort wind, rain, cloud cover, visibility, noise), and a set of NOT-conducted-in conditions (e.g., heavy rain or high winds).
- Data handling:
  - Multiple data inputters; data were error-checked, validated, and consolidated.

## Data structure and variables

- Two main dataframes in the dataset (F3UES_birdpoints2013.zip):
  - Bird observations dataframe (FU3ES_birdpoints2013_obsdata.csv):
    - Unique point count id: pcid (format year_tile_visit_point).
    - species information: spcode, species; counts broken down by time segments (m12, m34, m56, m78, m910) and by distance bands (20m, 40m, 60m, 100m, 200m) for non-singing (ns) and singing (s) birds, plus in flight (fly).
    - Variables for approach and best estimate (bestest) when totals differ from summed counts.
  - Survey details dataframe (FU3ES_birdpoints2013_surveydata.csv):
    - pcid (linking to observations).
    - Spatial and sampling metadata: city, observer, tile, visit, point, month, tod (time of day: am/pm), date, time.
    - Environmental and contextual variables: wind, rain, cloud, vis, temp, noise.
    - People counts by category: children, commuting, cycling, dogwalking, exercise, leisure, parentchild, shopping, working, walking, other.
    - Opportunistic fauna counts: butterfly, cat, deer, fox, rabbit, rat, squirrel.
- Supporting data:
  - Tile locations: F3UES_birdsurvey_tile_locations.csv with tile, city, easting, northing (OSGB 1936 coordinates) for tile centers.
  - Glossary of species: Table 4 lists codes and common names for bird species present in the dataset.
- Data relationships:
  - Each observation is linked to a pcid, enabling merge of the bird counts with the corresponding survey conditions and human activity data across the two dataframes.

## Data quality, scale, and accessibility

- Data completeness:
  - Some survey points were inaccessible and are not included; missing values are denoted as NA.
- Scale and granularity:
  - Fine-scale, temporally explicit bird counts (per 10-minute observation, across multiple minutes and distance bands) combined with concurrent human activity data and environmental conditions.
- Standardization and provenance:
  - Data collected with standardized point-count protocol; notes on potential variability due to multiple observers and field inputters; weather and time data help mitigate detection biases.
- Metadata and discoverability:
  - Data include a unique pcid for cross-dataset merging; tile coordinates and species glossary facilitate interpretation and reuse.
- Potential analysis considerations for analysts:
  - Examine correlations between urban form (greenspace vs sealed cover) and bird abundance/detectability across times of day.
  - Model detection probability by time of day, distance band, singing vs non-singing, and weather conditions.
  - Investigate human activity context as a potential covariate or confounder for bird detectability.
  - Address data gaps due to inaccessible points and the May–August 2013 time window; consider tile-level random effects to account for spatial structure.

## Summary of potential uses

- Comparative analyses of urban Bird communities across different city greenspace configurations.
- Modelling how detectability and observed abundance vary with time of day, weather, and human activity.
- Integrating species presence/absence and abundance data with detailed environmental and human activity metadata for practical decision-making in urban biodiversity and ecosystem service planning.