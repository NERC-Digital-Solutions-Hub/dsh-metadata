# Visualising UKCEH Land Cover Class using a GIS application

- The Land cover map rasters for 2017-2020 are multiband rasters:
  - 20m and 10m datasets have two bands: Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
  - 25m datasets have three bands: Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence.
- This document is a short guide for visualising the data in common GIS applications, focusing on Band 1. For a full data description, refer to the product documentation.

## Visualising the data in QGIS

- Add the file to your project; the layer appears in the layers panel.
- Open layer properties, choose Symbology.
- In Render Type, select Paletted/Unique Values; choose Band 1.
- Click the style button, select Load style, and load LCMcolours_QGIS.qml provided with the document.
- Click OK to redraw the map with the correct classification.

## Visualising the data in ArcGIS Desktop

- In the Catalogue window, locate the data folder and expand the raster to view its bands.
- Drag Band 1 into the Table of Contents.
- Open the layer properties, go to Symbology, and choose Unique Values (if prompted to build an attribute table, click Yes).
- Click Import and load LCMcolours.lyr provided with these instructions.
- Click OK to redraw the map with the correct classification.

## Visualising the data in ArcGIS Pro

- In the Catalog, locate the data folder and expand the raster bands.
- Drag Band 1 into the Table of Contents.
- Open the layer’s properties (Appearance > Symbology) and choose Unique Values.
- Use the hamburger menu in the Symbology panel and select Import to load LCMcolours.lyr.
- The map will be redrawn with the correct classification.