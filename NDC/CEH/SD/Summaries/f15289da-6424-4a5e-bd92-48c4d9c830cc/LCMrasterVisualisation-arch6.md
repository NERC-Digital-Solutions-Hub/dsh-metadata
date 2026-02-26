# Visualising UKCEH Land Cover Class using a GIS application

## What the data is
- Land cover map rasters for 2017-2020 are multiband rasters.
- 20m and 10m rasters have two bands: Band 1 is the UKCEH Land Cover Class identifier; Band 2 indicates classification confidence.
- 25m datasets have three bands: Band 1 is the dominant UKCEH Land Cover Class identifier; Bands 2 and 3 indicate classification confidence.
- This document is a short guide for visualising the Land Cover Class data contained in Band 1 in common GIS applications. For a full data description, refer to the product documentation.

## Visualising in QGIS
- Add the file to your project; the layer appears in the layers panel.
- Open layer properties → Symbology → render as Paletted/Unique Values → Band 1.
- Click the style button → Load style from the menu → load LCMcolours_QGIS.qml that accompanies this document → OK.
- The map redraws with the correct classification.

## Visualising in ArcGIS Desktop
- In the Catalogue window, locate the data folder → expand to view raster bands; drag band_1 into the Table of Contents.
- Open layer properties → Symbology → Unique Values (if prompted to calculate values, click YES).
- Click Import → load LCMColours.lyr provided with these instructions → OK.
- The map redraws with the correct classification.

## Visualising in ArcGIS Pro
- Open the Catalogue window → browse to the data folder → expand to view raster bands → drag band_1 into the Table of Contents.
- Open layer properties → Contents → Appearance → Symbology → set to Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel → Import → load LCMcolours.lyr → map redraws with the correct classification.