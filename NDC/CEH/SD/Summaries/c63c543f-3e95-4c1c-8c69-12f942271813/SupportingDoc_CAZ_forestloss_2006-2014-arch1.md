# Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar

## Data Generation Overview
- Comparisons among Landsat 7 SLC-off imagery (15 m resolution) with Landsat 2005 imagery and the Change in Natural Forest Cover (1990–2005) developed by USAID, Conservation International, and Madagascar’s Ministry of Environment, Water, Forests and Tourism.
- Imagery sources and years:
  - p158r73: 2006, 2007, 2008, 2009, 2010
  - p158r72: 2006, 2007, 2009, 2010
- Data acquisition and processing:
  - imagery obtained from USGS Global Visualization Viewer (Glovis)
  - Landsat 7 gap-free composites created with ENVI 4.7
  - Landsat 8 imagery preprocessed via Google Earth Engine

## Attribute Table Definition
- Scene: Landsat imagery used; value format “date_followed_by_underscore”
- Baseline: Landsat imagery used for comparison
- Year: Year of change (e.g., 2006 = 2005–2006 change)
- Area_ha: Area in hectares
- X_utm: UTM Easting
- Y_utm: UTM Northing
- Zone: Delineation within protected area; zones include priority for conservation, sustainable use, and controlled settlements
- Code: Unique identifier

## Analytical Methods
- Observed clearance areas identified via visual interpretation and manually digitized using Esri software
- Additional observation metadata recorded in the attribute table
- Identification criteria were subjective, based on expert experience; distinguishing true clearings from phenological changes using shape, color, texture, and proximity to settlements
- Resulted in 5,954 polygons
- Clearings ≥1 ha comprised ~75% of observations; minimum mapped area ~5 pixels

## Data Structure
- Format: Shapefile
- Attribute table contains eight columns: scene, baseline, year, area_ha, x_utm, y_utm, zone, and code

## Dataset Context and Citation
- Geographic focus: Ankeniheny-Zahemena Corridor, Madagascar
- Citation: Tabor, K., K. Jones, J. Hewson, A. Rasolohery, A. Rambeloson, T. Andrianjohaninarivo, and C. Harvey (submitted Nov 2016). Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar.