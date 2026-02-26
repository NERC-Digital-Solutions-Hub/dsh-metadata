# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover rasters for 2017-2020 are multi-band.
- 20m and 10m datasets: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
- 25m datasets: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2–3 = confidence indicators).
- This document provides a short guide to visualising the data in common GIS applications, focusing on band 1. For full data descriptions, refer to the product documentation.

## Visualising in QGIS
- Add the file to your project; layer appears in the layers panel.
- Open layer properties → Symbology.
- Render type: Paletted/unique values; Band: Band 1.
- Click Style → Load style from the menu.
- Load LCMcolours_QGIS.qml, then OK.
- The map is redrawn with the correct classification.

## Visualising in ArcGIS Desktop
- In the Catalogue, locate the data folder, expand the raster to show its bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties → Symbology.
- Choose Unique Values; if prompted to build values, click YES.
- Use Import to load the provided LCMcolours.lyr file.
- Click OK; the map is redrawn with the correct classification.

## Visualising in ArcGIS Pro
- Open the catalog, browse to the data folder and expand to view the raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties → Appearance > Symbology.
- Primary symbology: Unique values (Yes to build the attribute table if prompted).
- Click the hamburger menu in the symbology panel → Import, and load LCMcolours.lyr.
- The map is redrawn with the correct classification.