# Visualising UKCEH Land Cover Class using a GIS application

- Overview of data
  - Land cover rasters for 2017-2020, multi-band rasters
  - 20m and 10m datasets: two bands
    - Band 1 = UKCEH Land Cover Class identifier
    - Band 2 = classification confidence indicator
  - 25m datasets: three bands
    - Band 1 = dominant UKCEH Land Cover Class identifier
    - Bands 2 and 3 = classification confidence indicators
- Purpose
  - Short guide for using common GIS applications to visualise the Land Cover Class data in Band 1
  - For full data description, refer to the product documentation

- Visualising the data using QGIS
  - Add the file to your project; layer appears in the layers panel
  - Open layer properties, select Symbology
  - Render type: Paletted/unique values; Band: Band 1
  - Use Load style to import LCMcolours_QGIS.qml
  - Map is redrawn with the correct classification

- Visualising the data using ArcGIS Desktop
  - In Catalog, locate data folder; expand to view raster bands
  - Drag band_1 into the Table of Contents
  - Layer properties > Symbology > Unique Values
  - If prompted to calculate values, choose YES
  - Import the provided LCMcolours.lyr, OK
  - Map is redrawn with the correct classification

- Visualising the data using ArcGIS Pro
  - Open Catalog, browse to data folder, expand to view raster bands
  - Drag band_1 into the Table of Contents
  - Layer properties > Contents > Symbology
  - Primary: Unique values (build attribute table if prompted)
  - Use the hamburger menu in the Symbology panel > Import
  - Load LCMcolours.lyr; map is redrawn with the correct classification

- Additional notes
  - The colour styles are supplied as LCMcolours_QGIS.qml (for QGIS) and LCMcolours.lyr (for ArcGIS) with these instructions
  - This guide points users to self-serve visualization of the Land Cover Class data; refer to product documentation for full data details