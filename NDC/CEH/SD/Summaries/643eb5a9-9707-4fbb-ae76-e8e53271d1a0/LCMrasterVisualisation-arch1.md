# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- This document provides a short guide for visualising the Land Cover Class (LCC) data contained in band 1 of UKCEH land cover rasters (2017–2020) using common GIS applications.
- Data characteristics:
  - 20 m and 10 m rasters: two bands (Band 1 = LCC identifier, Band 2 = classification confidence).
  - 25 m rasters: three bands (Band 1 = dominant LCC identifier, Bands 2–3 = classification confidence).
- For a full data description, refer to the product documentation.

## Data structure and bands
- Band 1: UKCEH Land Cover Class identifier (dominant value for the pixel).
- Band 2 (and 3 on 25 m rasters): indicators of classification confidence.

## Visualising in QGIS
- Add the file to your project; the layer appears in the layers panel.
- Open layer properties (double-click the layer name).
- Go to Symbology.
- Render as Paletted/Unique Values.
- In Band, select Band 1.
- Click the style button, choose Load style from the menu.
- Load the LCMcolours_QGIS.qml file accompanying this document, then OK.
- The map redraws with the correct classification. 

## Visualising in ArcGIS Desktop
- In the Catalogue window, navigate to the data folder and expand the raster to display its bands.
- Drag Band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Symbology, choose Unique Values.
- If prompted to calculate values, click YES.
- Click Import and load the provided LCMcolours.lyr.
- Click OK; the map redraws with the correct classification.

## Visualising in ArcGIS Pro
- Open the Catalog and browse to the data folder.
- Expand to display the raster’s bands; drag Band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Contents, select the layer and open Symbology (Appearance > Symbology).
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and choose Import.
- Load the LCMcolours.lyr file provided with these instructions.
- The map will be redrawn with the correct classification.