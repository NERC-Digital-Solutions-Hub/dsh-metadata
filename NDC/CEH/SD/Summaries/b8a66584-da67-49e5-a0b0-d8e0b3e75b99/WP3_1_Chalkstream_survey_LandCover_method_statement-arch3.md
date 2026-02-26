# What has been recorded and what form does the data take?

## Overview
- A dataset describing land cover composition for 20 chalkstream catchments in southern England, recorded as areas (km2) per land cover class and linked to site coordinates.

## Data content
- 12 land cover classes by 20 stream sites, forming a matrix with the area of each land cover class in km2.
- Each stream site has a GB Ordnance Survey grid reference (NGR, Easting, Northing) for spatial定位.
- Land cover classes include broad habitat categories such as Broadleaved and Coniferous woodland, Arable, Various Grasslands (improved, neutral, calcareous, rough), Heath, Built areas, Rock, Freshwater, and a TOTAL_AREA.

## Spatial and temporal coverage
- Locations: 20 chalkstream catchments distributed along white chalk geology from Dorset (southwest) to Hampshire (northeast).
- Time of data collection: July 2012.

## Data collection and processing
- Upstream catchment shapefiles generated with WINFAP-FEH 3 software to produce catchment boundaries at the catchment scale.
- Catchment shapefiles used to clip the Land Cover Map 2007 (LCM2007) layer to derive land cover area per class for each catchment.
- Purpose: to aid site selection across a gradient of catchment land cover intensification, from calcareous grassland/woodland dominance to arable/improved grasslands.
- Responsible personnel: Dr John Murphy (Queen Mary University of London) assisted by Dr Tom Oliver and Dr Jon Redhead (CEH).

## Data completeness and validation
- Completeness: The dataset is reported as complete.
- Quality checks: Visual verification of catchment shapefiles before clipping LCM2007 to ensure error-free generation.

## Dataset schema (key fields)
- RIVER_ID: Unique identifier for each river in Britain.
- SITE_ID: Unique identifier for each sampling location along each river.
- RIVER_NAME, SITE_NAME: Names from official maps.
- NGR, EASTING, NORTHING: Spatial coordinates (Ordnance Survey references).
- LCM2007 Broad Habitat Name: Broad habitat category name.
- Units: km2 for each land cover class.
- Land cover class areas (examples): Broadleaved_km2, Coniferous_km2, Arable_km2, Impr_Grass_km2, Acid_Grass_km2, Neut_Grass_km2, Calc_Grass_km2, Rough_Grass_km2, Heath_km2, Built_Area_km2, Rock_km2, Freshwater_km2, TOTAL_AREA_km2.
- Notes: Data derived from clipping LCM2007 (25 m raster, v1.2) to upstream catchment boundaries; 12 land cover classes used.

## Data sources and references
- Land Cover Map 2007 (25m raster, GB) v1.2. Morton, R.D.; Rowland, C.S.; Wood, C.M.; Meek, L.; Marston, C.G.; Smith, G.M. (2014). NERC Environmental Information Data Centre. DOI: 10.5285/a1f88807-4826-44bc-994da902da5119c2
- WINFAP-FEH 3 software. Wallingford HydroSolutions (2012). http://www.hydrosolutions.co.uk/software-5-5.asp

## Use and purpose
- Enables selection of survey sites across a gradient of catchment land cover intensification, facilitating environmental health assessments and policy-relevant monitoring across land-use scenarios.

## Data governance and access considerations
- Data are derived from public datasets (LCM2007) and publicly documented software (WINFAP-FEH 3); underlying spatial data and methods are described for reproducibility.
- While the document confirms completeness and QA steps, it does not detail data access restrictions or governance policies beyond methodological transparency.