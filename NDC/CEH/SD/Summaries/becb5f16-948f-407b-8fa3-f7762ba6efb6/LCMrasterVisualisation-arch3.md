# Visualising UKCEH Land Cover Class using a GIS application

- The Land Cover Map rasters come in different resolutions and band configurations:
  - 20m and 10m rasters: two bands per raster
    - Band 1: UKCEH Land Cover Class identifier
    - Band 2: classification confidence indicator
  - 25m rasters: three bands
    - Band 1: dominant UKCEH Land Cover Class identifier
    - Bands 2 and 3: classification confidence indicators
- This document is a short guide for visualising the Land Cover Class data contained in band 1 using common GIS applications; for full data description, refer to the product documentation.

- Visualising the data using QGIS
  - Add the file to your project; the layer appears in the layers panel.
  - Open layer properties > Symbology
  - Render type: Paletted/unique values
  - Band: Band 1
  - Load style from the accompanying LCMcolours_QGIS.qml file
  - Click OK to redraw the map with the correct classification.

- Visualising the data using ArcGIS Desktop
  - In Catalog, locate the data folder and expand the raster to show its bands.
  - Drag band_1 into the Table of Contents.
  - Open layer properties > Symbology
  - Set Symbology type to Unique Values (if prompted to build an attribute table, click YES)
  - Click Import and load LCMcolours.lyr provided with these instructions
  - Click OK to redraw the map with the correct classification.

- Visualising the data using ArcGIS Pro
  - Open Catalog and locate the data folder
  - Expand the raster to show the bands and drag band_1 into the Contents window
  - Open layer properties > Appearance > Symbology
  - Primary symbology: Unique values
  - Use the hamburger menu in the Symbology panel > Import
  - Load LCMcolours.lyr and the map will be redrawn with the correct classification.