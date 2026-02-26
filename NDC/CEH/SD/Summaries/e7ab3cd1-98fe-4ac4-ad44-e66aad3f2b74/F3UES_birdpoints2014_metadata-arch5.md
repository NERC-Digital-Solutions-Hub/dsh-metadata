# F3UES_birdpoints2014 dataset description

- Part of the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project, funded under NE/J015067/1 within the Biodiversity and Ecosystem Service Sustainability (BESS) framework.
- Aims to characterise variation in breeding bird fauna across urban forms in the Luton, Bedford, and Milton Keynes area, defined by green space versus sealed built cover; simultaneously recorded the numbers of people observed during each observation period.
- Survey designed and implemented by Gavin Siriwardena and Kate Plummer (British Trust for Ornithology, BTO); contact details provided.

## Survey design and scope

- Timeframe and area: Began May and ended June 2014; sites in Bedford (BF), Luton (LT), and Milton Keynes (MK).
- Spatial sampling: Each town defined by 500m × 500m grid; 116 tiles randomly selected for surveying via stratified design.
- Within-tile sampling: Four survey points per tile, ≥200m apart and ≥100m from tile edges; some points inaccessible and excluded from the dataset.
- Data collected: Bird observations and people observed during each 10-minute point count; weather and survey conditions also recorded.

## Data collection methods

- Bird surveys: Point counts conducted at pre-defined survey points; two visits per tile (May and June) between 06:00 and 10:00; 10-minute observation periods with birds observed within 10m (including potentially disturbing birds).
  - Distances and timing: Birds counted in two-minute intervals across distance bands (0-20m, 20-40m, 40-60m, 60-100m, 100-200m) and in flight; singing and non-singing birds recorded separately.
  - Data detail: Best estimate (bestest) recorded when totals differ from the sum of counts.
- People surveys: Counts of people within 200m of the survey point during each 10-minute observation, categorized by activity type (e.g., children, dog walking, working, shopping, etc.).
- Survey conditions: Start time; weather (Beaufort wind, rain: none/light/shower, cloud cover %, visibility, noise level); temperature; surveys not conducted in heavy rain or high winds.
- Data consolidation: Multiple inputters collected field data; datasets were compiled, error-checked, and validated.

## Data structure and fields

- File and structure: The F3UES_birdpoints2014.zip dataset comprises two dataframes.
  - Bird observations dataframe: pcid (unique 10-minute point count ID), spcode (BTO 2-letter code), species name, and detailed counts by time blocks, distance bands, and singing status (e.g., m12_ns20, m12_s20, …, m910_nsfly, m910_sfly).
  - Point count survey details dataframe: pcid, city, observer, tile, visit, point, month, tod (time of day), date, time, wind, rain, cloud, vis, temp, noise, and counts for each people category (children, commuting, cycling, dogwalking, exercise, leisure, parentchild, shopping, working, walking, other).
- Linkage: A unique pcid connects observations to survey details, enabling dataset merging.
- Supporting data: Tile center coordinates (OSGB 1936) provided in F3UES_birdsurvey_tile_locations.csv; includes tile id, city, easting, northing.
- Glossary: Table 4 provides a complete mapping of bird species codes to common names (extensive list of codes such as B., BC, BF, etc.).

## Supporting data and metadata

- Tile locations: Center coordinates for each 500m × 500m tile (OSGB 1936/British National Grid) in the accompanying file.
- Species glossary: Full mapping of all species codes used in the dataset to their common names.
- Data availability note: Some tiles had inaccessible points and are not present in the dataset; missing data are indicated as NA within the dataframes.

## Data governance, quality and provenance

- Governance: Clear attribution to survey designers (BTO) and project context (F3UES/BESS).
- Provenance and quality: Field data collected by multiple observers, then compiled, error-checked, and validated to form the final two dataframes.
- Metadata and standards: Use of standardized BTO species codes; detailed variable descriptions; unique identifier (pcid) for data integrity and cross-table merges.
- Updates and reuse: Data are organized for reuse in ecological analyses; accompanying metadata files (tile locations and glossary) facilitate context and reproducibility.

## Limitations and cautions

- Incomplete sampling: Some survey points were inaccessible, resulting in their exclusion from the dataset.
- Temporal constraints: Data reflect May–June 2014 conditions; urban form and bird communities may have changed since.
- Detection and measurement: Bird counts depend on detectability influenced by time of day, weather, and anthropogenic noise; bestest estimates are provided to address count discrepancies.

## Access, usage and contact

- Data format: Two primary dataframes within the F3UES_birdpoints2014.zip, plus accompanying tile location file and species glossary.
- Reuse guidance: Use pcid to join observations with survey details; consult the tile location file for spatial context; refer to Table 1 and Table 2 variable descriptions for understanding fields.
- Contact: For survey design and implementation details, reach Gav in Siriwardena and Kate Plummer at the British Trust for Ornithology (BTO).