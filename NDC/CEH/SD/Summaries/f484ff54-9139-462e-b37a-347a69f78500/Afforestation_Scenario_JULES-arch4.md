# Supporting Documentation for, Potential afforestation scenarios based on catchment structure and land cover for twelve catchments in Great Britain for use with the Joint UK Land Environment Simulator (JULES)

## Overview
- Purpose: Generate afforestation scenarios to assess how extent and location of broadleaf afforestation influence streamflow using JULES.
- Scale and format: Scenarios are created at 1 km resolution; up to 288 afforestation scenarios per catchment.
- Base data: Built on CEH 2000 Land Cover Map; scenarios are designed for twelve specified catchments in Great Britain and are not intended for nationwide UK use.
- Accessibility: Data are Open Government Licence; citation required when reused.

## Data Access and Licensing
- Data license: Open Government Licence.
- Availability: Data accessible via provided DOI.
- Citation: Buechel, M. (2021). NERC Environmental Information Data Centre dataset.

## Data Content
- Land cover types: Eight land surface types plus three non-plant types.
  - Plant functional types: Broadleaf, Needleleaf, C3 Grasses, C4 Grasses/Shrubs, Crops.
  - Non-plant: Bare Ground, Inland Water, Urban.
- Spatial framework: NetCDF files for 1 km grid cells; fraction of each land cover type within each cell (frac variable; 0 to 1).
- Reference framework: Base maps from CEH 2000 Land Cover Map; local land cover references align with CHESS-land dataset conventions for UK-scale comparisons.
- Catchments: Twelve catchments with associated gauging stations; includes nested catchments:
  - Ure within Ouse
  - Severn-B within Severn-HB
- File count: Up to 288 scenarios per catchment; total scope includes 12 catchments.

## Methodology: Creation of Afforestation Scenarios
- Two catchment properties used to generate scenarios:
  1) River network structure
  2) Land use
- Afforestation extents: Approximately 25% and 50% within grassland areas; planted areas are allocated randomly within catchment boundaries.
- Land-use-based modifications: Buffers around three land-use features (Broadleaf woodland, River courses, Urban areas) using 25 m and 50 m buffers.
- Scenario range: Up to 288 combinations per catchment derived from varying extents and buffering strategies.

## River Network Structure and Land Use Details
- River network discretisation metrics (based on Strahler and Shreve orders and Topographic Wetness Index, TWI):
  - Strahler order: 1 (headwaters) to 7 (lowlands)
  - Shreve order: 1 to 9523 (varies by catchment)
  - TWI: Continuous 0.05–31.49 range
- Watershed delineation: Generated from downstream points of Strahler/Shreve orders; 50 m IHDTM data used; D8 flow direction algorithm applied; watersheds grouped into quantiles.
- Land-use framework: CEH 2000 land cover; buffers around broadleaf woodland, rivers, and urban areas discretised by river network areas as above.
- Output scope: Scenarios created separately for each catchment area, with afforestation applied both inside and outside defined watersheds.

## NetCDF Conversion and File Details
- Grid resampling: 1 km grid scale; fractions per land cover type computed per cell and combined into NetCDF files.
- Land surface type coding (z):
  1) Broadleaf woodland
  2) Needleleaf woodland
  3) C3 Grasses
  4) C4 Grasses/Shrubs
  5) Crops
  6) Urban Area
  7) Inland Water
  8) Bare Soil
- Metadata: NetCDFs follow CEH gridded dataset conventions; coordinates (x,y) in kilometers; British National Grid system; no explicit projection defined within NetCDF.
- Tools used: Python (rasterio, netCDF4) for computing fractions and assembling final NetCDF files.
- Base comparison: Generated maps compared to CHESS-land dataset for accuracy.

## File Naming Convention
- Example: CEH_2000_54057_P_N_25_Br_Shreve_1.nc
- Meaning of fields:
  - CEH_2000: Land cover base map (CEH 2000)
  - 54057: Gauging station number for the catchment
  - P: Percentage increase in broadleaf afforestation (as opposed to B for buffer)
  - N: Buffering around land-cover types (N = not around a specific land cover)
  - 25: 25% increase (or 25 m buffer) in afforestation
  - Br: Broadleaf as the afforestation target
  - Shreve: Catchment discretisation method (Shreve)
  - 1: Specific catchment structure order
  - .nc: NetCDF file extension
- Possible values:
  - < land_cover_base >: CEH_2000
  - < gauging_station >: 12,002; 15,006; 27,009; 27,034; 27,041; 39,001; 43,021; 47,001; 54,001; 54,057; 71,001; 84,013
  - < buffer_or_percentage >: P (percentage) or B (buffer)
  - < location_of_buffering >: B (broadleaf around land cover), U (around urban), W (around watercourses), or N (not around)
  - < level_of_afforestation >: 25 or 50
  - < catchment_structure_location >: Strahler, Shreve or TWI
  - < catchment_structure_order >: order number per catchment

## Catchments Included
- Dee (Gauging station 12002)
- Tay (15006)
- Ouse (27009)
- Ure (27034)
- Derwent (27041)
- Thames (39001)
- Avon (43021)
- Tamar (47001)
- Severn(-B) (54001)
- Severn(-HB) (54057)
- Ribble (71001)
- Clyde (84013)

Notes on catchment structure
- Nested configurations: Ure inside Ouse; Severn-B inside Severn-HB
- Reference catchment maps and gauging station details available in accompanying tables and figures

## References
- Beven, K. J. and Kirkby, M. J. (1979). Beven & Kirkby hydrology model.
- Fuller, R.M. et al. (2002). CEH Land Cover Map 2000.
- Martinez-de la Torre, A. et al. (2018). CHESS-land dataset.
- Morris, D. G. and Flavin, R. W. (1990). Digital terrain model for hydrology.
- O'Callaghan, J. F. and Mark, D. M. (1984). Drainage networks from digital elevation data.
- Shreve, R. L. (1966). Statistical law of stream numbers.
- Strahler, A. N. (1957). Quantitative analysis of watershed geomorphology.