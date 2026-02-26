# F3UES_birdpoints2014.zip

## Overview
- Dataset from the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project, within the Biodiversity and Ecosystem Service Sustainability (BESS) framework.
- Aims to characterize variation in breeding bird fauna across urban forms in the Luton, Bedford, and Milton Keynes area, relative to green vs built cover, and to record the number of people observed during surveys.

## Survey Organization
- Lead researchers: Gavin Siriwardena and Kate Plummer from the British Trust for Ornithology (BTO).
- Contact points provided for project correspondence.

## Survey Methods
- Timeframe and area:
  - Conducted May–June 2014 in Bedford, Luton, and Milton Keynes.
  - Study area defined by a 500m × 500m grid; 116 tiles randomly selected from this grid for surveying.
- Tile and survey point setup:
  - Within each tile, four survey points ( ≥200m apart, ≥100m from tile edges) selected to represent available greenspace; some points inaccessible and omitted from the dataset.
- Bird surveying:
  - Point counts conducted over two visits per tile between 06:00 and 10:00.
  - Each visit: ten-minute counts at all survey points in random order; record birds within 10m (and immediately disturbed birds), then extend observations across distance bands (0–20m, 20–40m, 40–60m, 60–100m, 100–200m) and in flight.
  - Birds recorded if singing or otherwise calling/visible; a best-estimate is provided if totals differ from the sum of recorded birds.
- People surveying:
  - Count of people within 200m of the survey point for each 10-minute observation, categorized by activity type (e.g., children, dog walking, working, etc.).
- Survey conditions:
  - Start time logged; weather data recorded at end of observation (Beaufort wind, rain, cloud cover, visibility, noise).
  - Surveys not conducted in heavy rain or high winds.
- Data consolidation:
  - Field data entered by multiple inputters; dataset compiled, error-checked, and validated.

## Data Description
- File: F3UES_birdpoints2014.zip containing two dataframes.
  - Dataframe 1: Bird observations for each 10-minute point count.
  - Dataframe 2: Other survey details for each 10-minute point count.
- Identifier:
  - Unique point count ID (pcid) used to merge the two dataframes.
- Key variables (Dataframe 1):
  - pcid, spcode (2-letter species code), species (common name), approach (count when approaching), bestest (best estimate if totals differ), and detailed counts by time segments (mins 1–2, 3–4, 5–6, 7–8, 9–10) across distance bands (20m, 40m, 60m, 100m, 200m) for singing and non-singing birds, plus in-flight counts.
- Key variables (Dataframe 2):
  - pcid, city (BF, LT, MK), observer, tile, visit, point, month, tod (time of day), date, time, wind, rain, cloud, vis (visibility), temp, noise, and counts of people by category (children, commuting, cycling, dogwalking, exercising, leisure, parent/child, shopping, working, walking, other).
- Data qualifiers:
  - Missing data indicated as NA.

## Supporting Data
- Tile locations:
  - File: F3UES_birdsurvey_tile_locations.csv with tile ID, city, and center coordinates in OSGB 1936 (easting, northing).
- Glossary:
  - Table of bird species codes and full common names (e.g., B. Blackbird, BT Blue Tit, etc.), including a comprehensive list of 2-letter codes.

## Data Quality and Notes
- Data include a mix of field-collected counts and derived estimates; there is a detailed structure to support merging and analysis across observations and survey details.
- Some tiles or survey points were inaccessible, which is noted as a caveat for data completeness and spatial coverage.
- Data are organized with explicit metadata and standardized coding to facilitate analysis and sharing across the urban ecology data community.