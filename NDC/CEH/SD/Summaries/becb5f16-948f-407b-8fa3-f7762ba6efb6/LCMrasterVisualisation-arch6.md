# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Quick guide to visualising Land Cover Map rasters (UKCEH Land Cover Class) in common GIS tools.
- Data structure: 20m and 10m rasters have two bands (Band 1 = class identifier; Band 2 = classification confidence). 25m rasters have three bands (Band 1 = dominant class; Bands 2-3 = confidence indicators).
- Focus of the guide is on visualising band 1 (the class) to produce a clear classification map.
- Supplementary style files accompany the instructions to ensure consistent colouring.

## Visualising with QGIS
- Add the data file to your project; the layer appears in the layers panel.
- Layer > properties > Symbology.
- Render type: Paletted/unique values; Band: Band 1.
- Click the style button > Load style from; select LCMcolours_QGIS.qml and open.
- OK; the map redraws with the correct classification colours.

## Visualising with ArcGIS Desktop
- In Catalog, navigate to the data folder; expand the raster to reveal bands.
- Drag band_1 into the Table of Contents.
- Layer properties > Symbology; choose Unique Values (if prompted to build an attribute table, click YES).
- Click Import and load LCMcolours.lyr provided with the instructions.
- OK; the map redraws with the correct classification colours.

## Visualising with ArcGIS Pro
- Open Catalog; navigate to the data folder and expand the raster bands.
- Drag band_1 into the Table of Contents.
- Layer properties > Appearance > Symbology; select Unique values.
- Use the hamburger menu in the Symbology panel and choose Import.
- Load LCMcolours.lyr; the map redraws with the correct classification colours.

## Additional notes
- The document is a concise how-to; for full data description, refer to the product documentation.
- Style files (LCMcolours_QGIS.qml and LCMcolours.lyr) are provided to ensure consistent visual classification across platforms.