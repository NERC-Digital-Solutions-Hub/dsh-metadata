# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- This is a short guide for visualising the UKCEH Land Cover Class data contained in band 1 of land cover rasters (2017-2020).
- Data structure: 
  - 20m and 10m rasters have two bands: Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
  - 25m rasters have three bands: Band 1 = dominant UKCEH Land Cover Class; Bands 2–3 = classification confidence.
- For full data description, refer to the product documentation.

## Data structure basics
- Band 1 always contains the land cover class identifier used for visualization.
- Bands 2 and 3 (where present) provide indicators of classification confidence.

## Visualisation steps by application

- QGIS
  - Add the file to your project; the layer appears in the layers panel.
  - Double-click the layer name in the layers panel to open Layer Properties.
  - In Symbology, set Render type to Paletted/unique values.
  - In Band, select Band 1.
  - Click the style button and choose Load style from the menu.
  - Browse to LCMcolours_QGIS.qml, select it, click Open, then OK.
  - The map will redraw with the correct classification.

- ArcGIS Desktop
  - In the Catalogue window, locate the data folder and expand the raster to display its bands.
  - Drag band_1 into the Table of Contents.
  - Double-click the layer name to open Layer Properties.
  - In the Symbology tab, choose Unique Values (if prompted to calculate values, click YES).
  - Click Import and load the provided layer file LCMcolours.lyr.
  - Click OK; the map will redraw with the correct classification.

- ArcGIS Pro
  - In the Catalog pane, browse to the data folder and expand the raster bands.
  - Drag band_1 into the Contents.
  - Double-click the layer name to open Layer Properties, then open Symbology (Appearance > Symbology).
  - In Primary Symbology, choose Unique values (if prompted to build an attribute table, click Yes).
  - Click the hamburger menu in the Symbology panel and choose Import.
  - Load the provided LCMcolours.lyr file; the map will redraw with the correct classification.

## Supporting assets
- LCMcolours_QGIS.qml (QGIS style file)
- LCMcolours.lyr (ArcGIS layer file)
- Both accompany these instructions.

## Practical notes
- Visualisation focuses on band 1 for classification; other bands serve as confidence indicators where available.
- For full data context and metadata, refer to the corresponding product documentation.

## Relevance to Data Support
- Provides end-users with a clear, repeatable workflow to visualise land cover classifications.
- Enables self-serve data exploration by delivering ready-made styles for common GIS platforms.
- Supports consistent data presentation across projects and teams.