# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover map rasters for 2017-2020 are multiband rasters.
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class ID; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant class; Bands 2–3 = classification confidence indicators).
- This short guide focuses on visualising Band 1; refer to the product documentation for full data description.

## Visualising the data using QGIS
- Add the file to your project; the layer appears in the layers panel.
- Double-click the layer name in the layers panel to open Layer Properties.
- In Symbology, set Render type to Paletted/Unique Values and Band to Band 1.
- Click the style button, choose Load style, and select LCMcolours_QGIS.qml; click Open, then OK.
- The map will redraw with the correct classification.

## Visualising the data using ArcGIS Desktop
- In the Catalog window, locate the folder containing the data and expand the raster to view its bands.
- Drag Band 1 (band_1) into the Table of Contents.
- Double-click the layer name to open Layer Properties. Go to the Symbology tab.
- Choose Unique Values (if prompted to calculate values, click YES).
- Click Import and load the file LCMcolours.lyr provided with these instructions.
- Click OK; the map will redraw with the correct classification.

## Visualising the data using ArcGIS Pro
- Open the Catalog, navigate to the folder with the data, and expand the raster’s bands.
- Drag Band 1 (band_1) into the Table of Contents.
- Double-click the layer to open Layer Properties; in Contents, select the layer and open Symbology (Appearance > Symbology).
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Click the hamburger menu in the Symbology panel and choose Import; load LCMcolours.lyr.
- The map will redraw with the correct classification.