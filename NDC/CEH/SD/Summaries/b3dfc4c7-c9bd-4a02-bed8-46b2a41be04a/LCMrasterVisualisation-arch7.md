# Visualising UKCEH Land Cover Class using a GIS application

- This document provides a short guide for visualising the Land Cover Class data (band 1) from UKCEH rasters (2017–2020) in common GIS applications.
- Data structure:
  - 20m and 10m rasters: two bands
    - Band 1: UKCEH Land Cover Class identifier
    - Band 2: classification confidence indicator
  - 25m rasters: three bands
    - Band 1: dominant UKCEH Land Cover Class identifier
    - Bands 2–3: classification confidence indicators
- For a full data description, refer to the product documentation.

## Using QGIS

- Add the file to your project; the layer appears in the layers panel.
- Open the layer properties and choose Symbology.
- Set Render type to Paletted/unique values.
- Set Band to Band 1.
- Click the style button, choose Load style from the menu.
- Browse to LCMcolours_QGIS.qml, select it, and click open.
- Click OK to redraw the map with the correct classification.

## Using ArcGIS Desktop

- In the Catalogue window, locate the data folder and expand the raster to display its bands.
- Drag band_1 into the Table of Contents.
- Open the layer properties and go to Symbology.
- Choose Unique Values (if prompted to calculate values, click YES).
- Click Import and load the accompanying layer file LCMcolours.lyr.
- Click OK to redraw the map with the correct classification.

## Using ArcGIS Pro

- In your project, open the Catalogue and locate the data folder.
- Expand the raster to display its bands and drag band_1 into the Table of Contents.
- Open the layer properties (Appearance > Symbology).
- In the primary symbology options, choose Unique values (if prompted to build an attribute table, click Yes).
- Click the hamburger menu in the symbology panel and choose Import.
- Load LCMcolours.lyr and the map will be redrawn with the correct classification.