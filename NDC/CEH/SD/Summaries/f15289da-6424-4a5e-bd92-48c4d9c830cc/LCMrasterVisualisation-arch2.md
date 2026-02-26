# Visualising UKCEH Land Cover Class using a GIS application

- Overview
  - A short guide for visualising UKCEH Land Cover Class data in common GIS applications to support consistent representation of environmental conditions.
  - Uses land cover raster data (2017–2020) with multiple bands, including classification confidence indicators for quality assessment.
  - For full data description, refer to the product documentation.

- Data structure
  - 2017–2020 Land cover map rasters are multiband.
  - 20m and 10m rasters: two bands
    - Band 1: UKCEH Land Cover Class identifier
    - Band 2: classification confidence indicator
  - 25m rasters: three bands
    - Band 1: dominant UKCEH Land Cover Class identifier
    - Bands 2 and 3: indicators of classification confidence

- Visualising in QGIS
  - Add the raster file to the project; layer appears in the layers panel.
  - Layer properties > Symbology > Render type: Paletted/Unique Values; Band: Band 1.
  - Click Style > Load style from the accompanying LCMcolours_QGIS.qml file.
  - Click OK; map redraws with correct classification.

- Visualising in ArcGIS Desktop
  - In Catalogue, navigate to the data folder and expand the raster to show bands.
  - Drag Band 1 into the Table of Contents.
  - Layer Properties > Symbology > Unique Values (Yes to build attribute table if prompted).
  - Click Import and load LCMcolours.lyr supplied with the instructions.
  - Click OK; map redraws with correct classification.

- Visualising in ArcGIS Pro
  - In the Catalogue, navigate to the data folder and expand the raster bands.
  - Drag Band 1 into the Table of Contents.
  - Layer Properties > Appearance > Symbology; Primary symbology: Unique Values (Yes to build attribute table if prompted).
  - Open the hamburger menu in the Symbology panel > Import; load LCMcolours.lyr.
  - Map redraws with correct classification.

- Additional resources
  - The styling files accompany the instructions: LCMcolours_QGIS.qml and LCMcolours.lyr.
  - For a full data description, refer to the product documentation.

- Relevance for environmental monitoring
  - Enables consistent, standardised visualization of land cover classifications across major GIS platforms.
  - Facilitates clear communication of environmental conditions and supports monitoring and policy evaluation over time.