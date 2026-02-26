# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- This is a short guide for visualising Land Cover Class data stored in band 1 of UKCEH Land Cover Map rasters.
- The rasters are multiband:
  - 20m and 10m: two bands (Band 1 = Land Cover Class identifier; Band 2 = classification confidence).
  - 25m: three bands (Band 1 = dominant Land Cover Class identifier; Bands 2–3 = classification confidence).
- For a full data description, refer to the product documentation.

## Purpose for analysts
- Provide a consistent approach to visualising environmental data in standard GIS tools.
- Use the band 1 classification and predefined colour styles to render maps accurately.

## Visualising in QGIS
- Add the file to your project; the layer appears in the layers panel.
- Open Layer Properties for the layer → Symbology.
- Render type: Paletted/Unique Values.
- Band: Band 1.
- Click Style → Load style from LCMcolours_QGIS.qml (accompanying file); open.
- Click OK; the map redraws with correct classification.

## Visualising in ArcGIS Desktop
- In Catalog, locate the data folder and expand the raster to display its bands.
- Drag Band_1 into the Table of Contents.
- Open Layer Properties → Symbology.
- Choose Unique Values (if prompted to build the attribute table, click Yes).
- Click Import and load LCMcolours.lyr (provided with the instructions).
- Click OK; the map redraws with correct classification.

## Visualising in ArcGIS Pro
- In Catalog, browse to the data folder; expand the raster bands.
- Drag Band_1 into the Table of Contents.
- Open the layer, then Symbology (Appearance > Symbology).
- Primary options: Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel → Import; load LCMcolours.lyr.
- The map will be redrawn with the correct classification.