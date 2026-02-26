# Visualising UKCEH Land Cover Class using a GIS application

- The Land cover map rasters for 2017-2020 are multiband rasters.
  - 20m and 10m rasters: two bands. Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence indicator.
  - 25m rasters: three bands. Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = indicators of classification confidence.
- This document is a short guide for visualising the Land Cover Class data contained in band 1 using common GIS applications; refer to the product documentation for full data description.

- Visualising the data using QGIS
  - Add the file to your project; it will appear in the layers panel.
  - In Layer properties > Symbology: set Render type to Paletted/Unique Values; select Band 1.
  - Click the style button and choose Load style from the menu; load LCMcolours_QGIS.qml accompanying this document; map will redraw with correct classification.

- Visualising the data using ArcGIS Desktop
  - In Catalog, browse to the data folder; expand the raster to view bands.
  - Drag band_1 into the Table of Contents.
  - Layer properties > Symbology: choose Unique Values (if prompted to calculate values, click YES).
  - Click Import and load LCMcolours.lyr provided with these instructions; map will redraw with correct classification.

- Visualising the data using ArcGIS Pro
  - In the project, open Catalog; browse to the data folder.
  - Expand the file to show raster bands; drag band_1 into the Table of Contents.
  - Layer properties > Appearance > Symbology: set to Unique values (if prompted to build an attribute table, click Yes).
  - Use the hamburger menu in the Symbology panel > Import to load LCMcolours.lyr; map will redraw with correct classification.