# Kinder Scout gully block survey 2021

## Overview
- Dataset documents the location, size/dimensions, and ecological characteristics of 492 gully blocks on Kinder Scout, an upland UK peatland.
- Dams (stone and timber) installed in 2013–2014 as part of peatland restoration; survey assesses long-term evolution over ~7–8 years.
- Data collected include dam positions via differential GPS, field measurements of dam dimensions and vegetation; some geospatial-derived attributes included.
- An ancillary vegetation dataset is provided separately and can be linked to the main dataset by dam ID.

## Experimental design and sampling
- >3000 gully blocks installed in 2013–2014; 500 blocks randomly selected for survey.
- Time constraints with dGPS meant differing times for positional vs. dimensional measurements; a relocation marker was used to find dams for follow-up surveys.
- Field activities limited by conditions; eight dams could not be relocated for the second survey.
- dGPS survey conducted 22/09/2021–06/10/2021; field survey conducted 13/09/2021–13/10/2021.

## Collection, generation, and transformation methods
- Dam positions collected with Leica VIVA GS10 GNSS (rover and base); post-processed with Leica Infinity using OS RINEX data from Buxton as the fixed reference.
- Fixed control points were repeatedly surveyed to assess 3D accuracy; 3D positional error estimated at ±0.03 m.
- Dam dimensions (depths/heights) measured in the field with a meter rule and level; some rows missing data where a dam could not be relocated ('nd' entries).
- Some dam attributes derived geospatially; terrain attributes derived from a 0.25 m DSM (Bluesky International) and up-slope bare peat estimates from 0.05 m RGB imagery (GetMapping, 2011).
- Local vegetation surveyed around each dam at three positions: gully floor, gully walls, and dam top; for each position, overall vegetation cover percentage and presence/absence (binary) of key indicator species were recorded.

## Fieldwork equipment
- Leica Viva GS10 Base and Rover GNSS
- Tape measure, 1 m ruler, and a level for dam measurements

## Calibration steps and values
- Not applicable (N/A)

## Nature and units of recorded values
- Main dataset columns include: GNSS_dateTime_GMT, dam_id, easting, northing, elevation_m, aspect_deg, gully_wall_slope_deg, channel_slope_deg, gully_width_m, gully_depth_m, upslope_contributing_area_m2, area_of_bare_peat_upslope_m2, percent_bare_peat_upslope_percent, field_survey_date, dam_type (Stone/Timber), dam_width_m, dam_height_m, dam_top_to_sediment_m, sediment_depth_m, storage_height_availability_percent, storage_height_sediment_infilled_percent, pool_behind_dam_binary, pool_depth_m, channel_flow_into_dam_pool_binary, static_storage_volume_m3, percent_storage_volume_full_percent, notes.
- Geological/geospatial attributes derived from DSMs and aerial imagery; vegetation attributes provided in a separate file with dam_id linkage.
- Vegetation dataset columns include matching dam_id and field_survey_date, with per-position (Flr, Wall, Dam_top) vegetation_cover_percent and presence/absence flags for key species; an 'other' field for notes per position.
- Data entry 'nd' indicates no data.

## Data structure and accessibility
- Data provided as two CSV files:
  - Main dam survey dataset (positional and physical dam attributes)
  - Ancillary vegetation dataset (paired via dam_id and field_survey_date)
- Dams are represented as rows; columns are the recorded attributes.
- Datasets can be joined by dam_id; detailed column descriptions are provided within the dataset documentation.

## Quality control and considerations
- 3D positional accuracy validated via repeated fixed control points; reported 3D error ±0.03 m.
- Some missing measurements due to field challenges (e.g., inability to relocate certain dams).
- Data include both measured (field) and derived (geospatial) attributes; some attributes rely on imagery from 2011–2020 datasets.
- Clear indication of data gaps with 'nd' entries to enable robust data interpretation and gap analysis.

## Relevance for monitoring frameworks
- Demonstrates long-term monitoring design for peatland restoration infrastructure (dams) with integration of field surveys and geospatial-derived metrics.
- Highlights practical data governance considerations for monitoring datasets: linking main and ancillary datasets, explicit metadata (column descriptions and units), handling of missing data, and openness of data sharing.
- Provides a structured example of how to document dataset provenance, measurement methods, and quality checks to support transparency and future reuse.