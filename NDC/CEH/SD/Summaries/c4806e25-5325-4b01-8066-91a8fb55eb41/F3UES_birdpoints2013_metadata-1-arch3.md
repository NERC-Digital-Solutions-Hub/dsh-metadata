# F3UES_birdpoints2013 data description

## Purpose and context
- Part of the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project within the Biodiversity and Ecosystem Service Sustainability (BESS) framework.
- Aimed to characterize variation in breeding bird fauna across urban forms (green space vs. sealed built cover) in Bedford, Luton, and Milton Keynes.
- Also designed to assess birds detectable at times of day when people are active, recording the number of people observed during each observation period.

## Survey organization
- Survey design and implementation led by Gavin Siriwardena and Kate Plummer of the British Trust for Ornithology (BTO).
- Contact information provided for the two organizers.

## Methods

### Bird surveys
- Point count method conducted at pre-defined survey points.
- Each of the tiles was visited six or seven times between May and August 2013.
- Two visits between 06:00 and 10:00 in May and June to measure morning abundances; remaining visits between 10:00 and 18:00 to measure afternoon abundances.
- 10-minute counts per survey point; on approach, birds within 10 m recorded; after disturbance reduction, a 10-minute observation period followed.
- Birds counted across distance bands (0–20 m, 20–40 m, 40–60 m, 60–100 m, 100–200 m) and in flight; singing and non-singing birds recorded separately; a best-estimate field count used if totals differed from the sum of recorded birds.

### Survey location
- Data collected May–August 2013 in 116 grid tiles (500 m × 500 m) randomly selected from a stratified sample across Bedford, Luton, and Milton Keynes.
- Within each tile, four survey points were selected (≥200 m apart, ≥100 m from tile edges) to represent the range of urban greenspace; some points became inaccessible and were not surveyed.
  
### Surveying people
- Observers counted the number of people within 200 m of the survey point during each 10-minute observation, categorized by activity type (e.g., children, dog walking, working).

### Other information
- Opportunistic records of mammals and butterflies near the survey point; included in the dataset but not part of primary aims.

### Survey conditions
- Start time recorded for each 10-minute count.
- Weather conditions recorded at the end of each observation: Beaufort wind, rain (none, light, shower), cloud cover, visibility, noise level.
- Surveys not conducted in heavy rain or high winds.

### Data consolidation
- Data input entered by multiple individuals; data were compiled, error checked, and validated before final dataset assembly.

## Data structure and content

### Dataframes
- Two dataframes:
  - Bird observations (observations per 10-minute point count).
  - Survey details (context for each 10-minute point count).

### Key variables
- pcid: Unique point count identifier (year_tile_visit_point); used to merge the two dataframes.
- Species coding: spcode (two-letter BTO code) and species (common name); distance and time banded counts (e.g., m12_ns20, m12_s20, etc.) across multiple minute blocks (1–2, 3–4, 5–6, 7–8, 9–10) and distance bands (20 m, 40 m, 60 m, 100 m, 200 m), including in-flight counts.
- Table 1 covers bird counts by time block, distance band, singing status, and flight status (e.g., ns for non-singing, s for singing, fly for in flight).
- Table 2 (survey details) includes: city, observer, tile, visit, point, month, time of day, date, start time, wind, rain, cloud, visibility, temperature, noise; counts by observer category (children, commuting, cycling, dogwalking, exercising, leisure, parent/child, shopping, working, walking, other); opportunistic counts for butterflies and several vertebrates (cat, deer, fox, rabbit, rat, squirrel).
- Supporting data: tile locations with OSGB coordinates (easting, northing) for 500 m tiles.
- Glossary (Table 4): mapping of species codes to common species names (extensive list of common UK birds).

### Data files and metadata
- Data package includes:
  - F3UES_birdpoints2013.zip containing the two dataframes (observations and survey details).
  - Missing data represented as NA.
  - Accompanying files:
    - F3UES_birdsurvey_tile_locations.csv with tile location coordinates.
    - Table 4 glossary of species codes.
- Species codes and context provided to enable interpretation and reuse.

## Data quality, governance, and limitations

- Data quality assurance:
  - Data were input by multiple people and then error-checked and validated during consolidation.
- Limitations and caveats:
  - Some survey points or tiles were inaccessible and not surveyed.
  - Opportunistic counts (butterflies, mammals) were recorded but not part of the primary aims.
  - Weather constraints meant some time windows were not sampled under certain conditions.
- Metadata and data sharing:
  - The dataset includes explicit metadata (variable descriptions, data structure, and a glossary) to aid interpretation and reuse.
  - Geographic data are provided in OSGB coordinates for reproducibility and spatial analyses.

## Practical use for monitoring framework authors

- Demonstrates a structured, tile-based, repeated-measures design across urban forms with explicit time-of-day sampling to capture detectability.
- Provides comprehensive metadata, including data dictionaries, variable definitions, and data provenance (survey organization and data consolidation process).
- Highlights data governance considerations such as data sharing (mergable dataframes via pcid), data quality checks, and openness of supporting data (tile locations and species glossary).
- Illustrates handling of incomplete data (inaccessible survey points) and integration of primary and opportunistic observations within a single dataset. 

## Contact and contact points

- Survey design and implementation contact: Gavin Siriwardena (gavin.siriwardena@bto.org) and Kate Plummer (kate.plummer@bto.org).
- Organization: British Trust for Ornithology (BTO), The Nunnery, Thetford, Norfolk, UK.