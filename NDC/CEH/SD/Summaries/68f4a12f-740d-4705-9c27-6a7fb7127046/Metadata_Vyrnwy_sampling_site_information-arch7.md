# Dyfnant Forest draining in to Llyn Vyrnwy

## Overview
- A multi-feature environmental dataset focused on the Dyfnant Forest catchment draining into Llyn Vyrnwy.
- Combines rainfall, ephemeral streams, and boreholes with associated soil, vegetation, and land management attributes.
- Supports GIS-based analysis of hydrochemistry and forested catchments in mid-Wales.

## Datasets included
- Vyrnwy Rainfall
  - Location codes: AA
  - Coordinates (lat/long): 52.7593, -3.4833; altitude 350 m
  - Description: Continuously open rain collector in open moorland above forest
  - Main soil/vegetation: Podzol; Acid grassland
  - Land management: Rough grazing
  - Temporal coverage: 5-Dec-1994 to 16-Feb-2001
  - Reference number: 10
- Vyrnwy1 Stream
  - Location code: W
  - Coordinates: 52.7860, -3.4309; altitude 320 m
  - Description: Ephemeral stream in Dyfnant Forest draining into Afon Hirnant
  - Main soil/vegetation: Brown Earth; Plantation Sitka spruce forest
  - Land management: 100% clearfelled (April 1997)
  - Temporal coverage: 7-Oct-1994 to 16-Feb-2001
  - Reference number: 10
- Vyrnwy2 Stream
  - Location code: X
  - Coordinates: 52.7796, -3.5107; altitude 258 m
  - Description: Ephemeral stream in Dyfnant Forest draining into Llyn Vyrnwy
  - Main soil/vegetation: Brown Earth; Plantation Sitka spruce forest
  - Land management: Vyrnwy 1 stream control; standing crop
  - Temporal coverage: 7-Oct-1994 to 16-Feb-2001
  - Reference number: 10
- Vyrnwy1 Borehole
  - Location code: Y
  - Coordinates: 52.7860, -3.4309; altitude 320 m
  - Description: By ephemeral stream in Dyfnant Forest draining into Afon Hirnant
  - Main soil/vegetation: Brown Earth; Plantation Sitka spruce forest
  - Land management: Clearfelled April 1997
  - Temporal coverage: 7-Oct-1994 to 16-Feb-2001
  - Reference number: 10
- Vyrnwy2 Borehole
  - Location code: Z
  - Coordinates: 52.7796, -3.5107; altitude 258 m
  - Description: By roadside near ephemeral stream
  - Main soil/vegetation: Brown Earth; Plantation Sitka spruce forest
  - Land management: Standing crop (control for Vyrnwy 1 borehole)
  - Temporal coverage: 7-Oct-1994 to 16-Feb-2001
  - Reference number: 10

## Spatial and temporal coverage
- Spatial reference: WGS84 (lat/long provided); plus OS-like local coordinates (Easting/Northing) for each feature.
- Elevation range: ~258–350 m
- Area context: Ephemeral streams, forested catchments, and rainfall collection sites within Dyfnant Forest and near Llyn Vyrnwy
- Temporal span: 7-Oct-1994 to 16-Feb-2001 for streams, boreholes, and rainfall data

## Attributes and data structure
- Features include rainfall points, streams, and boreholes with classification by location code and descriptive fields.
- Associated environmental metadata per feature:
  - Soil types: Podzol; Brown Earth
  - Vegetation: Acid grassland; Plantation Sitka spruce forest
  - Land management: Rough grazing; clearfelling; standing crop control
  - Mining: None/N/A
- Reference identifiers: Reference number 10 across components
- Primary references: Neal C., Reynolds B., Neal M. and Williams B. 2004; "Vyrnwy: streams, groundwater and rainfall" in Hydrology and Earth System Sciences (Hydrol. Earth Syst. Sci., 8, 460-484)

## Usage considerations for GIS specialists
- Enables map-based visualization of hydrological components (rainfall, ephemeral streams, boreholes) within the Dyfnant–Vyrnwy system.
- Useful for spatial analysis of hydrochemistry relationships in plantation forest catchments (as discussed in the primary reference).
- Data integration requires attention to differing data resolutions and potential mismatches in data standards across features.
- Suitable for creating layered map products showing land management history (e.g., 1997 clearfelling), soil/vegetation context, and hydrological connectivity.

## Primary references
- Vyrnwy: streams, groundwater and rainfall, Neal C., Reynolds B., Neal M., and Williams B., 2004. Hydrol. Earth Syst. Sci., 8, 460-484.