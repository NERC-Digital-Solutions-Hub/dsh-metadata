# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover map raster data for 2021 are multiband rasters: 10m rasters have two bands; 25m rasters have three bands.
  - 10m: Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
  - 25m: Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence.
- This document is a short guide for visualising Band 1 in common GIS applications; refer to the product documentation for full data description.

## Visualisation steps by platform

### QGIS
- Add the file to your project; layer appears in the layers panel.
- Double-click the layer name → Layer properties → Symbology.
- Render type: Paletted/Unique Values; Band: Band 1.
- Click Style → Load style from the menu → select LCMcolours_QGIS.qml → OK.
- The map will redraw with the correct classification.

### ArcGIS Desktop
- In Catalog, locate the data folder and expand the raster to show its bands.
- Drag Band 1 (band_1) into the Table of Contents.
- Double-click the layer → Layer properties → Symbology tab.
- Choose Unique Values; (if prompted to build an attribute table, click Yes).
- Click Import and load LCMcolours.lyr provided with the instructions.
- OK → map redraws with the correct classification.

### ArcGIS Pro
- Open Catalog, browse to the data folder, expand the raster bands.
- Drag Band 1 (band_1) into the Table of Contents.
- Double-click the layer → layer properties; Contents → Appearance > Symbology.
- Primary symbology: Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the symbology panel → Import → load LCMcolours.lyr.
- The map will redraw with the correct classification.

## Key notes
- The colour mappings are standardized via accompanying style files (LCMcolours_QGIS.qml or LCMcolours.lyr) to ensure consistent visualization across platforms.
- This guide focuses on visualising Band 1 (class identifiers); Band 2 (and Band 3 for 25m) provide classification confidence but are not required for the basic visualization described here.
- For a full data description, consult the product documentation.