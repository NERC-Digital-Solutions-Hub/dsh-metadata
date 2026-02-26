# Supporting Documentation for, Potential afforestation scenarios based on catchment structure and land cover for twelve catchments in Great Britain for use with the Joint UK Land Environment Simulator (JULES)

## Data access and citation
- Data licensed under Open Government Licence; available at the provided DOI.
- If reused, cite Buechel (2021) and the NERC Environmental Information Data Centre dataset.
- Source for dataset and related metadata: NE/NERC EIDC, with dataset DOI and link.

## Summary of content
- Purpose: generate afforestation scenarios to assess how extent and location of broadleaf afforestation influence streamflow using JULES at 1 km resolution.
- Scope: twelve river catchments in Great Britain; up to 288 afforestation scenarios per catchment; two extents of afforestation (approx. 25% and 50% within grassland areas) and two modes of placement (within catchment structure or around buffers), resulting in diverse scenario nets.
- Output format: land-cover-based scenarios converted to 1 km grid netCDF files compatible with JULES; base configuration information provided (Rose suite u-ce663).

## Catchments and gauging stations
- Twelve catchments with associated National Gauging Station numbers:
  - Dee (12002), Tay (15006), Ouse (27009), Ure (27034), Derwent (27041), Thames (39001), Avon (43021), Tamar (47001), Severn-B (54001), Severn-HB (54057), Ribble (71001), Clyde (84013).
- Nested catchments: Ure within Ouse; Severn-B within Severn-HB.
- Base land cover: CEH 2000 Land Cover Map (Fuller et al., 2002).

## How afforestation scenarios are created
- Two catchment properties used:
  - River network structure (defined by TWI, Strahler order, Shreve order).
  - Land use (derived from CEH 2000 land cover map).
- For each catchment, afforestation is applied under two extents (roughly 25% and 50% increases in broadleaf cover within grassland areas) and in different spatial configurations (buffers around land-cover features) to yield up to 288 scenarios per catchment.
- River network discretisation uses:
  - Topographic Wetness Index (TWI)
  - Strahler order
  - Shreve order
- Calculation workflow uses 50 m IHDTM, D8 flow direction, ArcGIS 10.6.1, and grouping into a manageable number of quantiles.

## Landscape and buffering details
- Land use manipulations:
  - Buffers of broadleaf around three land-use features: broadleaf woodland, river courses, and urban areas.
  - Buffers tested at 25 m and 50 m.
- Afforestation placement:
  - Within catchment areas and across the mapped land-use contexts as described above.
  - Random placement within defined eligible areas using ArcGIS random point generation.

## Data format and conversion to netCDF (for JULES)
- Output conversion:
  - 234–288 scenarios per catchment converted to 1 km grid resolution.
  - Each grid cell contains eight land-cover fractions and an overall surface-type code (z).
- Land-cover coding in netCDF:
  - 1 Broadleaf woodland
  - 2 Needleleaf woodland
  - 3 C3 Grasses
  - 4 C4 Grasses/Shrubs
  - 5 Crops
  - 6 Urban Area
  - 7 Inland Water
  - 8 Bare Soil
- frac variable stores the fraction of each land-cover type in a grid cell (0 to 1).
- Projections:
  - NetCDF files contain no defined projection within the file; they follow CEH gridded dataset conventions with x and y in kilometers and aligned with the British National Grid (true easting and northing in km).
- File naming convention:
  - Structure: < land_cover_base >_< gauging_station >_< buffer_or_percentage >_< location_of_buffering >_< level_of_afforestation >_Br_< catchment_structure_location >_< catchment_structure_order >.nc
  - Examples and parts:
    - land_cover_base: CEH_2000
    - gauging_station: 12002, 15006, 27009, 27034, 27041, 39001, 43021, 47001, 54001, 54057, 71001, 84013
    - buffer_or_percentage: P (percentage increase) or B (buffer increase)
    - location_of_buffering: B, U, W (around Broadleaf, Urban, Watercourses) or N (no around-feature buffering)
    - level_of_afforestation: 25 or 50
    - Br: always present to denote broadleaf afforestation
    - catchment_structure_location: Strahler, Shreve, or TWI (and outside variants)
    - catchment_structure_order: the order number per catchment (e.g., 1 for Strahler/Shreve within certain orders)
  - Example: CEH_2000_54057_P_N_25_Br_Shreve_1.nc

## Usage and references
- Designed for integration with the JULES land surface model (base Rose suite: u-ce663) and CHESS-land comparison datasets (Martinez-de la Torre et al., 2018) for broader benchmarking.
- Key methodological references include foundational hydrology and land-surface modelling sources: Beven & Kirkby (1979), Morris & Flavin (1990), O’Callaghan & Mark (1984), Strahler (1957), Shreve (1966), and related CEH and CHESS datasets.

## Notes on reproducibility and data reuse
- Data are provided with clear licensing and citation requirements; users should reference the original Buechel (2021) dataset and adhere to the Open Government Licence terms.
- The documentation outlines the exact structure of afforestation scenarios, naming conventions, and data formats to facilitate data discovery, integration, and reuse in policy-support and hydrological impact analyses.