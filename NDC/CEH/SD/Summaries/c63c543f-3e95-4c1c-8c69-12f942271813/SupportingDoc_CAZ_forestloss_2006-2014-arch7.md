# Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar.

## Overview
- GIS-focused dataset to assess deforestation and fire dynamics in the Ankeniheny-Zahemena Corridor (Madagascar).
- Combines multi-temporal Landsat imagery with a change dataset to detect and map forest clearance events.

## Data Generation Methods
- Imagery: Landsat 7 SLC-off imagery (15 m) compared to Landsat 2005 imagery and the Change in Natural Forest Cover (1990–2005).
- Sources and tiles: Imagery for tiles p158r73 (years 2006–2010) and p158r72 (years 2006, 2007, 2009, 2010); data acquired from USGS Glovis.
- Preprocessing:
  - Landsat 7: gap-free composites created with ENVI 4.7.
  - Landsat 8: preprocessed via Google Earth Engine.

## Attribute Table Definition
- Scene: Landsat imagery used; date followed by underscore (string).
- Baseline: Landsat imagery used for comparison (string).
- Year: Year of change (long integer; e.g., 2006 for 2005–2006 change).
- Area_ha: Area in hectares (double).
- X_utm: UTM Easting (long).
- Y_utm: UTM Northing (long).
- Zone: Delineation within protected area (string; values include priority for conservation, sustainable use, controlled settlements).
- Code: Unique identifier (long).

## Analytical Methods
- Observed clearance identified through visual interpretation and digitization using Esri software.
- Additional observation details recorded in the attribute table.
- Identification criteria were subjective, based on expert experience.
- Characteristics used to distinguish true clearings from natural phenology changes include shape, color, texture, and proximity to other clearings and settlements.
- Resulted in 5,954 polygons; about 75% of clearings were ≥1 ha; minimum recorded area ~5 pixels.

## Data Structure
- The dataset is a shapefile.
- Attribute table contains 8 relevant columns: scene, baseline, year, area_ha, x_utm, y_utm, zone, and code.

## Spatial Coverage and Dataset Notes
- Focused on the Ankeniheny-Zahemena Corridor region in Madagascar.
- Data presented as map-ready polygons for spatial analysis and visualization.

## Citation
- Tabor, K., K. Jones, J. Hewson, A. Rasolohery, A. Rambeloson, T. Andrianjohaninarivo, and C. Harvey (submitted Nov 2016 PlosOne). Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar.