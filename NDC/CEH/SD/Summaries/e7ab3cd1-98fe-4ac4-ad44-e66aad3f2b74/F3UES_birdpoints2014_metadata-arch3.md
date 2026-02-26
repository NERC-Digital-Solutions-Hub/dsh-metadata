# F3UES_birdpoints2014 data description

- Project context: Data from the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project, part of the Biodiversity and Ecosystem Service Sustainability (BESS) framework, focusing on breeding bird variation across urban forms in the Bedfordshire towns of Luton, Bedford, and Milton Keynes; also records numbers of people observed during surveys.
- Organisation and leadership: Survey design and implementation led by Gavin Siriwardena and Kate Plummer of the British Trust for Ornithology; contact details provided; institutional address listed.

## Survey organisation and scope

- Time and place: Data collected May–June 2014 in Bedford, Luton, and Milton Keynes, UK.
- Sampling design: 500m × 500m grid tiles; 116 tiles randomly selected for surveying using stratified sampling to represent urban greenspace variation and built cover; some survey points were inaccessible and removed from the dataset.
- Observers and data consolidation: Multiple inputters collected data; the complete dataset was error-checked and validated.

## Survey methods

- Bird surveys:
  - Point counts conducted at four survey points per tile, at least 200m apart and at least 100m from tile edges.
  - Two visits per tile, 06:00–10:00, in May and June.
  - Each visit: ten-minute counts at all points in random order; birds seen or heard within 10m (and within larger distance bands) recorded; singing and non-singing birds tracked separately.
  - Best estimate recorded when counts differed from the total presence.
- Human presence surveys:
  - Counts of people within 200m of each survey point, categorized by activity type (e.g., children, dog walkers, working, etc.).
- Environmental and survey conditions:
  - Start time, weather (Beaufort wind, rain, cloud cover, visibility), and noise levels recorded; surveys not conducted in heavy rain or high winds.
- Data handling:
  - Field data input collected by multiple individuals, then merged, error-checked, and validated into the final dataset.

## Data description and structure

- Data files:
  - FU3ES_birdpoints2014_obsdata.csv: Bird observations per 10-minute point count.
  - FU3ES_birdpoints2014_surveydata.csv: Other survey details per 10-minute point count.
- Key identifiers:
  - pcid: Unique identifier for each 10-minute point count (year_tile_visit_point format); used to merge the two dataframes.
  - Missing data is coded as NA.
- Bird observation variables (Table 1):
  - Spcode/species, counts by time windows (mins 1–2, 3–4, 5–6, 7–8, 9–10) across distance bands (0–20m, 20–40m, 40–60m, 60–100m, 100–200m) and in flight; categories include both singing and non-singing birds.
  - Variables also include approach, bestest (best estimate when totals differ), and a range of distance-band-specific counts for both singing and non-singing birds.
- Survey detail variables (Table 2):
  - City, observer, tile, visit, point, month, time of day, date/time, wind, rain, cloud cover, visibility, temperature, noise.
  - Human activity counts by category: children, commuting, cycling, dogwalking, exercise, leisure, parent/child, shopping, working, walking, and an “other” category.
- Supporting data (Table 3):
  - Tile locations with tile ID, city, OSGB eastings and northings (grid-centre coordinates) for each 500m × 500m tile.
- Species glossary (Table 4):
  - A mapping of BTO 2-letter codes to full common names for all species observed in the dataset (e.g., BT = Blue Tit, WL = Willow Warbler, etc.).

## Data governance, access, and interoperability

- Data structure for integration:
  - Two linked dataframes using the pcid key allow combining bird counts with survey context (time, weather, and human activity).
- Metadata and traceability:
  - Tile center coordinates provided separately; a clear data dictionary describes each variable, supporting reproducibility and external use.
- Data quality considerations:
  - The dataset acknowledges potential gaps due to inaccessibility of some survey points and weather-related survey cancellations; data are accompanied by a clear data consolidation and validation workflow.

## Relevance for monitoring frameworks

- Measured indicators:
  - Breeding bird abundance and apparent species richness per tile.
  - Spatial variation across urban form (greenspace vs sealed/built cover) and the influence of urban structure on bird communities.
  - Temporal and detectability covariates (time of day, weather, wind, rain, noise) and human activity near survey points.
- Data for policy evaluation and decision-making:
  - Structured, metadata-rich data suitable for assessing environmental health in urban areas and informing future urban biodiversity strategies.
- Potential data-use considerations:
  - Data sharing is facilitated through clearly defined data products; however, accessibility of some survey points and the need to interpret multiple distance/time-band figures may require careful analysis design.
- Data provenance and openness:
  - Datasets are described with explicit file names and variable definitions, enabling reproducibility and integration with other urban ecosystem service assessments.