# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover map rasters for 2017–2020; 20m and 10m rasters have two bands, 25m rasters have three bands.
- Band 1 in all cases is the UKCEH Land Cover Class identifier; the additional bands provide classification confidence indicators.
- This document is a short guide for visualising the data in Band 1 using common GIS applications; refer to the product documentation for a full data description.

## Data structure
- 20m and 10m datasets: Band 1 = class identifier; Band 2 = classification confidence.
- 25m datasets: Band 1 = dominant class identifier; Bands 2–3 = confidence indicators.

## Visualisation workflow by application

- QGIS
  - Add the file to your project; the layer appears in the layers panel.
  - Double-click the layer name to open Layer Properties.
  - In Symbology, choose Paletted/Unique values; set Band to 1.
  - Click Load style and select LCMcolours_QGIS.qml; OK to redraw the map with correct classification.

- ArcGIS Desktop
  - In Catalog, locate the data folder and expand the raster to reveal its bands.
  - Drag band_1 into the Table of Contents.
  - Double-click the layer, go to Symbology, and choose Unique Values.
  - Import the provided LCMcolours.lyr file; OK to redraw the map with correct classification.

- ArcGIS Pro
  - Open Catalog and locate the data folder; expand to view raster bands.
  - Drag band_1 into the Table of Contents.
  - Open Layer Properties and select Symbology (Appearance > Symbology).
  - Choose Unique Values; use the hamburger menu to Import and load LCMcolours.lyr.
  - The map will redraw with the correct classification.

## Additional notes
- The style files accompany these instructions: LCMcolours_QGIS.qml and LCMcolours.lyr.
- For a full data description, refer to the product documentation.