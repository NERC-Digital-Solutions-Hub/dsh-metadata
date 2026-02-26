# Land cover data for chalkstreams catchments in southern England

- Overview
  - A dataset recording the areal extent (km2) of 12 land cover classes for 20 chalkstream catchments in southern England, with site coordinates for mapping.
  - Collected in July 2012 to support sampling across a gradient of catchment land cover intensification.

- Data content and format
  - Data structure: matrix of 12 land cover classes by 20 stream sites, with the area of each class in km2.
  - Spatial references: GB Ordnance Survey easting and northing grid references for each stream site.
  - Land cover classes (km2, from LCM2007 Broad Habitat Names): 
    - Broadleaved_km2
    - Coniferous_km2
    - Arable_km2
    - Impr_Grass_km2
    - Acid_Grass_km2
    - Neut_Grass_km2
    - Calc_Grass_km2
    - Rough_Grass_km2
    - Heath_km2
    - Built_Area_km2
    - Rock_km2
    - Freshwater_km2
    - TOTAL_AREA_km2
  - Column-related identifiers include RIVER_ID, SITE_ID, RIVER_NAME, SITE_NAME, NGR, EASTING, NORTHING.

- Spatial and temporal coverage
  - Study area: 20 chalkstream catchments distributed along white chalk geology from Dorset (southwest) through Wiltshire to Hampshire (northeast).
  - Time of data collection: July 2012.

- Data collection methods
  - Catchment delineation: Upstream catchment shapefiles generated with WINFAP-Flood Estimation Handbook 3 (FEH3) software at ~50 m2 resolution.
  - Land cover extraction: Catchment shapefiles used to clip the Land Cover Map 2007 (LCM2007, 25 m raster) to each catchment (ArcGIS Clip tool).
  - Areal calculation: Derive areal coverage of each land cover class from clipped LCM2007 data.

- Purpose and use
  - Primary aim: Aid site selection for surveying chalkstreams across a gradient of catchment land cover intensification (calcareous grassland/woodland vs. arable/improved grassland).
  - Outputs intended to support analysis, visualization, and potential self-serve data exploration for end users.

- Data provenance and quality
  - Responsible researchers: Dr John Murphy (Queen Mary University of London), assisted by Dr Tom Oliver and Dr Jon Redhead (CEH) in generating catchment land cover data.
  - Completeness: Data is reported as complete.
  - Quality checks: Visual verification of catchment shapefiles prior to clipping the LCM2007 layer to ensure error-free generation.

- Data schema and definitions
  - Key identifiers: 
    - RIVER_ID: Unique river identifier in Britain
    - SITE_ID: Unique sampling location identifier along each river
    - RIVER_NAME: River name (from OS map)
    - SITE_NAME: Site name
    - NGR, EASTING, NORTHING: Spatial coordinates (OS National Grid)
  - Land cover data: 12 broad habitat classes with area in km2 (as listed above) plus TOTAL_AREA_km2.

- Documentation and references
  - Morton, R.D.; Rowland, C.S.; Wood, C.M.; Meek, L.; Marston, C.G.; Smith, G.M. (2014). Land Cover Map 2007 (25m raster, GB) v1.2. NERC Environmental Information Data Centre.
  - Wallingford HydroSolutions (2012). WINFAP-FEH 3 software.