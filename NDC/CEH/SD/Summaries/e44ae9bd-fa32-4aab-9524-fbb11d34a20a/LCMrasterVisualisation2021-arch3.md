# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover raster data for 2021: 10m rasters have two bands (Band 1: UKCEH Land Cover Class identifier; Band 2: classification confidence). 25m rasters have three bands (Band 1: dominant class; Bands 2–3: confidence indicators).
- This document is a short guide for visualising the Land Cover Class data contained in Band 1 using common GIS applications.
- For full data description, refer to the product documentation.

## Visualising with QGIS
- Add the file to your project; the layer appears in the layers panel.
- Open layer properties > Symbology.
- Render type: Paletted/unique values; Band: Band 1.
- Click style > Load style from the menu; select LCMcolours_QGIS.qml and open.
- Click OK to redraw the map with the correct classifications.

## Visualising with ArcGIS Desktop
- In the Catalogue window, locate the data folder and expand to display the raster bands.
- Drag band_1 into the Table of Contents.
- Open layer properties > Symbology; choose Unique Values (confirm YES if prompted to build values).
- Click Import and load the provided LCMcolours.lyr.
- Click OK to redraw the map with the correct classification.

## Visualising with ArcGIS Pro
- In the Catalog, browse to the data folder and expand to reveal the raster bands.
- Drag band_1 into the Table of Contents.
- Open layer properties > Symbology (Appearance > Symbology); choose Unique values.
- Use the hamburger menu in the Symbology panel > Import and load LCMcolours.lyr.
- The map will be redrawn with the correct classification.