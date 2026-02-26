# Supporting Documentation for, Potential afforestation scenarios based on catchment structure and land cover for twelve catchments in Great Britain for use with the Joint UK Land Environment Simulator (JULES)

- Purpose: Document afforestation scenarios to assess how extent and location of broadleaf afforestation influence streamflow using JULES at 1 km resolution.
- Scope: Twelve GB catchments (with two nested catchments: Ure inside Ouse; Severn-Bew inside Severn-HB); scenarios are tailored to these catchments and should not be applied to the entire GB. Data can be used with CHESS-land as needed for UK-wide 1 km runs.
- Output format: netCDF files compatible with JULES; base maps aligned with CHESS-land conventions; no defined projection in files (British National Grid conventions in x/y units with km).

Data and content
- Land cover types: eight surface types, five plant functional types
  - Plant: Broadleaf, Needleleaf, C3 Grasses, C4 Grasses/Shrubs, Crops
  - Non-plant: Bare Ground, Inland Water, Urban
- Spatial resolution: 1 km grid
- Base data: CEH 2000 Land Cover Map (Fuller et al., 2002)
- Maximum number of scenarios: up to 288 afforestation scenarios per catchment (234–288 range reported)
- Catchments and gauging stations: Twelve catchments with listed National Gauging Station numbers; two nested catchments (Ure within Ouse; Severn-Bew within Severn-HB)

Afforestation scenario design
- Two catchment properties used to generate scenarios:
  - River network structure
  - Land use
- Afforestation extents per catchment: tested at approximately 25% and 50% within grassland areas
- Random assignment: planted area determined by random point generation within catchment areas
- Land use modifications: buffers around CEH 2000 land cover classes including broadleaf woodland, river courses, and urban areas
  - Buffers set at 25 m and 50 m
- Scenario distribution: scenarios vary by combination of catchment structure and land use changes
- Special notes: running these scenarios outside the specified catchments or beyond the stated extents is not advised

River network structure and catchment discretisation
- Metrics used to delineate watersheds and locations for afforestation:
  - Topographic Wetness Index (TWI)
  - Strahler order
  - Shreve order
- Data sources and processing:
  - Derived from 50 m IHDTM
  - Stream formation uses a threshold of ten pixels with D8 flow direction
- The TWI formula and the interpretation of higher orders:
  - TWI = ln(a / tan(γ)); a = upslope contributing area per unit contour length; γ = local slope
  - TWI and Shreve order are grouped into multiple quantiles (TWI: five quantiles; Shreve: seven quantiles)
- Watershed creation: downstream point of Shreve and Strahler orders
- Limitations: some catchments show inconsistencies (e.g., some Strahler catchments appear only inside or outside defined watersheds)

Afforestation: land-use and location specifics
- Broadleaf buffers around three land-use types:
  - Broadleaf woodland
  - River courses
  - Urban areas
- Buffer sizes: 25 m and 50 m
- Discretisation by river-network areas to align with catchment structure (Strahler/Shreve/TWI)

NetCDF conversion and file content
- Grid and data transformation:
  - 234–288 scenarios converted to 1 km grid by computing the fraction of each land-cover type within each grid cell
  - Output includes eight land-cover fractions per cell
- NetCDF structure:
  - z: land surface type code (1–8) corresponding to land-cover categories
  - frac: fraction of each land-cover type in a grid cell (0 to 1)
  - Coordinates: in kilometers; aligns with CEH gridded conventions; British National Grid origin (x = easting, y = northing)
  - No explicit projection metadata defined in the NetCDF file
- Land-cover codes (z) mapping:
  1. Broadleaf woodland
  2. Needleleaf woodland
  3. C3 Grasses
  4. C4 Grasses/Shrubs
  5. Crops
  6. Urban Area
  7. Inland Water
  8. Bare Soil

File naming convention and examples
- Structure: <land_cover_base>_<gauging_station>_<buffer_or_percentage>_<location_of_buffering>_<level_of_afforestation>_Br_<catchment_structure_location>_<catchment_structure_order>.nc
- Key components:
  - land_cover_base: CEH_2000 (CEH 2000 land cover base)
  - gauging_station: 12002, 15006, 27009, 27034, 27041, 39001, 43021, 47001, 54001, 54057, 71001, 84013
  - buffer_or_percentage: P (percentage increase) or B (buffer increase)
  - location_of_buffering: B (around broadleaf), U (around urban), W (around watercourses), or N (percentage increase not location-specific)
  - level_of_afforestation: 25 or 50 (m buffers or percentage increase values)
  - Br: fixed tag indicating broadleaf afforestation
  - catchment_structure_location: Strahler, Shreve, or TWI (and Outside variants)
  - catchment_structure_order: order number for the specified structure (varies by catchment)
- Example:
  - CEH_2000_54057_P_N_25_Br_Shreve_1.nc
    - CEH_2000 base map
    - Gauging station 54057
    - P = 25% increase
    - N = percentage increase not tied to a land-cover type
    - 25 = 25% increase in broadleaf afforestation
    - Br = broadleaf
    - Shreve_1 = Shreve order 1
- Note: orders and catchment-location labels reflect catchment-specific tables (e.g., Strahler, Shreve, TWI, and outside variants)

Data access and references
- Access: Open Government Licence; data DOI provided
- Citation: Buechel, M. (2021). Potential afforestation scenarios based on catchment structure and land cover for twelve catchments in Great Britain for use with the Joint UK Land Environment Simulator (JULES). NERC Environmental Information Data Centre. Dataset. DOI provided
- Core references for methodologies and datasets used (Beven & Kirkby; Fuller et al.; Martinez-de la Torre et al.; Morris & Flavin; O'Callaghan & Mark; Shreve; Strahler)

Implementation notes for GIS specialists
- Data interoperability: netCDF files designed for JULES; ensure alignment with CHESS-land for cross-compatibility
- Coordinate handling: in-kilometer units; no explicit projection metadata in NetCDF; convert or reproject as needed to match local GIS workflows while preserving x/y consistency
- Data handling scale: 1 km grid; up to 288 scenarios per catchment; plan for storage and processing accordingly
- Caution on scope: not intended for nationwide GB simulations; use within defined catchments and refer to CHESS-land for broader-scale runs if required