# About the survey

- Purpose and framework
  - Data collected as part of the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project, within the Biodiversity and Ecosystem Service Sustainability (BESS) framework.
  - Objective: characterize variation in breeding bird fauna across urban forms in the Luton, Bedford, and Milton Keynes area, focusing on green space vs built (sealed) cover; also recorded the number of people observed during each observation period.

- Survey organisation
  - Team: Gavin Siriwardena and Kate Plummer (British Trust for Ornithology) designed and implemented the survey.
  - Contact references provided for the BTO.

- Spatial design and study area
  - Timeframe: May–June 2014.
  - Area: Bedford, Luton, Milton Keynes, UK.
  - Sampling design: a 500m × 500m grid defined the study area; 116 tiles were randomly selected from this grid using stratified sampling.
  - Within each tile: four survey points selected using GIS, each at least 200m apart and at least 100m from tile edges.
  - Inaccessible points were later excluded; such points do not appear in the dataset.
  - GIS relevance: tile centers and locations are provided; spatial context is tied to the 500m grid and green space vs built cover.

- Survey methods
  - Birds: two visits per tile (May and June), between 06:00 and 10:00; 10-minute point counts at all survey points within a tile in random order.
    - On arrival: record all birds within 10m (potential disturbance) and then observe for 10 minutes.
    - Distances: counts recorded in distance bands (0–20m, 20–40m, 40–60m, 60–100m, 100–200m) and in flight.
    - Singing vs non-singing birds recorded separately; a best-estimate count is used if totals differ from sums of observed birds.
  - People: counted within 200m of each survey point, categorized by activity (children, commuting, cycling, dog walking, exercising, leisure, parent/child, shopping, working, walking, other).
  - Conditions: start time logged; weather (wind, rain, cloud cover, visibility, noise) recorded; surveys avoided in heavy rain or high winds.
  - Data consolidation: multiple inputters digitized field sheets; dataset was error-checked and validated.

- Data structure and contents
  - Dataset: F3UES_birdpoints2014.zip containing two dataframes.
    - Dataframe 1: bird observations for each 10-minute point count.
    - Dataframe 2: other survey details for each 10-minute point count.
  - Key linking field: pcid (unique 10-minute point count identifier, format year_tile_visit_point) to merge the two dataframes.
  - Missing data: represented as NA.
  - Data tables and variables
    - Table 1 (obsdata): variables include pcid, spcode (BTO 2-letter code), species, common name, and detailed count data across time blocks (minutes 1–2, 3–4, 5–6, 7–8, 9–10), for each distance band (20m, 40m, 60m, 100m, 200m) and for singing, non-singing, and in flight, plus bestest estimates.
    - Table 2 (surveydata): variables include pcid, city (BF, LT, MK), observer, tile, visit, point, month, tod (time of day), date, time, wind, rain, cloud, visibility, temperature, noise, and counts of people by activity category (children, commuting, cycling, dogwalking, exercising, leisure, parent/child, shopping, working, walking, other).
  - Supporting tile information
    - F3UES_birdsurvey_tile_locations.csv: centre coordinates for each 500m × 500m tile (OSGB 1936), with tile_id and city.
  - Spatial reference
    - Tile centers provided in OSGB 1936 / British National Grid. This enables GIS-ready joins to the bird data via tile identifiers and easy reprojection if needed.

- Species reference
  - Glossary (Table 4) provides a full list of all bird species by BTO code and common name, covering a wide range of frequently observed species in UK urban environments.

- Data integration and GIS use
  - pcid enables merging of observation data with survey context (environmental conditions, observer, time, and people counts).
  - Spatial mapping opportunities:
    - Map bird counts and sightings by tile across the 116 tiles.
    - Overlay with tile-level spatial context (greenspace vs sealed surfaces) using the tile location data.
    - Create GIS-derived products such as choropleth maps of bird abundance by tile, species richness by tile, and effort-adjusted bird metrics.
    - Reproject OSGB36 coordinates to other CRSs for compatibility with existing GIS tools.
  - Data quality considerations for GIS:
    - Some tiles/points were inaccessible and not surveyed.
    - Data cleaning needed due to multiple inputters; validated but should be checked during integration.
    - NA values indicate missing measurements, which should be handled in spatial analyses.

- Organisation and contact
  - Survey coordination and dataset management attributed to the British Trust for Ornithology, with contact details provided for primary researchers.