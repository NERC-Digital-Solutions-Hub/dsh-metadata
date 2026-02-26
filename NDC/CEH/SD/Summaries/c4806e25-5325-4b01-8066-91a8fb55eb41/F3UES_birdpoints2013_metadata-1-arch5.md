# F3UES_birdpoints2013.zip dataset

- Overview
  - Part of the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project within the Biodiversity and Ecosystem Service Sustainability (BESS) framework.
  - Objective: characterize variation in breeding bird fauna across urban forms (green space vs. built cover) and assess detectability at different times of day, including incidental counts of people observed during observations.
  - Geography and period: Bedford, Luton, and Milton Keynes, UK; May–August 2013.
  - Data scope includes birds, human presence, and opportunistic observations of mammals and butterflies; weather and site conditions are recorded.

- Survey organisation and design
  - Lead institutions: British Trust for Ornithology (BTO) with survey design and implementation by Gavin Siriwardena and Kate Plummer.
  - Tile-based sampling: 116 tiles defined by 500m × 500m grids, selected from three cities; tiles stratified by available green/green-seal mix.
  - Field setup: four survey points per tile, at least 200m apart and 100m from tile edges; some points later inaccessible and not surveyed.
  - Timing: six to seven visits per tile from May to August 2013; mornings (06:00–10:00) for a subset to measure morning abundances; remaining visits (10:00–18:00) for afternoon abundances.

- Data collection methods
  - Birds: 10-minute point counts per survey point; approach within 0–10m recorded; birds observed or heard within five distance bands (0–20m, 20–40m, 40–60m, 60–100m, 100–200m) and in flight; separate recording for singing vs. non-singing birds; best estimate provided when counts differ from the sum of observations.
  - Time/seasonal splits: data captured in two-minute intervals across bands; counts grouped into mins 1–2, 3–4, 5–6, 7–8, 9–10.
  - People: counts of people seen within 200m of the survey point, categorized by activity type (children, dog walking, working, etc.).
  - Opportunistic observations: mammals and butterflies recorded near survey points (not part of core aims).
  - Survey conditions: start times logged; weather (Beaufort wind, rain, cloud cover, visibility, noise) recorded; surveys not conducted in heavy rain or high winds.
  - Data handling: multiple inputters digitized field sheets; dataset consolidated, error-checked, and validated.

- Data structure and variables
  - Two linked dataframes in the F3UES_birdpoints2013.zip:
    - FU3ES_birdpoints2013_obsdata.csv: bird observations per 10-minute count; key variable pcid (unique id) and spcode/species; detailed counts across time bands, distance bands, and singing status; fields for approach and bestest estimates.
    - FU3ES_birdpoints2013_surveydata.csv: survey metadata per 10-minute observation; includes city, observer, tile, visit, month, time-of-day, date/time, weather (wind, rain, cloud, visibility, noise), and counts of people by category; opportunistic species counts (butterfly, cat, deer, fox, rabbit, rat, squirrel).
  - Key identifiers:
    - pcid: unique point count id (format year_tile_visit_point) used to merge the two dataframes.
    - Tables outline variable names and descriptions (Table 1 for bird observations, Table 2 for survey details).
  - Data types and handling:
    - Counts are numeric; missing data represented as NA.
    - Data can be merged across dataframes using pcid.

- Supporting data and resources
  - Tile locations: F3UES_birdsurvey_tile_locations.csv provides tile center coordinates in OSGB 1936 (easting/northing) and associated city.
  - Glossary: Table 4 lists species by two-letter codes and full common names (e.g., BT Blue Tit, GK Kestrel), including a code for feral/hybrid mallard or goose (ZF ZL).

- Data quality, limitations, and provenance
  - Data quality measures: field data were input by multiple personnel, then subjected to error checking and validation before final consolidation.
  - Limitations:
    - Some survey points were inaccessible, so not all tiles/points are represented.
    - Opportunistic observations (mammals/butterflies) are not part of the core aims.
  - Provenance:
    - Data originate from a clearly defined, published survey design within the F3UES project, with explicit methodologies, timing, and data consolidation steps documented.

- Usage, access, and governance notes for Data Stewards
  - File organization and access:
    - Core dataset files: FU3ES_birdpoints2013_obsdata.csv and FU3ES_birdpoints2013_surveydata.csv (linked via pcid).
    - Supporting files: F3UES_birdsurvey_tile_locations.csv and a species glossary (Table 4) for interpretation of codes.
  - Metadata and standards:
    - Detailed variable descriptions are provided (Tables 1–4).
    - pcid enables robust data merging across bird observations and survey metadata.
  - Reuse considerations:
    - Data can support analyses of species abundance by time of day, distance bands, and urban form; can be linked with tile locations for spatial analyses.
    - Ensure proper citation of the F3UES/BESS project and grant when used.
  - Data stewardship implications:
    - Maintain and update metadata for any reuses or downstream analyses.
    - Preserve the linkages between the two dataframes via pcid and maintain provenance from field collection to validation.