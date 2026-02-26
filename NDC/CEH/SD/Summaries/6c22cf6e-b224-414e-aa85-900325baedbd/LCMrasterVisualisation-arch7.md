# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover map rasters for 2017-2020 are multiband rasters.
- 20m and 10m datasets: two bands. Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence indicator.
- 25m datasets: three bands. Band 1 = dominant UKCEH Land Cover Class; Bands 2 and 3 = indicators of classification confidence.
- This document provides a short guide for visualising the Land Cover Class data (Band 1) in common GIS applications.
- For a full data description, refer to the product documentation.

## Visualising in QGIS
- Add the file to your project; the layer appears in the layers panel.
- Open layer properties and select Symbology.
- Render as Paletted/Unique Values; set Band to Band 1.
- Click the style button and choose Load style from the menu.
- Load the accompanying LCMcolours_QGIS.qml file and apply.
- The map will be redrawn with the correct classification.

## Visualising in ArcGIS Desktop
- In the Catalogue window, navigate to the data folder.
- Expand the raster and drag band_1 into the Table of Contents.
- Open the layer properties and go to the Symbology tab.
- Choose Unique Values (if prompted to build an attribute table, say Yes).
- Click Import and load the accompanying LCMcolours.lyr file.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro
- In a project, open the Catalog and browse to the data folder.
- Expand the file to display raster bands and drag band_1 into the Table of Contents.
- Open layer properties (Contents > Symbology).
- In Primary Symbology, choose Unique Values.
- Use the hamburger menu in the Symbology panel and select Import.
- Load the LCMcolours.lyr file provided with these instructions.
- The map will be redrawn with the correct classification.