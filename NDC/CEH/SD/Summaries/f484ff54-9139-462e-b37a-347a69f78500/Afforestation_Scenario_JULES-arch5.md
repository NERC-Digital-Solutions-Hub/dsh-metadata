# Supporting Documentation for, Potential afforestation scenarios based on catchment structure and land cover for twelve catchments in Great Britain for use with the Joint UK Land Environment Simulator (JULES)

- Data access and licensing
  - Data are available under the Open Government Licence.
  - Dataset available via the NERC Environmental Information Data Centre with a DOI: https://doi.org/10.5285/f484ff54-9139-462e-b37a-347a69f78500
  - Reuse requires citation: Buechel, M. (2021). Potential afforestation scenarios... NERC EIDC dataset. https://doi.org/10.5285/f484ff54-9139-462e-b37a-347a69f78500

- Purpose and scope
  - Generates afforestation scenarios to assess how extent and location of broadleaf afforestation influence streamflow.
  - Output format compatible with JULES at 1 km resolution.
  - Covers twelve GB catchments; up to 288 afforestation scenarios per catchment.
  - Not intended for running across all GB; refer to CHESS-land for broader 1 km scale simulations.

- Data content and structure
  - Land cover framework
    - Eight land surface types: five plant functional types (Broadleaf, Needleleaf, C3 Grasses, C4 Grasses/Shrubs, Crops) and three non-plant types (Bare Ground, Inland Water, Urban).
    - NetCDF-based data with z representing land surface type (values 1–8) and frac representing the fraction of each land surface type within a 1 km cell (0 to 1).
  - Spatial resolution and projection
    - 1 km grid, British National Grid coordinates (x = easting, y = northing) in km units.
    - NetCDF files follow CEH gridded dataset conventions; no explicit projection defined in the NetCDF metadata.
  - Data provenance
    - Base land maps derived from CEH 2000 Land Cover Map (Fuller et al., 2002).
    - CHESS-land dataset referenced for broader GB-scale simulations (Martinez-de la Torre et al., 2018).

- Methodology for creating afforestation scenarios
  - Two catchment properties used to discretize the catchment and guide afforestation:
    - River network structure: Topographic Wetness Index (TWI), Strahler order, and Shreve order (calculated from 50 m IHDTM; D8 flow direction in ArcGIS 10.6.1).
    - Land use: buffers around broadleaf woodland, rivers, and urban areas derived from CEH 2000 land cover, generated at 25 m resolution.
  - Afforestation extents and placement
    - Two extents tested per catchment: approximately 25% and 50% within grassland areas.
    - Afforestation planted randomly within defined catchment areas using random point generation in ArcGIS.
    - Buffers applied around existing land covers to create additional scenarios.
  - Output and conversion
    - Between 234 and 288 scenarios per catchment.
    - Scenarios converted to 1 km grid by computing the fraction of each surface type within each cell.
    - Python, using rasterio and netCDF4, creates netCDF files suitable for JULES.
    - Base maps validated against CHESS-land for accuracy.

- File naming conventions and contents
  - Example file naming structure: <land_cover_base>_<gauging_station>_<buffer_or_percentage>_<location_of_buffering>_<level_of_afforestation>_Br_<catchment_structure_location>_<catchment_structure_order>.nc
  - Key components
    - land_cover_base: CEH_2000 (all files use CEH 2000 map)
    - gauging_station: associated NRFA station number (e.g., 12002, 15006, 27009, etc.)
    - buffer_or_percentage: P (percentage increase) or B (buffer increase)
    - location_of_buffering: B (around broadleaf), U (around urban), W (around watercourses), or N (no specific buffering)
    - level_of_afforestation: 25 or 50 (extent or percentage increase)
    - Br: indicates broadleaf as the afforestation target
    - catchment_structure_location: Strahler, Shreve, or TWI (or outside of these)
    - catchment_structure_order: numerical order value (varies by catchment; e.g., 1, 2, 5, 7 as defined per catchment)
  - Example: CEH_2000_54057_P_N_25_Br_Shreve_1.nc

- Use and limitations
  - Designed for use with JULES; no overarching GB-wide applicability; refer to CHESS-land for broader GB-scale scenarios.
  - Some catchments have edge cases in order assignments (e.g., Strahler/ Shreve / TWI inside vs outside watershed areas) noted in the documentation.
  - Data are intended to document and compare the influence of afforestation patterns on hydrology, not to provide a single definitive forecast.

- References and data sources
  - Beven, K. J. and Kirkby, M. J. (1979)
  - Fuller, R.M. et al. (2002)
  - Martinez-de la Torre, A. et al. (2018)
  - Morris, D. G. and Flavin, R. W. (1990)
  - O'Callaghan, J. F. and Mark, D. M. (1984)
  - Shreve, R. L. (1966)
  - Strahler, A. N. (1957)