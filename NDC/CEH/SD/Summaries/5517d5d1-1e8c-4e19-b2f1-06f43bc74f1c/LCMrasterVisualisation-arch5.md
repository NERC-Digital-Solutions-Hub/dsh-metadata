# Visualising UKCEH Land Cover Class using a GIS application

- The Land cover map rasters for 2017-2020 are multiband rasters:
  - 20m and 10m rasters: two bands
    - Band 1: UKCEH Land Cover Class identifier
    - Band 2: classification confidence indicator
  - 25m rasters: three bands
    - Band 1: dominant UKCEH Land Cover Class identifier
    - Bands 2 and 3: indicators of classification confidence
- This document is a short guide for visualising the Land Cover Class data using common GIS applications; refer to the full product documentation for complete data descriptions.

- Purpose for Data Stewards:
  - Supports consistent visualization of land cover data to improve discoverability and usability.
  - Uses provided style files to ensure standardized color mappings across tools.
  - Guides users to focus on Band 1 for classification display.

- Governance considerations:
  - Data versioning and metadata alignment (Band1 as the primary class identifier; confidence bands kept for context).
  - Ensure correct application of styling files to maintain consistency with catalogued datasets.

Visualization steps by GIS tool

- Visualising the data using QGIS
  - Add the file to your project; layer appears in the layers panel.
  - Double-click the layer name to open Layer Properties.
  - Select Symbology.
  - In Render type, choose Paletted/Unique Values.
  - In Band, select Band 1.
  - Click Style > Load Style from the menu.
  - Browse to LCMcolours_QGIS.qml, select it, and open.
  - Click OK to redraw the map with the correct classification.

- Visualising the data using ArcGIS Desktop
  - In Catalog, locate the data folder and expand the raster to view its bands.
  - Drag Band_1 into the Table of Contents.
  - Double-click the layer name to open Layer Properties.
  - In Symbology, choose Unique Values (if prompted to calculate values, select YES).
  - Click Import and load LCMcolours.lyr (provided with these instructions).
  - Click OK to redraw the map with the correct classification.

- Visualising the data using ArcGIS Pro
  - Open the Catalog and navigate to the data folder.
  - Expand the raster to display its bands.
  - Drag Band_1 into the Table of Contents.
  - Double-click the layer name to open Layer Properties.
  - In Contents, open Appearance > Symbology.
  - Select Unique Values (and if prompted, build an attribute table: Yes).
  - Click the hamburger menu in the Symbology panel and choose Import.
  - Load LCMcolours.lyr (provided with these instructions).
  - The map will be redrawn with the correct classification.