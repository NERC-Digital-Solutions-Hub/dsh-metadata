# F3UES_birdpoints2014.zip dataset

## Overview
- Part of the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project within the Biodiversity and Ecosystem Service Sustainability (BESS) framework.
- Aims to characterize variation in breeding bird fauna across urban forms (green space vs built/sealed cover) in the Luton, Bedford, and Milton Keynes area.
- Also records the number of people observed during each observation period.

## Survey organization
- Design and implementation led by Gavin Siriwardena and Kate Plummer of the British Trust for Ornithology (BTO).
- Contact details provided for the two organizers.

## Study area and timing
- Data collection: May 1 to June 30, 2014.
- Area: Bedford (BF), Luton (LT), Milton Keynes (MK).
- Sampling frame: each town defined by a 500m × 500m grid; 116 tiles were randomly selected using stratified sampling.
- Within each tile: four survey points located ≥200m apart and ≥100m from tile edges; some points inaccessible and excluded from the dataset.

## Survey methods
- Bird surveys:
  - Point counts conducted at pre-defined survey points.
  - Two visits per tile between 06:00 and 10:00 in May and June.
  - Ten-minute counts per point, in random order across tiles.
  - All birds within 10m observed; after a disturbance period, a 10-minute observation followed.
  - Counts recorded over distance bands (0–20m, 20–40m, 40–60m, 60–100m, 100–200m) and in flight; singing vs non-singing categorized.
  - A "best estimate" field used if totals differed from the sum of counts.
- People observation:
  - Number of people within 200m of each survey point during each 10-minute observation, categorized by activity (e.g., children, dog walking, working, etc.).
- Survey conditions:
  - Start time recorded; weather data collected (Beaufort wind, rain, cloud cover, visibility, noise).
  - Surveys not conducted in heavy rain or high winds.
- Data handling:
  - Multiple data inputters digitized field sheets; dataset compiled, error-checked, and validated.

## Data description
- FU3ES_birdpoints2014_obsdata.csv:
  - obs data per 10-minute observation, linked by pcid.
  - Key fields: pcid, spcode (species code), species, approach, bestest, and counts across multiple distance bands and singing/non-singing statuses (e.g., m12_ns20, m12_s20, m34_ns40, etc., across 20m–200m bands and fly/travel categories).
- FU3ES_birdpoints2014_surveydata.csv:
  - survey details per 10-minute observation.
  - Key fields: pcid, city, observer, tile, visit, point, month, tod, date, time, wind, rain, cloud, vis, temp, noise, and counts for various people activities (children, commuting, cycling, dogwalking, exercise, leisure, etc.).
- Missing data: represented as NA.
- pcid serves as the unique identifier to merge the two dataframes.

## Supporting data and glossary
- Supporting tile locations: F3UES_birdsurvey_tile_locations.csv with tile id, city, easting, northing (OSGB 1936 coordinates).
- Table of bird species (Table 4) providing a glossary of species codes and common names (extensive list covers common UK urban birds).

## Data structure and interoperability
- The dataset comprises two linked dataframes (observations and survey details) that can be joined via pcid.
- Clear variable naming and documentation support standardised data analysis and cross-site comparisons.
- Data quality steps include error checking and validation during consolidation.

## Relevance for environmental monitoring
- Enables standardized monitoring of breeding bird abundance across different urban forms, useful for policy evaluation and urban planning.
- Facilitates integration with ancillary data (e.g., human activity, weather) to interpret habitat and disturbance effects on birds.
- Designed for compatibility with portal-based data sharing and long-term analysis.

## Limitations and notes
- Some potential survey points were inaccessible and not included.
- Data reflect a specific seasonal window (May–June 2014); cross-seasonal comparisons require additional data.

## Contact
- Project leads: Gavin Siriwardena and Kate Plummer (BTO).