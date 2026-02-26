# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover map rasters for 2017-2020 are multiband rasters.
- 20m and 10m datasets: two bands — Band 1 is the UKCEH Land Cover Class identifier; Band 2 indicates classification confidence.
- 25m datasets: three bands — Band 1 is the dominant UKCEH Land Cover Class; Bands 2 and 3 indicate classification confidence.
- This document is a short guide for visualising the Land Cover Class data contained in Band 1 using common GIS applications; refer to the product documentation for a full data description.

## How to visualise in QGIS
- Add the file to your project; the data appears in the layers panel.
- Double-click the layer name to open layer properties.
- In Symbology, choose Paletted/unique values.
- In the band option, select Band 1.
- Click the style button and choose Load style from the menu.
- Load the accompanying LCMcolours_QGIS.qml file, then OK.
- The map is redrawn with the correct classification.

## How to visualise in ArcGIS Desktop
- In the Catalog window, locate the data folder and expand to view the raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open layer properties.
- In Symbology, select Unique Values (if prompted to calculate values, click YES).
- Click Import and load the provided LCMcolours.lyr file.
- OK to redraw the map with the correct classification.

## How to visualise in ArcGIS Pro
- Open the Catalog, navigate to the data folder, and expand the raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open layer properties.
- In Contents, open Appearance > Symbology.
- Set Primary Symbology to Unique Values (if prompted, click Yes).
- Open the hamburger menu in the Symbology panel and choose Import.
- Load the LCMcolours.lyr file; the map will be redrawn with the correct classification.