# Land Cover Class Areal Coverage (km2) for 20 Chalkstream Catchments in Southern England

## What is included
- A matrix of 12 land cover classes by 20 chalkstream catchment sites, with the area of each land cover class given in km2.
- For each stream site: a GB Ordnance Survey easting/northing grid reference, plus NGR, Easting, and Northing coordinates.
- Land cover totals include a TOTAL_AREA_km2 corresponding to the sum of the class areas.

## Study area and sampling
- 20 discrete chalkstream catchments distributed along white chalk geology from Dorset (southwest) through Wiltshire to Hampshire (northeast).

## Temporal coverage
- Data acquired in July 2012.

## Data collection methods
- Upstream catchment shapefiles were generated using WINFAP-Flood Estimation Handbook 3 software (Wallingford HydroSolutions, 2012) to create catchment boundaries at 50m2 resolution.
- Catchment shapefiles were used to clip the Land Cover Map 2007 (LCM2007) layer (Morton et al., 2014) in ArcGIS, from which the areal coverage of each land cover class was derived.

## Purpose
- To aid site selection for surveying chalkstreams across a gradient of catchment land cover intensification, from predominately calcareous grassland/woodland to predominantly arable/improved grassland.

## Data provenance and interpretation
- Data collected by Dr John Murphy (Queen Mary University of London), assisted by Dr Tom Oliver and Dr Jon Redhead (CEH) for generating catchment land cover data.

## Completeness and quality checks
- Data is complete.
- Visual checks were performed on each catchment shapefile to ensure error-free generation before clipping the LCM2007 layer.

## Data structure and field definitions
- Key identifiers and location
  - RIVER_ID: Unique identifier for each river in Britain
  - SITE_ID: Unique identifier for each sampling location along each river
  - RIVER_NAME: River name (from OS map)
  - SITE_NAME: Site name
  - NGR: Ordnance Survey National Grid Reference
  - EASTING: OS Easting
  - NORTHING: OS Northing
- Land cover data (LCM2007)
  - LCM2007 Broad Habitat Name
  - Units: LCM2007 Broad Habitat class
- Land cover area (all in km2)
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

## References
- Morton, R.D.; Rowland, C.S.; Wood, C.M.; Meek, L.; Marston, C.G.; Smith, G.M. (2014). Land Cover Map 2007 (25m raster, GB) v1.2. NERC Environmental Information Data Centre.
- Wallingford HydroSolutions (2012). WINFAP-FEH 3.