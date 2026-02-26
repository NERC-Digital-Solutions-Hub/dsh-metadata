# Visualising UKCEH Land Cover Class using a GIS application

## Overview of the data
- Land cover map raster data products for 2021 are multiband rasters.
- 10m rasters have two bands: Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
- 25m rasters have three bands: Band 1 = dominant Land Cover Class; Bands 2-3 = classification confidence.
- This document is a short guide for visualising the Land Cover Class data contained in Band 1; refer to the product documentation for full data details.

## Visualising with QGIS
- Add the file to your project; it appears in the layers panel.
- Double-click the layer name in the layers panel to open Layer Properties.
- In Symbology, set Render type to Paletted/Unique values.
- In Band, select Band 1.
- Use the style button to Load style from the LCMcolours_QGIS.qml file that accompanies this document, then OK.
- The map will redraw with the correct classification.

## Visualising with ArcGIS Desktop
- In the Catalog window, locate the data folder and expand the raster to view its bands.
- Drag Band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Symbology, select Unique Values (if prompted to build an attribute table, click YES).
- Click Import and load the accompanying LCMcolours.lyr file.
- Click OK to redraw the map with the correct classification.

## Visualising with ArcGIS Pro
- In your ArcGIS Pro project, open the Catalog window and locate the data folder.
- Expand the raster to view its bands and drag Band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Contents, open Appearance > Symbology.
- Under Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Open the hamburger menu in the Symbology panel and choose Import.
- Load the accompanying LCMcolours.lyr file; the map will redraw with the correct classification.

## Additional notes
- The colour/style files (LCMcolours_QGIS.qml for QGIS and LCMcolours.lyr for ArcGIS Desktop/Pro) accompany these instructions.
- This guide focuses on visualising Band 1 data; refer to the full product documentation for complete data descriptions and context.