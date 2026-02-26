# Land Cover Data for Chalkstream Catchments in Southern England

## What has been recorded and what form does the data take
- A matrix of 12 land cover classes by 20 stream sites, with the area of each land cover class given in square kilometers (km2).
- For each stream site, includes a GB Ordnance Survey easting/northing grid reference and related identifiers.

## Where were the data collected?
- 20 discrete chalkstream catchments distributed along white chalk geology from Dorset (southwest) through Wiltshire to Hampshire (northeast) in southern England.

## When were the data collected?
- July 2012.

## How were the data collected?
- Stream site coordinates were processed with WINFAP-FEH 3 software to generate upstream catchment shapefiles at 50m2 resolution.
- Upstream catchment shapefiles were used to clip the Land Cover Map 2007 (LCM2007) layer, from which land cover areas were derived.
- Clipped data provided the areal coverage of each land cover class for each catchment.

## Why were the data collected?
- To aid site selection for surveying a gradient of catchment land cover intensification, from catchments dominated by calcareous grassland/woodland to those dominated by arable/improved grassland.

## Who was responsible for the collection and interpretation of data?
- Dr John Murphy (Queen Mary University of London) assisted by Dr Tom Oliver and Dr Jon Redhead (CEH) for generating catchment land cover data.

## Completeness and quality checks
- Data are complete.
- Visual verification of catchment shapefiles ensured error-free generation before clipping to LCM2007.
  
## Data structure: columns and definitions
- River and site identifiers and coordinates:
  - RIVER_ID: Unique river identifier in Britain
  - SITE_ID: Unique sampling location identifier
  - RIVER_NAME: River name
  - SITE_NAME: Site name
  - NGR: OS National Grid Reference
  - EASTING: OS Easting
  - NORTHING: OS Northing
- Land cover data (12 broad habitat classes, in km2):
  - Broadleaved_km2: Broadleaved, mixed and yew woodland
  - Coniferous_km2: Coniferous woodland
  - Arable_km2: Arable and horticulture
  - Impr_Grass_km2: Improved grassland
  - Acid_Grass_km2: Acid grassland
  - Neut_Grass_km2: Neutral grassland
  - Calc_Grass_km2: Calcareous grassland
  - Rough_Grass_km2: Rough low-productivity grassland
  - Heath_km2: Dwarf shrub heath
  - Built_Area_km2: Built-up areas and gardens
  - Rock_km2: Inland rock
  - Freshwater_km2: Freshwater
  - TOTAL_AREA_km2: Total area (sum of all land cover classes)
  
## References
- Morton, R.D.; Rowland, C.S.; Wood, C.M.; Meek, L.; Marston, C.G.; Smith, G.M. (2014). Land Cover Map 2007 (25m raster, GB) v1.2. NERC Environmental Information Data Centre. https://doi.org/10.5285/a1f88807-4826-44bc-994da902da5119c2
- Wallingford HydroSolutions (2012). WINFAP-FEH 3. http://www.hydrosolutions.co.uk/software-5-5.asp