# Kinder Scout gully block survey 2021

## Overview
- Dataset of location, dimensions, and ecological characteristics for 492 gully blocks on Kinder Scout, an upland peatland in the UK.
- Origin: peatland restoration works in 2013–2014 (stone and timber dams).
- Purpose: assess longer-term (7–8 years) evolution of gully blocks.
- Data include dam point location (dGPS), field measurements of dam dimensions and vegetation, with some attributes derived geospatially.
- Ancillary vegetation data available in a separate file to be matched by dam identification number.

## Experimental design and sampling
- >3,000 gully blocks installed in 2013–2014; 500 randomly selected for survey across the plateau.
- Eight dams could not be relocated for the field survey.
- dGPS survey conducted between 22/09/2021 and 06/10/2021.
- Field measurements conducted between 13/09/2021 and 13/10/2021.

## Data collection, transformation and attributes
- Dam locations measured with Leica VIVA GS10 GNSS (rover and base); post-processed with Leica Infinity using Ordnance Survey RINEX data (Buxton station) as fixed reference.
- 3D quality checked via repeat control points; achieved 3D accuracy of ±0.03 m.
- Dam dimensions (depths, heights) measured in field with a meter rule and level; some records missing data (marked as nd).
- Some dam attributes derived from geospatial data:
  - Terrain attributes from 0.25 m DSM (Bluesky International) and 0.25 m gully-related measures.
  - Bare peat area upslope prior to dam installation estimated from 0.05 m RGB imagery (2011, GetMapping).
- Vegetation around each dam recorded at three positions (gully floor, gully walls, dam top) with overall vegetation cover and presence/absence of key indicator species.
- Data entry notes, measurements, and derived attributes are described in the accompanying data dictionaries within the dataset.

## Data structure and accessibility
- Two CSV files:
  - Main dataset: dam-specific attributes and GNSS/location data (one row per dam).
  - Ancillary vegetation dataset: matching dam_id and field_survey_date, with vegetation metrics.
- Datasets can be paired via dam_id (shared key) and field_survey_date.
- Columns include GNSS date/time, easting/northing/elevation (British National Grid), aspect, gully slopes, channel slope, gully dimensions, upslope bare peat metrics, dam type (Stone/Timber), dam dimensions, sediment behind dam, storage metrics, pool presence/depth, channel inflow, and notes.
- ND entries indicate missing data for specific measurements.

## Key variables and measurements
- Spatial: GNSS_dateTime_GMT, easting, northing, elevation (m), aspect (deg), gully_wall_slope (deg), channel_slope (deg), gully_width (m), gully_depth (m), upslope_contributing_area (m^2).
- Bare peat metrics: area_of_bare_peat_upslope (m^2), percent_bare_peat_upslope (%).
- Field timing: field_survey_date.
- Dam characteristics: dam_type (Stone/Timber), dam_width (m), dam_height (m), dam_top_to_sediment (m), sediment_depth (m), storage_height_availability (%), storage_height_sediment_infilled (%).
- Hydrology indicators: pool_behind_dam (binary), pool_depth (m), channel_flow_into_dam_pool (binary), static_storage_volume (m^3), percent_storage_volume_full (%), notes.
- Vegetation: datasets include percent cover per position (gully floor, walls, dam top) and binary presence/absence of indicator species; additional notes per position.

## Vegetation ancillary dataset
- Linked by dam_id and field_survey_date.
- Provides per-position vegetation cover and species presence/absence with an extra notes field for other species.

## Quality control and uncertainty
- 3D accuracy checked using repeated fixed control points; reported 3D error of ±0.03 m.
- Some records lack data due to field relocation issues or data loss (marked as nd).
- Derived geospatial attributes based on high-resolution DSM/RGB imagery to support standardized monitoring.

## Relevance to environmental monitoring and policy
- Provides a standardized, long-term dataset to monitor peatland restoration outcomes and hydrological behaviour of gully blocks.
- Supports cross-year comparisons and assessment of storage capacity and sediment infill behind dams.
- Data are structured for integration into environmental monitoring portals and can be reused alongside other datasets to increase the value of monitoring efforts (aligns with aims to enable broader data access and combination with related data sources).