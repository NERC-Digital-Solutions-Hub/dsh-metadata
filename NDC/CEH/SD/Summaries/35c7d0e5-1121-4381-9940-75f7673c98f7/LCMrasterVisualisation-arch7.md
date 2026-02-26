# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover map rasters for 2017-2020 are multiband rasters.
- 20m and 10m rasters: two bands — Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
- 25m rasters: three bands — Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2–3 = confidence indicators.
- This document provides a short guide to visualising Band 1 data in common GIS applications; refer to the product documentation for a full data description.

## Visualising in QGIS
- Add the file to your project; layer appears in the layers panel.
- Open layer properties and select Symbology.
- Render as Paletted/Unique values; choose Band 1.
- Click Load style and select LCMcolours_QGIS.qml accompanying the document; apply to redraw the map with correct classification.

## Visualising in ArcGIS Desktop
- In Catalog, navigate to the data folder and expand the raster bands.
- Drag Band_1 into the Table of Contents.
- Open Layer Properties → Symbology; choose Unique Values (if prompted to calculate values, click YES).
- Click Import and load LCMcolours.lyr provided with these instructions; map redraws with proper classification.

## Visualising in ArcGIS Pro
- Open Catalog, locate the data folder, and expand the raster bands.
- Drag Band_1 into the Table of Contents.
- Open Layer Properties → Appearance > Symbology; select Unique Values (answer Yes to build the attribute table if prompted).
- Use the hamburger menu in the Symbology panel and choose Import; load LCMcolours.lyr; map redraws with correct classification.