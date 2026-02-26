# Visualising UKCEH Land Cover Class using a GIS application

- Purpose: Short guide for visualising Land Cover Class data (band 1) within common GIS applications.
- Data structure:
  - Land cover map rasters for 2017-2020 are multiband.
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence).
- Scope: Focuses on visualising information contained in Band 1; refer to product documentation for full data description.

- Visualising in QGIS:
  - Add the file to the project; layer appears in Layers panel.
  - Layer properties > Symbology > render type: Paletted/unique values.
  - Band: Band 1.
  - Load style: LCMcolours_QGIS.qml accompanying the document; apply to redraw the map with correct classification.

- Visualising in ArcGIS Desktop:
  - In Catalog, locate the data folder; expand raster bands.
  - Drag Band 1 into Table of Contents.
  - Layer properties > Symbology > Unique Values (confirm value calculation if prompted).
  - Import the provided LCMcolours.lyr; apply to redraw the map with correct classification.

- Visualising in ArcGIS Pro:
  - Open Catalog; locate data folder and display raster bands.
  - Drag Band 1 into Table of Contents.
  - Layer properties > Appearance > Symbology > Unique values.
  - Use the hamburger menu in the Symbology panel > Import; load LCMcolours.lyr; map redraws with correct classification.

- Additional note:
  - The color/style files (LCMcolours_QGIS.qml and LCMcolours.lyr) accompany these instructions and ensure consistent visualization.
  - For a full data description, refer to the product documentation.