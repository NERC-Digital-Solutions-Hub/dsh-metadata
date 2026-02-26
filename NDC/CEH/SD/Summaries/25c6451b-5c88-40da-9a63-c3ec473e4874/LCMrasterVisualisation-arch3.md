# Visualising UKCEH Land Cover Class using a GIS application

- Overview
  - Provides a short, practical guide to visualising UKCEH Land Cover Class data in common GIS applications.
  - Data: Land cover map rasters for 2017–2020, multi-band rasters with band configurations:
    - 20m and 10m: two bands (Band 1 = Land Cover Class identifier; Band 2 = classification confidence)
    - 25m: three bands (Band 1 = dominant Land Cover Class; Bands 2–3 = confidence indicators)
  - Purpose: Visualise the Band 1 classification data; full data description available in the product documentation.
  - Important for monitoring frameworks: standardises visual representation across platforms using provided style files.

- Visualising in QGIS
  - Add the file to your project; layer appears in the layers panel.
  - Open layer properties and choose Symbology.
  - Set render type to Paletted/Unique Values and select Band 1.
  - Load the style from LCMcolours_QGIS.qml accompanying the document.
  - Click OK to redraw the map with the correct classification.

- Visualising in ArcGIS Desktop
  - In the Catalogue window, navigate to the data folder and expand the raster.
  - Drag band_1 into the Table of Contents.
  - Open layer properties, go to Symbology, choose Unique Values (confirm value generation if prompted).
  - Click Import and load LCMcolours.lyr provided with the instructions.
  - Click OK to redraw the map with the correct classification.

- Visualising in ArcGIS Pro
  - Open the Catalog, browse to the data folder, expand the raster bands.
  - Drag band_1 into the Table of Contents.
  - Open layer properties (Contents > Symbology), set primary option to Unique Values (Yes to build attribute table if prompted).
  - Use the hamburger menu in the Symbology panel to Import and load LCMcolours.lyr.
  - The map will reflect the correct classification.

- Additional notes
  - The LCMcolours_QGIS.qml and LCMcolours.lyr files accompany these instructions to ensure consistent styling.
  - For a full data description, refer to the product documentation.
  - This workflow supports reproducible, governance-friendly visualization for environmental monitoring.