# Visualising UKCEH Land Cover Class using a GIS application

- Overview
  - Land cover map rasters for 2017–2020 are multiband. 20m and 10m rasters have two bands (Band 1: UKCEH Land Cover Class identifier; Band 2: classification confidence). 25m rasters have three bands (Band 1: dominant class; Bands 2–3: confidence indicators).
  - This is a short guide for visualising the Land Cover Class data in common GIS applications, focusing on visualising Band 1. For full data descriptions, refer to the product documentation.

- Visualising in QGIS
  - Add the file to your project; layer appears in the layers panel.
  - Layer properties -> Symbology -> Paletted/unique values -> Band 1.
  - Click the style button -> Load style from the accompanying LCMcolours_QGIS.qml file.
  - Apply; the map redraws with the correct classification colors.

- Visualising in ArcGIS Desktop
  - In the Catalog window, locate the data, expand to show the raster’s bands.
  - Drag band_1 into the Table of Contents.
  - Layer properties -> Symbology -> Unique Values (if prompted to build values, click YES).
  - Click Import and load the accompanying LCMcolours.lyr file.
  - OK; the map redraws with the correct classification.

- Visualising in ArcGIS Pro
  - Open the Catalog, drag band_1 into the Table of Contents.
  - Layer properties -> Contents -> Symbology.
  - In primary symbology options, choose Unique values (if prompted to build an attribute table, click Yes).
  - Use the hamburger menu in the Symbology panel -> Import, and load LCMcolours.lyr.
  - The map redraws with the correct classification.

- Files accompanying this guide
  - LCMcolours_QGIS.qml for QGIS visualisation
  - LCMcolours.lyr for ArcGIS visualisation

- Practical note
  - The guide focuses on visualising Band 1; refer to the product documentation for detailed data descriptions and any version-specific steps.