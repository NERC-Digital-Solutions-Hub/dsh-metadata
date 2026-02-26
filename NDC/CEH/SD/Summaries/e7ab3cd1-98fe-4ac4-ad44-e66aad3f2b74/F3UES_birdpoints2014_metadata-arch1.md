# About the survey

- The data come from the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project, focusing on variation in breeding bird fauna across urban forms in the Luton, Bedford, and Milton Keynes area, and recording numbers of people observed during surveys.
- Purpose: characterise relationships between urban greenspace, built cover, and breeding birds; enable analysis of correlations and potential predictors of bird abundance and diversity.

## Survey organization

- Lead investigators: Gavin Siriwardena and Kate Plummer from the British Trust for Ornithology (BTO).
- Contact details: gavin.siriwardena@bto.org; kate.plummer@bto.org; BTO address and phone provided.

## Survey design and study area

- Timeframe: surveys conducted May to June 2014.
- Study units: 500m × 500m tiles, with 116 tiles randomly selected across Bedford, Luton, and Milton Keynes.
- Within each tile: four survey points (≥200m apart, ≥100m from tile edges); some points inaccessible and not surveyed.
- Data collected: breeding birds and counts of people observed within 200m of each survey point.

## Field methods

- Bird surveys: point counts at each survey point, two visits per tile between 06:00 and 10:00.
  - 10-minute counts; record all birds seen or heard within 10m (potentially disturbed) and in five distance bands (0-20m, 20-40m, 40-60m, 60-100m, 100-200m) plus in-flight observations.
  - Birds singing and those only calling or seen (not singing) recorded separately.
  - For totals that diverged from the sum of counts, a 'best estimate' (bestest) is recorded.
  - Data include counts by 2-minute intervals (mins 1-2, 3-4, 5-6, 7-8, 9-10) for each distance band and for birds in flight, split into singing and non-singing where applicable.
- People surveys: counts of people observed within 200m of each survey point, categorized by activity type (e.g., children, dog walking, working, shopping, etc.).
- Environmental conditions: start time of each 10-minute count; weather data (Beaufort wind, rain, cloud cover, visibility, noise) recorded; surveys not conducted in heavy rain or high winds.

## Data processing and structure

- Data consolidation: multiple data inputters collected field sheets, then data were compiled, error-checked, and validated.
- Data files:
  - FU3ES_birdpoints2014_obsdata.csv: bird observation data for each 10-minute point count (unique pcid).
  - FU3ES_birdpoints2014_surveydata.csv: survey details for each 10-minute point count (pcid links to obsdata).
- pcid: unique point count identifier (formatted year_tile_visit_point) to merge the two dataframes.
- Missing data: represented as NA.
- Supporting data: tile centers provided in F3UES_birdsurvey_tile_locations.csv with OSGB coordinates (easting, northing).
- Glossary: Table 4 lists species codes and full species names (extensive mapping of codes to common names).

## Variables and data interpretation

- Bird observations dataframe includes:
  - spcode (two-letter species code) and species (common name).
  - Counts by time blocks (mins 1-2, 3-4, etc.) across distance bands (ns: non-singing; s: singing) and in-flight categories.
  - Best estimate (bestest) when totals differ from summed counts.
  - Additional fields capture counting detail (approach, point) and spatial-temporal granularity.
- Survey details dataframe includes:
  - City, observer, tile, visit, point, month, time of day (tod), date, start time, and a suite of environmental and human-activity variables (wind, rain, cloud, visibility, temperature, noise; counts by activity types such as children, dogwalking, working, etc.).

## Supporting data and resources

- Tile locations: F3UES_birdsurvey_tile_locations.csv provides tile centre coordinates (OSGB 1936) for spatial analysis.
- Species glossary: Table 4 maps codes to full Latin names for all species encountered.

## Considerations for analysis

- Intended for examining how breeding bird assemblages vary with urban form (greenspace vs sealed cover) and across the three towns.
- Covariates available for modeling: time of day, month, weather (wind, rain, cloud, visibility, noise), and human activity levels within 200m.
- Spatial analysis opportunities using tile coordinates to relate bird counts to urban form and geographic location.
- Data limitations:
  - Some tiles/points were inaccessible, reducing spatial coverage.
  - Data limited to May–June 2014; seasonal and inter-annual variability not captured.
  - Data collected by multiple inputters; validation steps documented, but users should consider potential minor inconsistencies.

## Access and reuse notes

- Data are organized into two linked dataframes (obsdata and surveydata) via pcid, enabling integrated analyses of bird counts with survey context and environmental variables.
- Comprehensive metadata and a species glossary support reproducible analysis and interpretation.