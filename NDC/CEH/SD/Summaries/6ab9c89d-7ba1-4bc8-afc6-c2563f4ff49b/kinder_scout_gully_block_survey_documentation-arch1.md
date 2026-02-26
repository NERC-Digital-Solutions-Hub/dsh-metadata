# Kinder Scout gully block survey 2021

## Overview
- Project: Protect-NFM (Optimising NFM in headwater catchments to protect downstream communities)
- Dataset: Location, dimensions, and ecological characteristics of 492 gully blocks on Kinder Scout, upland peatland, UK
- Timeline: Dam installation (2013–2014); long-term survey conducted Sep–Oct 2021 (7–8 years post-installation)
- Purpose: Assess longer-term evolution of gully blocks and associated ecological/geomorphological features
- Data products: Main dam survey dataset and ancillary vegetation dataset (matched by dam_id)

## Experimental design and sampling
- Installation scale: >3,000 gully blocks installed in 2013–2014; 500 blocks randomly selected for survey
- Survey challenges: dGPS timing and field relocation constraints; eight dams could not be relocated for field survey
- Survey windows: dGPS survey (22 Sep–6 Oct 2021); field measurements (13 Sep–13 Oct 2021)

## Data collection and generation methods
- Location data: Dam positions collected with Leica VIVA GS10 GNSS (rover and base); post-processed with Leica Infinity using OS RINEX (Buxton fixed reference)
- Positional accuracy: 3D error ± 0.03 m from repeat surveys
- Dam measurements: In-field measurements of dam dimensions (width, height, depth behind dam, sediment depth) using tape measure, ruler, and level
- Geospatial attributes: Derived attributes from 0.25 m DSM (terrain aspect, gully wall slope, channel slope, gully width/depth) using Bluesky International photogrammetry
- Bare peat and vegetation context: Bare peat upslope area estimated from 0.05 m RGB imagery (2011 GetMapping); local vegetation surveyed at gully floor, walls, and dam top
- Data notes: Some fields marked as nd (no data) when data were not collected or dam relocation failed

## Data structure and contents
- Main dataset: Dam-centered attributes per row (dam_id as unique key; GNSS date/time; easting/northing (British National Grid); elevation; dam_type; dam dimensions; storage metrics; vegetation indicators; notes)
- Ancillary vegetation dataset: Paired with main dataset via dam_id and field_survey_date; includes vegetation cover percentages and presence/absence of indicator species per position (gully floor, gully walls, dam top)
- Key derived fields: 
  - Terrain and geomorphology: aspect, gully_wall_slope, channel_slope, gully_width, gully_depth
  - Hydrology/storage: upslope bare peat area/percent, storage-related metrics (storage_height_availability, sediment_infilled, pool presence/depth, channel inflow)
  - Vegetation: percent cover (bare peat, sedge/grasses, moss/Sphagnum) and binary presence indicators
- Data availability: Provided as two CSV files (main dataset and ancillary vegetation dataset)

## Quality control and limitations
- dGPS accuracy: 3D error ± 0.03 m with daily repeat surveys and fixed control points
- Data gaps: Some dam dimension data missing (nd) due to data loss or unsuccessful relocation
- Temporal scope: 7–8 years since installation; field survey constraints may affect completeness of measurements
- Derived data: Some attributes derived from photogrammetry (DSM) and previous imagery (2011 bare peat) may introduce uncertainties tied to historical data resolution

## Analytical value and potential uses
- Enables analysis of long-term evolution of constructed gully blocks on peatland
- Supports understanding of hydrological storage capacity, sediment infill, and pool dynamics behind dams
- Linked vegetation data allows assessment of ecological responses around dam structures
- Datasets can support modeling of downstream hydrology and inform peatland restoration and nature-based flood risk strategies
- Dataset structure facilitates reproducibility and data discoverability through metadata and clear dam-level observations