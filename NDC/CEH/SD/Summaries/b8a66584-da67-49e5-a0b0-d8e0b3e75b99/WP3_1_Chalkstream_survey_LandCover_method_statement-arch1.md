# Land cover data for chalkstream catchments in southern England

- What is recorded and in what form
  - Areal coverage (km2) of 12 land cover classes recorded for each of 20 chalkstream catchments.
  - Data arranged as a matrix: 12 land cover classes by 20 stream sites, with area values in km2.
  - Each stream site includes a GB Ordnance Survey grid reference (NGR), Easting, and Northing.

- Study area and timing
  - 20 chalkstream catchments distributed along white chalk geology from Dorset (SW) to Hampshire (NE) in southern England.
  - Data collection conducted in July 2012.

- Data collection and preprocessing
  - Upstream catchment shapefiles generated with WINFAP-FEH 3 software (50 m2 resolution).
  - Catchment shapefiles used to clip the Land Cover Map 2007 (LCM2007) to derive areal coverage for each catchment (via ArcGIS Clip).
  - Visual QA performed on catchment shapefiles to ensure error-free generation before clipping LCM2007.

- Purpose and use
  - Aimed to aid site selection for surveying chalkstreams along a gradient of catchment land cover intensification—from calcareous grassland/woodland to arable/improved grasslands.

- Data structure and fields
  - Identifiers: RIVER_ID (unique river), SITE_ID (site along river), RIVER_NAME, SITE_NAME, NGR, EASTING, NORTHING.
  - Land cover classes (12; units: km2): Broadleaved_km2, Coniferous_km2, Arable_km2, Impr_Grass_km2, Acid_Grass_km2, Neut_Grass_km2, Calc_Grass_km2, Rough_Grass_km2, Heath_km2, Built_Area_km2, Rock_km2, Freshwater_km2.
  - TOTAL_AREA_km2 for each catchment.
  - Land cover classifications aligned with LCM2007 Broad Habitat Names.

- Data quality and completeness
  - Completeness: data are complete.
  - Quality checks: visual verification of catchment shapefiles prior to clipping.

- Data sources and references
  - Land Cover Map 2007 (GB, 25 m raster) v1.2; Morton et al. 2014.
  - WINFAP-FEH 3; Wallingford HydroSolutions (2012).
  - DOI for LCM2007: https://doi.org/10.5285/a1f88807-4826-44bc-994da902da5119c2