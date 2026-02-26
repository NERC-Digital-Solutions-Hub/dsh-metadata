# Supporting Documentation for, Potential afforestation scenarios based on catchment structure and land cover for twelve catchments in Great Britain for use with the Joint UK Land Environment Simulator (JULES)

- Objective
  - Produce afforestation scenarios to evaluate how extent and location of broadleaf woodlands affect streamflow using the JULES land surface model.
  - Scenarios are formatted for JULES at 1 km resolution; base configuration is Rose suite u-ce663.

- Data coverage
  - Twelve river catchments in Great Britain; base land cover from CEH 2000 Land Cover Map.
  - Eight land cover surface types with five plant functional types (Broadleaf, Needleleaf, C3 Grasses, C4 Grasses/Shrubs, Crops) and three non-plant types (Bare Ground, Inland Water, Urban).
  - Up to 288 afforestation scenarios per catchment (0 to ~40 percentage-point increase in broadleaf woodland).
  - Catchments include two nested cases: Ure inside Ouse; Severn at Bewdley inside Severn at Haw Bridge.
  - Not designed to cover the entire Great Britain; reference CHESS-land dataset for 1 km-scale GB-wide simulations if needed.

- Catchment and land-surface properties used
  - River network structure discretised with:
    - Topographic Wetness Index (TWI)
    - Strahler order
    - Shreve order
  - Calculations based on 50 m IHDTM, D8 flow, ArcGIS 10.6.1.
  - TWI computed as ln(a/tanγ) with a upslope contributing area and γ slope.
  - Strahler orders: 1 (headwaters) to 7 (lowlands); Shreve orders range widely up to 9523.
  - Watersheds are formed downstream from the Shreve and Strahler orders; some first-order Strahler catchments are noted as misclassified in Table 2.

- Afforestation design approach
  - Afforestation scenarios defined by two properties:
    - River network structure (discretisation by Strahler/Shreve/TWI)
    - Land use (buffers around land-cover types)
  - Within grassland areas (per CEH 2000 map) two extents tested: ~25% and ~50% within catchments.
  - Random planting: probability-based placement within available catchment area using GIS random point generation.
  - Buffers around land-use features:
    - Broadleaf woodland
    - River courses
    - Urban areas
  - Buffers created at 25 m and 50 m; buffers are discretised according to river-network-defined areas.

- Output data and format
  - NetCDF files aligned to 1 km grid; multiple land-cover types represented within each cell.
  - Land-surface type coding (z) uses 1–8:
    1. Broadleaf woodland
    2. Needleleaf woodland
    3. C3 Grasses
    4. C4 Grasses/Shrubs
    5. Crops
    6. Urban Area
    7. Inland Water
    8. Bare Soil
  - frac variable records the fraction of each land-cover type in a grid cell (0 to 1).
  - Coordinate system: CEH CHESS conventions; x and y in kilometers; British National Grid (false origin), no explicit projection stored in the NetCDF.
  - NetCDF creation uses Python with rasterio and netCDF4; base maps checked against CHESS-land dataset for accuracy.

- File naming convention and examples
  - Structure: <land_cover_base>_<gauging_station>_<buffer_or_percentage>_<location_of_buffering>_<level_of_afforestation>_Br_<catchment_structure_location>_<catchment_structure_order>.nc
  - Values:
    - land_cover_base: CEH_2000
    - gauging_station: 12002, 15006, 27009, 27034, 27041, 39001, 43021, 47001, 54001, 54057, 71001, 84013
    - buffer_or_percentage: P (percentage increase) or B (buffer increase)
    - location_of_buffering: B (broadleaf), U (urban), W (watercourses), or N (no around existing land cover)
    - level_of_afforestation: 25 or 50
    - Br: fixed to indicate broadleaf afforestation
    - catchment_structure_location: Strahler, Shreve, or TWI (and variations like StrahlerM, ShrevM, TWM)
    - catchment_structure_order: numeric order per catchment (e.g., 1, 2, …)
  - Example: CEH_2000_54057_P_N_25_Br_Shreve_1.nc
    - CEH_2000 base map
    - gauging station 54057
    - 25% broadleaf increase
    - N = not around a specific land-cover type
    - 25% increase in broadleaf afforestation
    - Shreve-based discretisation
    - order 1

- Data access and citation
  - Data available under Open Government Licence
  - DOI: 10.5285/f484ff54-9139-462e-b37a-347a69f78500
  - Citation: Buechel, M. (2021). Potential afforestation scenarios based on catchment structure and land cover for twelve catchments in Great Britain for use with the Joint UK Land Environment Simulator (JULES). NERC Environmental Information Data Centre (Dataset). https://doi.org/10.5285/f484ff54-9139-462e-b37a-347a69f78500

- Usage with JULES and references
  - Files are designed to be used directly with JULES; base configuration documented as Rose suite u-ce663.
  - For broader GB-scale simulations at 1 km, refer to CHESS-land (Martinez-de la Torre et al., 2018).

- References (selected)
  - Beven, Beven & Kirkby (1979) on dynamic basin hydrology.
  - Fuller et al. (2002) CEH Land Cover Map 2000.
  - Martinez-de la Torre et al. (2018) CHESS-land dataset.
  - Morris & Flavin (1990); O'Callaghan & Mark (1984); Shreve (1966); Strahler (1957).