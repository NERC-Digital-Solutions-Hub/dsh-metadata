# Visualising UKCEH Land Cover Class using a GIS application

- This guide explains how to visualize the Land Cover Class data contained in band 1 of UKCEH Land Cover Map rasters.
- Data structure:
  - 20m and 10m rasters: two bands
    - Band 1 = UKCEH Land Cover Class identifier
    - Band 2 = classification confidence indicator
  - 25m rasters: three bands
    - Band 1 = dominant UKCEH Land Cover Class identifier
    - Bands 2 and 3 = classification confidence indicators
- Purpose: Use common GIS applications to display the Land Cover Class in band 1 and apply the correct classification colours.

## Visualising in QGIS

- Add the file to your project; it appears in the layers panel.
- Double-click the layer name in the layers panel.
- In Layer Properties, select Symbology.
- In Render type, choose Paletted/unique values.
- In Band, select Band 1.
- Click the style button and choose Load style from the menu.
- Browse to LCMcolours_QGIS.qml provided with this document, select it, and click open.
- Click OK; the map will be redrawn with the correct classification.

## Visualising in ArcGIS Desktop

- In the Catalogue window, browse to the data folder.
- Expand the file to display the raster’s bands; drag band_1 into the Table of Contents.
- Double-click the layer name in the Table of Contents to open Layer Properties.
- In Symbology, choose Unique Values.
- If prompted to build an attribute table, click YES.
- Click Import and load the provided layer file (LCMcolours.lyr).
- Click OK; the map will be redrawn with the correct classification.

## Visualising in ArcGIS Pro

- In the Catalog window, browse to the data folder.
- Expand the file to display the raster’s bands and drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Contents, open Appearance > Symbology.
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Open the hamburger menu in the Symbology panel and choose Import.
- Load the provided layer file (LCMcolours.lyr).
- The map will be redrawn with the correct classification.