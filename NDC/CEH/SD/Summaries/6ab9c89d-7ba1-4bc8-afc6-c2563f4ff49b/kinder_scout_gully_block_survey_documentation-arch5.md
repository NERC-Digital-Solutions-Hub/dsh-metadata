# Kinder Scout gully block survey 2021

## Overview
- Dataset on location, dimensions, and ecological characteristics of 492 gully blocks on Kinder Scout peatland, UK.
- Origin: peatland restoration with stone and timber dams installed in 2013–2014; survey to assess 7–8 year evolution.
- Two linked data files: main dam survey data and ancillary vegetation data; records can be paired via dam_id.

## Purpose and scope
- Supports understanding long-term evolution of gully blocks and informs peatland restoration and water management (Protect-NFM project; NERC NE/R004560/1).
- Captures geospatial position, physical dam dimensions, and vegetation context around each dam, with some attributes derived from geospatial analysis.

## Sampling design
- From >3,000 installed blocks, 500 were randomly selected for survey.
- Positional data collected separately and later relocated to other measurements; 8 dams could not be relocated.
- Data collection windows: dGPS survey 22 Sept–6 Oct 2021; field measurements 13 Sept–13 Oct 2021.

## Data collection and methods
- Location data: Leica VIVA GS10 GNSS (rover/base); post-processed with Leica Infinity using OS RINEX Buxton as fixed reference; daily fixed control points used to assess 3D accuracy (±0.03 m).
- Dam dimensions: measured in the field with tape/level; some records missing and marked as nd.
- Geospatial derivatives: terrain attributes (aspect, slopes, gully dimensions) from 0.25 m DSM by Bluesky International (2020); bare peat upslope area estimated from 0.05 m RGB imagery (2011) by GetMapping.
- Vegetation context: three positions per dam (gully floor, gully walls, top of dam) with percent cover estimates and binary presence/absence of indicator species; ancillary dataset links via dam_id and field_survey_date; additional notes field included.

## Data structure and content
- Two CSV files:
  - Main dataset: dam_id, GNSS_dateTime, easting, northing, elevation, aspect, gully_wall_slope, channel_slope, gully_width, gully_depth, upslope_area, bare_peat_upslope_percent, field_survey_date, dam_type, dam_width, dam_height, dam_top_to_sediment, sediment_depth, storage_height_availability, storage_height_emptied, pool_behind_dam, pool_depth, channel_flow_into_dam_pool, static_storage_volume, percent_storage_volume_full, notes, plus derived/qualifier fields.
  - Ancillary vegetation dataset: dam_id, field_survey_date, notes, and vegetation columns for each position (Flr, Wall, Dam_top) including percent cover and binary species indicators (and other).
- Key units and definitions are described in the dataset metadata; missing data denoted by 'nd'.
- Data are organized with dams as rows and attributes as columns; datasets can be joined by dam_id.

## Data quality and limitations
- Positional accuracy validated with repeat surveys; 3D error around ±0.03 m.
- Missing data due to data loss or relocation failures; eight dams could not be relocated.
- Some fields derived from ancillary geospatial data; provenance tied to specific imagery/date ranges.

## Governance, access, and reuse
- Data provided as two CSV files intended for reuse and cross-project integration.
- Clear provenance: field methods, equipment, and timeframes documented; geospatial derivations and imagery sources specified.
- Suitable for longitudinal analyses of peatland restoration outcomes and dissemination through data portals; care needed to handle missing values and potential non-interoperability of older datasets.

## Project and contact
- Project: Protect-NFM; NERC grant NE/R004560/1.
- Author: Adam Johnston.