# F3UES_birdpoints2013 data description

## Overview
- Data from the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project, part of the Biodiversity and Ecosystem Service Sustainability (BESS) framework.
- Aimed to characterize breeding bird variation across urban forms in Bedford, Luton, and Milton Keynes, and to capture birds detectable during peak human activity times.
- Includes both bird counts and accompanying context data (e.g., people observed, weather, and other organisms).

## Survey scope and organization
- Coordinated by Gavin Siriwardena and Kate Plummer (British Trust for Ornithology).
- Study area: Bedford, Luton, Milton Keynes, UK.
- Grid design: 500m × 500m tiles; 116 tiles randomly selected for surveying using stratified design.
- Within each tile: four survey points positioned to represent the range of urban greenspace; some points later inaccessible and thus not surveyed.
- Survey period: May–August 2013; multiple visits per tile and per point.

## Survey methods
- Bird surveying:
  - Point count method with 10-minute observations at each survey point.
  - Morning counts (06:00–10:00) in May–June; afternoon counts (10:00–18:00) for remaining visits.
  - Birds recorded within 10 m (and thus potentially disturbed) and categorized by distance bands: 0–20 m, 20–40 m, 40–60 m, 60–100 m, 100–200 m, plus in flight.
  - Singing vs. non-singing birds recorded; a best-estimate count provided when totals differed from summed observations.
- Human observers:
  - Counts of people within 200 m of the survey point, categorized by activity type (e.g., children, dog walking, working).
- Other fauna:
  - Opportunistic records of mammals and butterflies near survey points (not core survey aims).
- Conditions and data quality:
  - Weather and noise conditions recorded (Beaufort wind, rain, cloud cover, visibility, noise).
  - Data consolidation involved multiple inputters with subsequent error checking and validation.

## Data structure

### Dataframe 1: FU3ES_birdpoints2013_obsdata.csv
- Unique point count observation identifier: pcid (format: year_tile_visit_point).
- Species information: spcode (2-letter BTO code), species (common name).
- Distance-band counts by time segments:
  - Minutes 1–2 (m12_*) for 0–20 m, 20–40 m, 40–60 m, 60–100 m, 100–200 m, and flight.
  - Minutes 3–4 (m34_*) for the same bands.
  - Minutes 5–6 (m56_*) for the same bands.
  - Minutes 7–8 (m78_*) for the same bands.
  - Minutes 9–10 (m910_*) for the same bands.
- Categories include distinguishing singing vs. non-singing birds and in-flight birds.

### Dataframe 2: FU3ES_birdpoints2013_surveydata.csv
- pcid: unique point count id (to merge with obsdata).
- Spatial and temporal context: city, tile, visit, point, month, tod (time of day: am/pm), date, time.
- Environmental and atmospheric conditions: wind (Beaufort), rain, cloud, vis (visibility), temp, noise.
- Human activity counts: children, commuting, cycling, dogwalking, exercise, leisure, parentchild, shopping, working, walking, other.
- Opportunistic fauna counts: butterfly, cat, deer, fox, rabbit, rat, squirrel.

## Supporting spatial data and glossary
- Tile locations: F3UES_birdsurvey_tile_locations.csv
  - tile, city, easting (OSGB 1936 / British National Grid), northing (OSGB 1936).
  - Provides centre-point coordinates for each 500m × 500m tile.
- Species glossary: Table 4 lists scientific/common names and BTO codes for all species present in the dataset.
- Data linkage: A unique pcid enables merging between the bird observations and the corresponding survey details.

## Data quality, processing, and limitations
- Data collected by multiple inputters; dataset underwent error checking and validation after consolidation.
- Some survey points within tiles were inaccessible and thus not surveyed; these points are not present in the dataset.
- Missing data are denoted as NA.
- Spatial data are centered at tile centroids; detailed point-level locations are linked through pcid but precise point coordinates are not provided in the described files beyond tile centers.

## GIS considerations and usage notes
- The dataset is designed for map-based analyses of urban birding patterns in relation to urban form and human activity.
- Spatial resolution is organized around 500m tiles and 200m survey radii around survey points, suitable for urban-scale analyses.
- Integration workflow:
  - Use F3UES_birdsurvey_tile_locations.csv to map tile centers.
  - Link to birdpoints2013_obsdata.csv and birdpoints2013_surveydata.csv via pcid for spatial and contextual analysis.
  - Leverage distance-band and time-of-day counts to create spatially informed species distribution and activity models within urban environments.
- Data useful for comparing bird presence/abundance with green space coverage versus sealed (built) areas, as part of broader urban ecosystem service studies.

## Access, credits, and references
- Project and contact information:
  - Gavin Siriwardena and Kate Plummer, British Trust for Ornithology.
  - Project grant: NE/J015067/1; F3UES (BESS framework).
  - Data repository details and accompanying files referenced in the metadata.