# Supporting Documentation for, Potential afforestation scenarios based on catchment structure and land cover for twelve catchments in Great Britain for use with the Joint UK Land Environment Simulator (JULES)

## Overview
- Purpose: Generate afforestation scenarios to assess how extent and location of broadleaf afforestation influence streamflow using JULES.
- Coverage: Twelve Great Britain catchments; nested catchments included (Ure within Ouse; Severn-B within Severn-HB).
- Resolution and format: Scenarios provided for use with JULES at 1 km resolution; base JULES configuration documented (Rose suite u-ce663).
- Output scale: Not intended for the entire British Isles; designed for the specified twelve catchments.
- Quantity: Up to 288 afforestation scenarios per catchment (with variations in land cover and spatial arrangement).

## Data inputs and base maps
- Land cover foundation: CEH 2000 Land Cover Map (Fuller et al., 2002).
- Validation reference: CHESS-land dataset (Martinez-de la Torre et al., 2018).
- Land cover types (8 total) and non-plant functional types (3 total):
  - Plant: Broadleaf, Needleleaf, C3 Grasses, C4 Grasses/Shrubs, Crops
  - Non-plant: Bare Ground, Inland Water, Urban
- Spatial alignment: Scenarios re-mapped to a 1 km grid; land-cover fractions per grid cell encoded in netCDF.
- Gauging stations: 12 catchments each linked to a specific National Gauging Station number (e.g., Dee 12002, Tay 15006, Ouse 27009, etc.).

## Catchment structure and discretisation
- Watershed discretisation metrics (for defining afforestation locations):
  - Topographic Wetness Index (TWI)
  - Strahler Order
  - Shreve Order
- Data source and resolution: 50 m IHDTM; D8 flow direction; threshold of ten pixels for stream formation.
- Processing notes: Watersheds generated from downstream points of Strahler/Shreve orders; quantiles used to discretise continuous TWI and large Shreve orders.
- Catchment specifics: Some first-order Strahler catchments may be inconsistently defined across catchments (document notes with details in accompanying table).

## Afforestation scenarios: how they are generated
- Two main afforestation axes:
  1) River network structure-based discretisation (Strahler, Shreve, TWI) to define areas for afforestation.
  2) Land-use-based modifications (buffers around land uses).
- Within-catchment afforestation extents:
  - Approximately 25% and 50% increases in broadleaf woodland within grassland areas (CEH 2000 land cover) at 25 m resolution.
  - Random placement: within catchment areas, afforestation points are generated randomly (Create Random Points tool in ArcGIS 10.6.1).
- Land-use buffers:
  - Buffers around: Broadleaf woodland, River courses, and Urban areas.
  - Buffer distances: 25 m and 50 m.
  - Buffers are discretised relative to river network areas.
- File naming and scenario identifiers:
  - File names encode base land cover, gauging station, type and location of afforestation, extent, catchment structure (Strahler/Shreve/TWI) and order, with “Br” indicating broadleaf-afforestation.
  - Examples illustrate combinations like buffers around urban areas or random afforestation within designated catchment structures and orders.

## Afforestation to NetCDF conversion and output details
- NetCDF construction:
  - Each scenario has eight land cover surface types, plus a fraction field for each type within every 1 km grid cell.
  - The frac variable ranges from 0 to 1 for each land cover type in a grid cell.
  - Land surface type codes in the NetCDF:
    1. Broadleaf woodland
    2. Needleleaf woodland
    3. C3 Grasses
    4. C4 Grasses/Shrubs
    5. Crops
    6. Urban Area
    7. Inland Water
    8. Bare Soil
- Projections and coordinates:
  - NetCDF files do not include a dedicated projection field; they follow CEH gridded dataset conventions.
  - Coordinates are in kilometers and aligned with the British National Grid (x = easting, y = northing).
- Validation:
  - Base maps generated for scenarios are compared against CHESS-land data to ensure accuracy.

## Data access and attribution
- Access: Data released under the Open Government Licence.
- Citation: Buechel, M. (2021). Potential afforestation scenarios based on catchment structure and land cover for twelve catchments in Great Britain for use with the Joint UK Land Environment Simulator (JULES). NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/f484ff54-9139-462e-b37a-347a69f78500
- How to reuse: Cite the above dataset when reusing the data.

## References (key sources)
- Beven, K. J. and Kirkby, M. J. (1979). A physically based, variable contributing area model of basin hydrology.
- Fuller, R.M. et al. (2002). Land Cover Map 2000 (25m raster, GB).
- Martinez-de la Torre, A. et al. (2018). CHESS-land dataset.
- Morris, D. G. and Flavin, R. W. (1990). A digital terrain model for hydrology.
- O'Callaghan, J. F. and Mark, D. M. (1984). The extraction of drainage networks from digital elevation data.
- Shreve, R. L. (1966). Statistical Law of Stream Numbers.
- Strahler, A. N. (1957). Quantitative analysis of watershed geomorphology.