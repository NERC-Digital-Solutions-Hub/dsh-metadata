# Kinder Scout gully block survey 2021

## Overview
- Dataset describes location, dimensions, and ecological characteristics of 492 gully blocks on Kinder Scout, an upland peatland in the UK.
- Context: stone and timber dams installed in 2013–2014 as peatland restoration; survey aims to understand longer-term evolution 7–8 years post-installation.
- Data structure: main dam survey dataset plus an ancillary vegetation dataset; both linked by dam_id. Two CSV files; dams are rows with multiple attribute columns.

## Experimental design/sampling regime
- More than 3,000 gully blocks installed in 2013–2014; 500 blocks randomly selected for survey.
- Time constraints with dGPS led to staggered data collection; a relocation marker was used to find dams for follow-up measurements.
- Some dams (eight) could not be relocated for the second survey.

## Collection, generation, or transformation methods
- Dam location: surveyed with Leica VIVA GS10 GNSS (rover and base); post-processed in Leica Infinity using OS RINEX data from Buxton as fixed reference; daily fixed control points used to assess 3D quality.
- Accuracy: 3D positional error ±0.03 m from repeat surveys.
- Dam measurements: dimensions (width, height, sediment depth, etc.) measured in field with tape rule and level; some fields marked as nd (no data) when data were lost or a dam couldn’t be relocated.
- Geospatial derivations: terrain attributes (aspect, gully slopes) derived from 0.25 m DSM photogrammetry by Bluesky International; pre-install bare peat area estimated from 0.05 m RGB imagery (2011) by GetMapping.
- Vegetation: three positions per dam (gully floor, gully walls, dam top) with percent cover estimates and binary presence/absence of key indicator species; a separate vegetation file accommodates these data and can be matched to the main dataset via dam_id.

## Equipment
- Leica Viva GS10 Base and Rover GNSS.
- Measuring tapes, 1 m ruler, and level for dam dimensions.

## Calibration steps and values
- Not applicable (N/A).

## Nature and units of recorded values
- Core columns include: GNSS_dateTime_(GMT); dam_id; easting/northing/elevation (UK grid coordinates and elevation); aspect, gully_wall_slope, channel_slope (degrees); gully_width, gully_depth (m); upslope_area (m^2); area_of_bare_peat_upslope (m^2); percent_bare_peat_upslope (%); field_survey_date; dam_type (Stone/Timber); dam_width/dam_height (m); dam_top_to_sediment (m); sediment_depth (m); storage metrics (percent, volume, etc.); pool metrics (presence, depth); channel flow into pool; notes. All units include metres, degrees, metres cubed, percentages, and binary indicators where appropriate. nd denotes missing data.

## Quality control
- 3D positional accuracy verified via repeated fixed control points; reported 3D error ±0.03 m.

## Details of data structure
- Two CSV files: main dam survey dataset (positional data and physical characteristics) and ancillary vegetation dataset.
- Dams are in rows; attributes are columns.
- Pairing between datasets achieved through dam_id; vegetation and field survey dates align via field_survey_date.

## Miscellaneous
- Project context: Protect-NFM, NERC grant NE/R004560/1 (Optimising NFM in headwater catchments to protect downstream communities); Author: Adam Johnston.