# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover map raster data products for 2021 are multiband rasters.
- 10m rasters: two bands; Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
- 25m rasters: three bands; Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2–3 = classification confidence.
- This short guide focuses on visualising data contained in Band 1; refer to the product documentation for full data descriptions.

## General approach to visualization
- Add the file to your GIS project; the layer appears in the layers panel.
- Open layer properties and set the symbology to render correctly using Band 1.
- Load the accompanying color/style file to ensure correct classification colors.
- The map will redraw with the correct classification.

## Software-specific instructions

### QGIS
- Add file to project; select the layer.
- Layer Properties → Symbology → Render type: Paletted/unique values → Band: Band 1.
- Click Style → Load style from, browse to LCMcolours_QGIS.qml → Open → OK.
- Map redraws with correct classification.

### ArcGIS Desktop
- In Catalog, browse to data folder; expand the raster to view its bands.
- Drag band_1 into the Table of Contents.
- Layer Properties → Symbology → Unique Values (if prompted to calculate values, click YES).
- Click Import and load the accompanying file LCMcolours.lyr.
- OK → map redraws with correct classification.

### ArcGIS Pro
- Open project; Catalog → browse to data folder; expand to view raster bands.
- Drag band_1 into the Table of Contents.
- Layer properties → Symbology (Appearance) → Primary symbology: Unique values (Yes to build attribute table if prompted).
- Use the hamburger menu in the Symbology panel → Import → load LCMcolours.lyr.
- Map redraws with correct classification.

## Additional notes
- For a full description of the data, refer to the product documentation.
- The color/style files (LCMcolours_QGIS.qml, LCMcolours.lyr) accompany this guide to ensure consistent visualization.