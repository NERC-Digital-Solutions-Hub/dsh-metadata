# What has been recorded and what form does the data take?

- Data describe the areal coverage (in km2) of 12 land cover classes for 20 chalkstream catchments in southern England.
- Data structure: a matrix of 12 land cover classes by 20 stream sites, with the area of each land cover class provided in km2.
- Each stream site also has a GB Ordnance Survey easting/northing grid reference (NGR), including Easting and Northing coordinates.

## Location, scope, and timeframe

- Spatial scope: 20 discrete chalkstream catchments distributed along white chalk geology from Dorset (southwest) through Wiltshire to Hampshire (northeast).
- Data collection period: July 2012.

## Data creation and transformations

- Upstream catchment shapefiles (50 m2 resolution) were generated using WINFAP-FEH 3 software.
- Catchment shapefiles were used to clip a Land Cover Map 2007 (LCM2007) layer to derive land cover areas for each catchment (via ArcGIS Clip).
- The dataset is derived from the LCM2007 25 m raster layer (Morton et al., 2014).

## Purpose and use

- Primary purpose: aid site selection for surveying chalkstreams across a gradient of catchment land cover intensification (e.g., calcareous grassland/woodland vs arable/improved grassland).

## Responsible parties and provenance

- Data collection and interpretation led by Dr John Murphy (Queen Mary University of London), with assistance from Dr Tom Oliver and Dr Jon Redhead (CEH).

## Metadata, completeness, and quality checks

- Completeness: the data are complete.
- Quality checks: visual verification of each catchment shapefile to ensure error-free generation before clipping LCM2007.

## Data fields and structure (column definitions)

- Identifiers and location:
  - RIVER_ID: Unique river identifier in Britain
  - SITE_ID: Unique sampling location identifier
  - RIVER_NAME: River name (from OS map)
  - SITE_NAME: Site name
  - NGR: Ordnance Survey National Grid Reference
  - EASTING: OS Easting
  - NORTHING: OS Northing
- Land cover data (LCM2007 Broad Habitat Name) with units in km2:
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
- Note: The table shows some formatting inconsistencies in the column definitions, but the intended fields are as listed above.

## Data provenance and references

- Morton, R.D.; Rowland, C.S.; Wood, C.M.; Meek, L.; Marston, C.G.; Smith, G.M. (2014). Land Cover Map 2007 (25m raster, GB) v1.2. NERC Environmental Information Data Centre. https://doi.org/10.5285/a1f88807-4826-44bc-994da902da5119c2
- Wallingford HydroSolutions (2012). WINFAP-FEH 3. http://www.hydrosolutions.co.uk/software-5-5.asp

## Data access and governance considerations ( Data Stewards perspective )

- Data lineage is clear: from WINFAP-FEH 3-derived catchment shapefiles to clipping LCM2007 to produce per-catchment land cover totals.
- Metadata coverage covers identifiers, location, methodology, and data sources; consider expanding to include data license, access rights, and any embargo or usage restrictions if sharing.
- Interoperability notes: uses standard UK datasets (LCM2007, OS grid references) and a defined clipping process, aiding reproducibility and reuse across similar governance workflows.
- Potential governance needs:
  - Explicit data licensing and usage terms for the clipped LCM2007-derived outputs.
  - Versioning and update plan if input datasets (LCM2007 or catchment boundaries) are revised.
  - Documentation of any assumptions or edge cases in the clipping process, to support data users and future audits.