# Kinder Scout gully block survey 2021

## Overview
- Project: Protect-NFM; NERC grant NE/R004560/1; Author: Adam Johnston.
- Purpose: assess long-term (7–8 years) evolution of gully blocks installed during peatland restoration on Kinder Scout, UK.
- Dataset includes 492 gully blocks with location, dimensions, and ecological characteristics; dam-related data collected in 2013–2014 and re-surveyed in 2021; vegetation data provided in a separate file linked by dam_id.

## Experimental design and sampling
- From 2013–2014, >3000 gully blocks were installed; 500 blocks were randomly selected for survey.
- Due to time constraints with dGPS, location data collected separately from other measurements.
- Marker placed at each dam to enable relocation for follow-up survey; eight dams could not be relocated for the field survey.

## Data collection and processing methods
- Location: surveyed with Leica VIVA GS10 GNSS (rover and base). Post-processed in Leica Infinity using Ordnance Survey RINEX data from Buxton as fixed reference.
- Quality: fixed control points repeat-surveyed daily; 3D accuracy assessed with 3D error of ±0.03 m.
- Dam measurements: dimensions (width, height, sediment depth, dam-top to sediment height) measured in field with tape and level; some data may be missing (denoted nd) if not recorded or if dam not relocated.
- Derived attributes: some features derived geospatially from 0.25 m DSMs (terrain attributes: aspect, gully wall slope, channel slope, gully width/depth) from Bluesky International data (2020); bare peat upslope area estimated from 0.05 m RGB imagery (2011) by GetMapping.
- Vegetation: three positions per dam (gully floor, gully walls, dam top) surveyed for overall vegetation cover and presence/absence of key indicator species; field notes also captured.
- Data entry: missing data indicated as nd.

## Fieldwork equipment
- Leica Viva GS10 Base and Rover GNSS; measuring tapes, 1 m rule, and a level for dam dimensions.

## Data structure and content
- Main dataset: dam location and physical characteristics (rows = dams; columns = attributes).
- Ancillary vegetation dataset: paired on dam_id and field_survey_date with vegetation cover percentages and binary species indicators; includes a notes field.
- Data provided as two CSV files; columns and units are described in the accompanying metadata (e.g., GNSS_dateTime_GMT, easting/northing/elevation in British National Grid, various slope/width/depth attributes, storage and pool metrics, etc.).

## Quality control and uncertainty
- 3D positional accuracy validated via daily repeat surveys; reported 3D error ±0.03 m.
- Occasional data gaps due to inability to relocate certain dams or data loss; missing values marked as nd.
- Fixed control points re-surveyed each day to ensure spatial quality.

## Usage, limitations, and potential applications
- Enables long-term analysis of dam block evolution, hydrology (pooling, storage), and sediment/peat dynamics in relation to terrain attributes.
- Allows linking vegetation dynamics around dams to structural characteristics and upstream bare peat conditions.
- Suitable for cross-dataset analyses by pairing main **dam** data with the ancillary vegetation dataset via dam_id.
- Users should account for missing data (nd) and the time gap between dGPS collection (Sept–Oct 2021) and field measures for some attributes; some attributes are geospatially derived rather than directly measured.