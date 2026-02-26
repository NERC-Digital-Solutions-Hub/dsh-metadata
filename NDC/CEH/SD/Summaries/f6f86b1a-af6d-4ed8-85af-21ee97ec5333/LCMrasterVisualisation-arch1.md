# Visualising UKCEH Land Cover Class using a GIS application

- This document is a short guide for visualising the Land Cover Class data contained in band 1 of the UKCEH land cover rasters (2017–2020) using common GIS applications.
- Data characteristics:
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant Land Cover Class identifier; Bands 2–3 = classification confidence indicators).
- For a full data description, refer to the product documentation.

## Visualising the data using QGIS

- Add the file to your project; it will appear in the layers panel.
- Open layer properties, choose Symbology.
- In render type, select Paletted/Unique values; set Band to Band 1.
- Click the style button and choose Load style from the menu.
- Browse to LCMcolours_QGIS.qml, select it, and open.
- Click OK to redraw the map with the correct classification.

## Visualising the data using ArcGIS Desktop

- In the Catalogue window, locate the folder with the data and expand the file to show its bands.
- Drag Band_1 into the Table of Contents.
- Double-click the layer name to open the Layer Properties.
- In the Symbology tab, choose Unique Values (if prompted to calculate values, click YES).
- Click Import and load the provided layer file LCMcolours.lyr.
- Click OK to redraw the map with the correct classification.

## Visualising the data using ArcGIS Pro

- In the Project, open the Catalogue window and locate the data folder.
- Expand the file to view the raster bands; drag Band_1 into the Contents pane.
- Double-click the layer name to open Layer Properties, then select Appearance > Symbology.
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Open the hamburger menu in the Symbology panel and choose Import.
- Load the provided layer file LCMcolours.lyr.
- The map will be redrawn with the correct classification.