# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover map rasters for 2017-2020 are multiband rasters.
  - 20 m and 10 m datasets: two bands. Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence indicator.
  - 25 m datasets: three bands. Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence indicators.
- Purpose: guide for visualising the Land Cover Class data contained in Band 1 using common GIS applications.
- Full data description available in product documentation.

## Visualising in QGIS
- Add the file to your project; layer will appear in the layers panel.
- Double-click the layer name to open Layer Properties.
- In Symbology, set render type to Paletted/Unique Values.
- Select Band 1.
- Click the style button, choose Load style, and load LCMcolours_QGIS.qml.
- Click OK to redraw the map with correct classification.

## Visualising in ArcGIS Desktop
- In the Catalogue window, browse to the data folder and expand the raster to view its bands.
- Drag Band 1 (band_1) into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Symbology, choose Unique Values (if prompted to calculate values, click YES).
- Click Import and load LCMcolours.lyr provided with these instructions.
- Click OK to redraw the map with correct classification.

## Visualising in ArcGIS Pro
- Open the Catalog window and browse to the data folder.
- Expand the file to display the raster bands, then drag Band 1 into the Table of Contents.
- Double-click the layer to open Layer Properties.
- In Contents, open Appearance > Symbology.
- Set Primary Symbology to Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and choose Import.
- Load LCMcolours.lyr to redraw the map with correct classification.