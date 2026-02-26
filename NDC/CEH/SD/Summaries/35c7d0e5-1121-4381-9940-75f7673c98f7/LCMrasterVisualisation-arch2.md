# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover rasters for 2017-2020 are multiband.
- 20m and 10m rasters: two bands; Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
- 25m rasters: three bands; Band 1 = dominant class; Bands 2-3 = confidence indicators.
- This document is a short guide for visualising the Band 1 data in common GIS applications; refer to the product documentation for a full data description.

## What you need
- Style files to apply correct classification colours:
  - LCMcolours_QGIS.qml for QGIS
  - LCMcolours.lyr for ArcGIS Desktop/Pro

## Visualising in QGIS
- Add the file to your project; the layer appears in the layers panel.
- Layer Properties → Symbology; Render type: Paletted/Unique Values; Band: Band 1.
- Click the style button → Load style → select LCMcolours_QGIS.qml → OK. The map redraws with the correct classification.

## Visualising in ArcGIS Desktop
- In the Catalog window, locate the data folder and expand the raster’s bands.
- Drag band_1 into the Table of Contents.
- Layer Properties → Symbology → Unique Values (if prompted to calculate values, click YES).
- Click Import → load LCMcolours.lyr → OK. The map redraws with the correct classification.

## Visualising in ArcGIS Pro
- Open the Catalog and locate the data folder; expand the raster to display bands.
- Drag band_1 into the Contents pane.
- Layer Properties → Appearance → Symbology → Primary: Unique Values (if prompted, build an attribute table).
- Use the hamburger menu in the Symbology panel → Import → load LCMcolours.lyr.
- The map redraws with the correct classification.

## Practical notes for analysts
- The visualisations convey Band 1 classifications consistently across GIS platforms.
- For detailed data description, consult the product documentation.
- This approach supports standardised, scrutiny-ready outputs and facilitates data access and reuse.