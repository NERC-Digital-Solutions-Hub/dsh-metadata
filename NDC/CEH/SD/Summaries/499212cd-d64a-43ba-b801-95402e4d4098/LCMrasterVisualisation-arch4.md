# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- This document provides a concise guide to visualising UKCEH Land Cover Class data using common GIS applications.
- Focus is on visualising the Land Cover Class information contained in band 1 of the multiband rasters from 2017-2020.
- Data at different resolutions have different band structures:
  - 20m and 10m rasters: two bands (Band 1 = Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant Land Cover Class identifier; Bands 2 and 3 = classification confidence).
- For full data description, refer to the product documentation.
- Use the accompanying style files (LCMcolours_QGIS.qml and LCMcolours.lyr) to ensure correct classification colors.

## Data structure (bands)
- 20m and 10m rasters
  - Band 1: UKCEH Land Cover Class identifier
  - Band 2: classification confidence indicator
- 25m rasters
  - Band 1: dominant UKCEH Land Cover Class identifier
  - Band 2 and Band 3: classification confidence indicators

## Visualising in QGIS
- Add the land cover file to your project; the layer appears in the layers panel.
- Open layer properties → Symbology → render type: Paletted/Unique values → Band: Band 1.
- Click the style button → Load style from the LCMcolours_QGIS.qml file accompanying this document.
- Confirm to redraw the map with correct classification.

## Visualising in ArcGIS Desktop
- In the Catalogue, navigate to the data folder and expand the raster to expose Band 1.
- Drag Band 1 into the Table of Contents.
- Layer properties → Symbology → Unique Values (if prompted to build an attribute table, click Yes).
- Use Import to load LCMcolours.lyr provided with these instructions.
- Click OK to redraw the map with correct classification.

## Visualising in ArcGIS Pro
- Open the Catalog, navigate to the data folder, and expand the raster bands.
- Drag Band 1 into the Table of Contents.
- Layer properties → Appearance → Symbology → Primary: Unique Values (or as prompted).
- Use the hamburger menu in the Symbology panel → Import to load LCMcolours.lyr.
- The map will redraw with the correct classification.