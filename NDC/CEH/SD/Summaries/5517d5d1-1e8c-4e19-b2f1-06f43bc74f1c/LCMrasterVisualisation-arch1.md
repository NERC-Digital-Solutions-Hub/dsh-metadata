# Visualising UKCEH Land Cover Class using a GIS application

- The Land cover map rasters for 2017-2020 come in different resolutions and band configurations:
  - 20m and 10m rasters: two bands
    - Band 1: UKCEH Land Cover Class identifier
    - Band 2: classification confidence indicator
  - 25m rasters: three bands
    - Band 1: dominant UKCEH Land Cover Class identifier
    - Bands 2 and 3: indicators of classification confidence
- This document is a short guide focused on visualising the data in Band 1 using common GIS applications. A full description of the data is available in the product documentation.
- The guidance includes ready-to-use color styles provided with the document:
  - QGIS: LCMcolours_QGIS.qml
  - ArcGIS: LCMcolours.lyr

- Visualising the data using QGIS
  - Add the file to your project; the layer appears in the layers panel
  - Double-click the layer name to open Layer Properties
  - In Symbology, set Render type to Paletted/Unique Values
  - Select Band 1
  - Click the style button, choose Load style, and load LCMcolours_QGIS.qml
  - Click OK to redraw the map with the correct classification

- Visualising the data using ArcGIS Desktop
  - In the Catalogue window, navigate to the data folder and expand the raster to reveal the bands
  - Drag band_1 into the Table of Contents
  - Double-click the layer name to open Layer Properties
  - In the Symbology tab, choose Unique Values
  - If prompted to calculate values, click YES
  - Click Import and load LCMcolours.lyr provided with these instructions
  - Click OK to redraw the map with the correct classification

- Visualising the data using ArcGIS Pro
  - In your ArcGIS Pro project, open the Catalog and browse to the data folder
  - Expand to display the raster bands and drag band_1 into the Table of Contents
  - Double-click the layer name to open Layer Properties
  - In the Contents window, select the layer and open Symbology (Appearance > Symbology)
  - In Primary Symbology, choose Unique Values (if prompted to build an attribute table, select Yes)
  - Use the hamburger menu in the Symbology panel and choose Import, then load LCMcolours.lyr
  - The map will be redrawn with the correct classification

- Additional notes
  - The accompanying style files are intended to standardise the visualisation of land cover classifications across applications. For the full data description, refer to the product documentation.