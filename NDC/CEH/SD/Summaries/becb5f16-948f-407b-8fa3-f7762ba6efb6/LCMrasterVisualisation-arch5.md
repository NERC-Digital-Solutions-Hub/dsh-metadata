# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land Cover Map rasters are multiband.
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant class; Bands 2 and 3 = classification confidence indicators).
- The document is a short guide for visualising Band 1 data in common GIS applications. For a full data description, refer to the product documentation.

## Visualising in QGIS
- Add the file to your project; the layer appears in the layers panel.
- Open Layer Properties → Symbology.
- Render type: Paletted/unique values; Band: Band 1.
- Click Style → Load style, and select LCMcolours_QGIS.qml accompanying this document.
- Confirm (OK); map will redraw with the correct classification.

## Visualising in ArcGIS Desktop
- In the Catalogue window, browse to the data folder and expand the raster to show its bands.
- Drag Band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties → Symbology.
- Choose Unique Values; if prompted to build an attribute table, click YES.
- Click Import and load the provided LCMcolours.lyr file.
- Click OK; map will redraw with the correct classification.

## Visualising in ArcGIS Pro
- Open the Catalog and navigate to the data folder; expand to reveal the raster bands.
- Drag Band_1 into the Table of Contents.
- Open the layer’s properties (Appearance → Symbology).
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and choose Import; load LCMcolours.lyr.
- The map will redraw with the correct classification.

## Additional notes
- The LCMcolours_QGIS.qml and LCMcolours.lyr style files accompany these instructions to ensure consistent visualization across platforms.