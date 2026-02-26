# Visualising UKCEH Land Cover Class using a GIS application

- Overview
  - Land cover map rasters for 2017-2020 are multiband rasters with:
    - 20m and 10m datasets: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence)
    - 25m datasets: three bands (Band 1 = dominant Land Cover Class identifier; Bands 2 and 3 = classification confidence)
  - Purpose: a short guide for visualising the Land Cover Class data contained in Band 1 using common GIS applications; refer to product documentation for full data description
  - Additional notes: uses predefined style files to ensure correct classification colours (LCMcolours files)

- Visualising in QGIS
  - Add the file to your project; layer appears in the layers panel
  - Open layer properties, select Symbology
  - Set Render type to Paletted/Unique Values, Band to Band 1
  - Click Style > Load style, browse to LCMcolours_QGIS.qml, open
  - OK to redraw map with correct classification

- Visualising in ArcGIS Desktop
  - In Catalog, locate the data folder and expand the raster to view bands
  - Drag band_1 into the Table of Contents
  - Open layer properties, go to Symbology
  - Choose Unique Values, import LCMcolours.lyr, OK
  - Map redraws with correct classification

- Visualising in ArcGIS Pro
  - Open Catalog, browse to data folder and expand raster bands
  - Drag band_1 into the Contents
  - Open layer properties (Appearance > Symbology)
  - Set Primary Symbology to Unique Values (Yes to build attribute table if prompted)
  - Use the Import option in the symbology panel to load LCMcolours.lyr
  - Map redraws with correct classification

- Additional context
  - For a full description of the data, refer to the product documentation
  - The LCMcolours style files accompany these instructions to ensure consistent visual representation