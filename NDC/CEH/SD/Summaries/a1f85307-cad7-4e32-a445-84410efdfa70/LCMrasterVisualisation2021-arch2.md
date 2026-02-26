# Visualising UKCEH Land Cover Class using a GIS application

- Overview of data
  - Land cover map raster data products for 2021:
    - 10m rasters: two bands
      - Band 1 = UKCEH Land Cover Class identifier
      - Band 2 = classification confidence indicator
    - 25m rasters: three bands
      - Band 1 = dominant UKCEH Land Cover Class identifier
      - Bands 2–3 = classification confidence indicators
  - This document is a short guide to visualising the Land Cover Class data contained in Band 1; refer to the product documentation for full data description.

- Visualising in QGIS
  - Add the file to your project; layer appears in the Layers panel.
  - Open Layer > Properties > Symbology
  - Render as Paletted/Unique Values; Band = Band 1
  - Click Style > Load Style, select LCMcolours_QGIS.qml accompanying this document, open
  - OK to redraw the map with correct classification

- Visualising in ArcGIS Desktop
  - In Catalog, locate the data folder and expand to view raster bands
  - Drag Band_1 into the Table of Contents
  - Layer Properties > Symbology
  - Choose Unique Values (if prompted to calculate values, click YES)
  - Import > load LCMcolours.lyr provided with these instructions
  - OK to redraw the map with correct classification

- Visualising in ArcGIS Pro
  - In the project, open Catalog and browse to the data folder
  - Expand the file to view raster bands; drag Band_1 into the Table of Contents
  - Layer Properties > Appearance > Symbology
  - Primary Symbology: Unique Values (if prompted to build an attribute table, click Yes)
  - Use the hamburger menu in Symbology > Import; load LCMcolours.lyr
  - Map will redraw with correct classification

- Additional notes
  - The color style files (LCMcolours_QGIS.qml and LCMcolours.lyr) accompany this document and ensure consistent classification visuals across platforms.