# Visualising UKCEH Land Cover Class using a GIS application

## Purpose and audience
- Short, practical guide to visualise UKCEH Land Cover Class data in common GIS applications.
- Intended for users who need to view and interpret land cover classifications, supporting monitoring and decision-making processes.

## Data structure (land cover rasters)
- 2017–2020 land cover rasters come in 20m, 10m, and 25m resolutions.
- Band composition:
  - 20m and 10m rasters: two bands
    - Band 1: UKCEH Land Cover Class identifier
    - Band 2: classification confidence indicator
  - 25m rasters: three bands
    - Band 1: dominant UKCEH Land Cover Class identifier
    - Bands 2 and 3: classification confidence indicators

## Getting started (files provided)
- The document provides platform-specific steps and requires accompanying style files:
  - QGIS: LCMcolours_QGIS.qml
  - ArcGIS (Desktop/Pro): LCMcolours.lyr
- Full data description and metadata are available in the product documentation.

## Visualising in QGIS
- Add the land cover file to your project (Layer added to the layers panel).
- Open Layer Properties > Symbology.
- Render type: Paletted/Unique Values; Band: Band 1.
- Click Style > Load style, select LCMcolours_QGIS.qml, open.
- OK to redraw the map with the correct classification.

## Visualising in ArcGIS Desktop
- In Catalog, locate the data folder and expand the raster to view its bands.
- Drag band_1 into the Table of Contents.
- Open Layer Properties > Symbology.
- Choose Unique Values; if prompted to build an attribute table, click Yes.
- Click Import and load LCMcolours.lyr.
- OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro
- Open Catalog in your ArcGIS Pro project; locate the data folder and view the raster bands.
- Drag band_1 into the Map/Contents.
- Open Layer Properties > Symbology.
- In Primary Symbology, select Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel > Import; load LCMcolours.lyr.
- The map will be redrawn with the correct classification.