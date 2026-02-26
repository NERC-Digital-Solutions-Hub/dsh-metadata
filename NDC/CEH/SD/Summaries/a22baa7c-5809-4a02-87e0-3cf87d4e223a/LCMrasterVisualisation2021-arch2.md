# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover map raster data products for 2021 are multiband rasters.
- 10m rasters have two bands:
  - Band 1: UKCEH Land Cover Class identifier
  - Band 2: classification confidence indicator
- 25m rasters have three bands:
  - Band 1: dominant UKCEH Land Cover Class identifier
  - Bands 2 and 3: classification confidence indicators
- This document provides a short guide for visualising the Land Cover Class data contained in band 1, with full data description available in the product documentation.

## Visualising in QGIS
- Add the file to your project; the layer appears in the layers panel.
- Double-click the layer name in the layers panel to open Layer Properties.
- In Symbology, set Render type to Paletted/Unique Values.
- In Band, select Band 1.
- Click the Style button and choose Load style from the menu.
- Browse to the LCMcolours_QGIS.qml file accompanying this document, select it, and click Open.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Desktop
- In the Catalog window, navigate to the folder containing the data.
- Expand the file to display the raster's bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Symbology, choose Unique Values (if prompted to calculate values, click YES).
- Click the Import button and load the provided layer file (LCMcolours.lyr).
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro
- In the Catalog window, browse to the folder containing the data and expand to display the raster's bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In the Contents window, open Symbology (Appearance > Symbology).
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Click the hamburger menu in the Symbology panel and choose Import.
- Load the provided layer file (LCMcolours.lyr).
- The map will be redrawn with the correct classification.