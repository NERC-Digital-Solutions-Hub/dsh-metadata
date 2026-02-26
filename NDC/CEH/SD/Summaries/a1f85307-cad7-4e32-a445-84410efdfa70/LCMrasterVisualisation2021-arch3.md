# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Short guide for visualising the Land Cover Class data contained in band 1 of UKCEH 2021 land cover raster products.
- Raster data specifics:
  - 10m rasters: two bands (Band 1 = Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant Land Cover Class identifier; Bands 2–3 = classification confidence).
- For full data description, refer to the product documentation.
- Output: consistent visual representation using pre-made style files.

## Data structure (bands)
- 10m rasters: Band 1 ( Land Cover Class ID ); Band 2 ( classification confidence ).
- 25m rasters: Band 1 ( dominant Land Cover Class ID ); Band 2 & 3 ( classification confidence ).

## Visualising in QGIS
- Add the file to your project; layer appears in the layers panel.
- Steps:
  - Double-click layer name in layers panel.
  - In Layer properties > Symbology: choose Paletted/unique values.
  - Band: Band 1.
  - Click style > Load style from the menu.
  - Browse to LCMcolours_QGIS.qml provided with this document, select it, Open.
  - Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Desktop
- In Catalog, locate the data folder and expand to view raster bands.
- Steps:
  - Drag band_1 into the Table of Contents.
  - Double-click layer name to open Layer properties > Symbology.
  - Choose Unique Values (if prompted to calculate values, click YES).
  - Click Import and load LCMcolours.lyr provided with these instructions.
  - Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro
- In ArcGIS Pro project, open Catalog and locate the data folder.
- Steps:
  - Expand to view raster bands and drag band_1 into the Table of Contents.
  - Double-click the layer name to open Layer properties; go to Appearance > Symbology.
  - In primary symbology, choose Unique values (if prompted to build an attribute table, click Yes).
  - Open the hamburger menu in the symbology panel and choose Import; load LCMcolours.lyr.
  - The map will be redrawn with the correct classification.

## Additional notes
- The LCMcolours_QGIS.qml and LCMcolours.lyr style files accompany these instructions.
- These steps facilitate consistent visualisation to support monitoring and communication of land cover classifications.