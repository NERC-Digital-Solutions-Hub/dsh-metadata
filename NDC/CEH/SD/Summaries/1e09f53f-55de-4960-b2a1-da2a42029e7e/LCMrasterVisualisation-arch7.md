# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- The Land Cover Map rasters are multiband datasets:
  - 20m and 10m: two bands
    - Band 1 = UKCEH Land Cover Class identifier
    - Band 2 = classification confidence indicator
  - 25m: three bands
    - Band 1 = dominant UKCEH Land Cover Class identifier
    - Bands 2–3 = classification confidence indicators
- This document provides a short guide to visualising the Land Cover Class data contained in Band 1 using common GIS applications. A full data description is in the product documentation.

## Visualising in QGIS
- Add the file to your project; the layer appears in the layers panel.
- Steps:
  - Double-click the layer name in the layers panel to open Layer Properties.
  - In Symbology (left menu), set Render type to Paletted/Unique Values.
  - Select Band 1 in the Band box.
  - Click the style button and choose Load style from the menu.
  - Browse to LCMcolours_QGIS.qml (provided with these instructions), select it, and open.
  - Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Desktop
- In the Catalogue window, locate the data folder and expand the file to reveal raster bands.
- Steps:
  - Drag band_1 into the Table of Contents.
  - Double-click the layer name to open Layer Properties.
  - Symbology tab: choose Unique Values (if prompted to build an attribute table, click YES).
  - Click Import and load the provided LCMcolours.lyr file.
  - Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro
- In ArcGIS Pro, open the Catalog and locate the data folder.
- Steps:
  - Expand the file to show the raster bands.
  - Drag band_1 into the Table of Contents.
  - Double-click the layer name to open Layer Properties (Appearance > Symbology).
  - In primary symbology, choose Unique Values (and if prompted to build an attribute table, click Yes).
  - Open the hamburger menu in the Symbology panel and choose Import.
  - Load the provided LCMcolours.lyr file; the map will be redrawn with the correct classification.