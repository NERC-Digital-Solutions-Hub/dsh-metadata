# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Short guide for visualising Land Cover Class data in common GIS applications.
- Data bands:
  - 20m and 10m rasters: two bands (Band 1 = Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant Land Cover Class; Bands 2–3 = classification confidence).
- Focuses on visualising band 1; refer to product documentation for full data descriptions.
- Uses accompanying style files to ensure consistent classification colours.

## Visualising in QGIS
- Add the file to your project; layer appears in the layers panel.
- Open layer properties → Symbology → Paletted/unique values → Band 1.
- Use the style editor: Load style from LCMcolours_QGIS.qml.
- Apply and the map redraws with correct classification.

## Visualising in ArcGIS Desktop
- In the Catalog window, locate the data folder and expand the raster bands.
- Drag band_1 into the Table of Contents.
- Layer properties → Symbology → Unique Values (if prompted to build an attribute table, click YES).
- Import the provided LCMcolours.lyr to apply the correct classification.
- OK to redraw the map with the appropriate classification.

## Visualising in ArcGIS Pro
- Open the Catalog and locate the data folder; expand to view raster bands.
- Drag band_1 into the Table of Contents.
- Layer properties → Appearance > Symbology → Primary: Unique Values (if prompted, build attribute table = Yes).
- Use the hamburger menu in the Symbology panel → Import; load LCMcolours.lyr.
- Map will redraw with correct classification.