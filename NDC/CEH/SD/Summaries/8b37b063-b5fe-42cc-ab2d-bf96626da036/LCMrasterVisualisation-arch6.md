# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Data: Land cover map rasters for 2017–2020, provided as multiband rasters.
  - 20m and 10m datasets: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m datasets: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2–3 = classification confidence).
- Purpose: A short guide for visualising the Land Cover Class data in Band 1 using common GIS applications; refer to the product documentation for the full data description.
- Output focus: Visual representation of the first band with a standardized color scheme to show classifications accurately.

## Visualising in QGIS
- Add the file to your project; the layer appears in the layers panel.
- Open Layer Properties → Symbology.
- Render as Paletted/Unique Values; Band = Band 1.
- Use the provided style: Load style from LCMcolours_QGIS.qml.
- Apply and redraw to display correct classification.

## Visualising in ArcGIS Desktop
- In Catalog, locate the data folder and expand the raster to view bands; drag band_1 into the Table of Contents.
- Layer Properties → Symbology.
- Set Unique Values (confirm value building if prompted).
- Import and load the provided LCMcolours.lyr.
- OK to redraw the map with correct classification.

## Visualising in ArcGIS Pro
- Open Catalog and locate the data folder.
- Expand the raster to show bands; drag band_1 into the Table of Contents.
- Layer Properties → Contents window → Appearance > Symbology.
- Primary symbology: Unique Values (Yes to build attribute table if prompted).
- Open the hamburger menu in the Symbology panel → Import; load LCMcolours.lyr.
- The map will redraw with the correct classification.

## Practical notes for Data Support
- The document provides actionable steps to enable end users to self-serve Land Cover Class visualisations.
- Standardized color styles (LCMcolours files) ensure consistent interpretation across tools.
- While focused on Band 1 visualisation, the guidance references the full data description in the product documentation for deeper understanding.