# Visualising UKCEH Land Cover Class using a GIS application

- The Land cover map rasters for 2017-2020 are multi-band rasters.
  - 20m and 10m rasters: two bands. Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
  - 25m rasters: three bands. Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence.
- Purpose of this document: a short guide for visualising the Land Cover Class data contained in Band 1 using common GIS applications. For a full description of the data, refer to the product documentation.

- What this guide helps you do
  - Visualise Band 1 classifications consistently across GIS platforms.
  - Apply a predefined colour scheme to the classifications via accompanying style files.
  - Produce maps that reflect the correct Land Cover Class mapping.

- Visualising the data by GIS platform

  - QGIS
    - Add the file to your project; the layer appears in the layers panel.
    - Open Layer properties > Symbology.
    - Render as Paletted/Unique values; Band = Band 1.
    - Click the style button > Load style from LCMcolours_QGIS.qml (provided with the document).
    - Open, and the map is redrawn with the correct classification.

  - ArcGIS Desktop
    - In the Catalogue window, locate the data folder, expand the raster bands, and drag band_1 into the Table of Contents.
    - Double-click the layer name to open Layer Properties > Symbology.
    - Choose Unique Values; if prompted to build the attribute table, click Yes.
    - Click Import and load LCMcolours.lyr (provided with the instructions).
    - Click OK to redraw the map with the correct classification.

  - ArcGIS Pro
    - In the project, open Catalog and locate the data folder.
    - Expand the raster bands and drag band_1 into the Contents window.
    - Open Layer Properties > Appearance > Symbology; choose Unique Values.
    - Use the hamburger menu in the Symbology panel > Import; load LCMcolours.lyr.
    - The map will be redrawn with the correct classification.

- Notes
  - The colour mappings are provided via LCMcolours_QGIS.qml (for QGIS) and LCMcolours.lyr (for ArcGIS) accompanying these instructions.
  - This guide focuses on visualising Band 1; refer to the product documentation for detailed data descriptions and metadata.