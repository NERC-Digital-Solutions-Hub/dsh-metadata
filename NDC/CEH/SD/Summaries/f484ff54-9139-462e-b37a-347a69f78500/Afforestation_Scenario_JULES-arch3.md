# Supporting Documentation for, Potential afforestation scenarios based on catchment structure and land cover for twelve catchments in Great Britain for use with the Joint UK Land Environment Simulator (JULES)

## Purpose and scope
- Generate afforestation scenarios to assess how both extent and location of broadleaf woodland influence streamflow using the JULES land surface model at 1 km resolution.
- Scenarios vary by catchment structure and land use, producing up to 288 afforestation scenarios per catchment.
- Baseline land cover is CEH 2000; scenarios alter broadleaf and C3 grasses within defined catchment areas.

## Data and access
- Data available under Open Government Licence.
- DOI: 10.5285/f484ff54-9139-462e-b37a-347a69f78500; dataset cited in NERC Environmental Information Data Centre.
- For UK-wide 1 km scale simulations, refer to the CHESS-land dataset (Martinez-de la Torre et al., 2018).
- NetCDF outputs contain eight land cover types; no defined projection in the file (CEH gridded conventions), coordinates in kilometers, British National Grid reference system.

## Catchments included
- Twelve GB catchments: Dee, Tay, Ouse, Ure, Derwent, Thames, Avon, Tamar, Severn (two nested: Severn-B within Severn-HB), Ribble, Clyde.
- Each catchment is linked to a National Gauging Station number (e.g., Dee 12002, Tay 15006, Ouse 27009, etc.).
- Nested catchments: Ure is within Ouse; Severn-B (Severn) is within Severn-HB.

## Methodology for creating afforestation scenarios
- Two catchment properties used to generate scenarios:
  - River network structure (discretisation of watersheds)
  - Land use
- River network structure metrics (calculated from 50 m IHDTM):
  - Topographic Wetness Index (TWI)
  - Strahler order (1 to 7 across GB)
  - Shreve order (1 to 9523, varying by catchment)
- Watersheds are defined downstream from the specified orders; some catchments have minor inconsistencies in Strahler delineation.
- Afforestation extents:
  - Within grassland areas (CEH 2000) at ~25% and ~50% extents, randomly distributed inside catchments.
  - Buffer-based approach around land uses: 25 m and 50 m buffers around Broadleaf woodland, River courses, and Urban areas.
- Two afforestation configurations per catchment:
  - 25 or 50% increase in broadleaf land cover
  - 25 or 50 m buffer around targeted land uses
- Random placement is achieved by generating random points within eligible areas.

## NetCDF conversion and land cover representation
- Outputs converted to a 1 km grid, with eight land surface types:
  1. Broadleaf woodland
  2. Needleleaf woodland
  3. C3 Grasses
  4. C4 Grasses/Shrubs
  5. Crops
  6. Urban Area
  7. Inland Water
  8. Bare Soil
- Each grid cell contains the fraction (0 to 1) of each land surface type in the frac variable.
- Files have no explicit projection defined; coordinates are in kilometers and align with CEH gridded dataset conventions; x and y correspond to easting/northing in the British National Grid system.

## File naming convention and examples
- File name structure:
  < land_cover_base >_< gauging_station >_< buffer_or_percentage >_< location_of_buffering >_< level_of_afforestation >_Br_< catchment_structure_location >_< catchment_structure_order >.nc
- Examples and components:
  - land_cover_base: CEH_2000 (base CEH 2000 land cover)
  - gauging_station: 12002, 15006, 27009, 27034, 27041, 39001, 43021, 47001, 54001, 54057, 71001, 84013
  - buffer_or_percentage: P (percentage increase) or B (buffer increase)
  - location_of_buffering: B (around broadleaf), U (around urban), W (around watercourses), or N (percentage increase, not around a land cover)
  - level_of_afforestation: 25 or 50 (meters for buffers or percentage points for afforestation extent)
  - Br: constant marker indicating broadleaf afforestation
  - catchment_structure_location: Strahler, Shreve, or TWI (or their M-variants for outside areas)
  - catchment_structure_order: numeric order (e.g., 1, 2, 3, …; varies by catchment)
- Example: CEH_2000_54057_P_N_25_Br_Shreve_1.nc
  - CEH_2000 base map
  - Gauging station 54057
  - P indicates 25% increase (not a buffer)
  - N indicates not around a specific land cover type
  - 25% broadleaf afforestation
  - Broadleaf afforestation around Shreve order 1

## Usage guidance
- Scenarios are designed for twelve specified catchments and should not be used to represent afforestation across all of Great Britain.
- For broader GB-scale simulations, use the CHESS-land dataset to drive JULES at 1 km resolution.

## References
- Beven, K. J. and Kirkby, M. J. (1979). A physically based, variable contributing area model of basin hydrology.
- Fuller, R.M. et al. (2002). Land Cover Map 2000 (25m raster, GB).
- Martinez-de la Torre, A. et al. (2018). CHESS-land dataset.
- Morris, D. G. and Flavin, R. W. (1990). A digital terrain model for hydrology.
- O'Callaghan, J. F. and Mark, D. M. (1984). Extraction of drainage networks from digital elevation data.
- Shreve, R. L. (1966). Statistical Law of Stream Numbers.
- Strahler, A. N. (1957). Quantitative analysis of watershed geomorphology.