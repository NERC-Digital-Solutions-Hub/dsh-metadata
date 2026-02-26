# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover map rasters for 2017-2020 are multiband rasters.
- 20m and 10m datasets: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
- 25m datasets: three bands (Band 1 = dominant Land Cover Class; Bands 2 and 3 = confidence indicators).
- This guide focuses on visualising the Land Cover Class data in band 1 using common GIS applications. For full data description, refer to the product documentation.

## Visualising in QGIS
- Add the file to your project; layer appears in the layers panel.
- Double-click the layer name to open properties.
- In Symbology, set Render type to Paletted/unique values.
- In Band, select Band 1.
- Click the style button and choose Load style from the menu.
- Browse to LCMcolours_QGIS.qml provided with this document, select it, and open.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Desktop
- In the Catalogue window, browse to the folder containing the data.
- Expand the file to display the raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open the layer properties.
- In Symbology, choose Unique Values (if prompted to calculate values, click YES).
- Click the import button and load the provided LCMcolours.lyr.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro
- Open the Catalogue window in your ArcGIS Pro project and browse to the data folder.
- Expand the file to display the raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Contents, open Symbology (Appearance > Symbology).
- In Primary Symbology, choose Unique values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and choose Import.
- Load the provided LCMcolours.lyr file.
- The map will be redrawn with the correct classification.