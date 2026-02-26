# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- This is a short guide for visualising the UKCEH Land Cover Class data in common GIS applications.
- Data cover land cover rasters for 2017–2020; multi-band rasters have different band structures by resolution.
- Band 1 contains the UKCEH Land Cover Class identifier; bands 2 (and 3 for 25m) provide classification confidence.
- The guide focuses on visualising Band 1; refer to the product documentation for full data description.

## Data details
- 20m and 10m rasters: two bands (Band 1 = class ID; Band 2 = confidence indicator).
- 25m rasters: three bands (Band 1 = dominant class ID; Bands 2–3 = confidence indicators).
- The document provides steps to visualise Band 1 using common GIS tools.

## Visualisation instructions by GIS platform

- QGIS
  - Add the file to your project; layer appears in the layers panel.
  - Open Layer Properties > Symbology.
  - Render type: Paletted/Unique Values; Band: Band 1.
  - Click the style button > Load style from the menu.
  - Load the LCMcolours_QGIS.qml file supplied with the document; open.
  - OK to redraw the map with the correct classification.

- ArcGIS Desktop
  - In Catalog, navigate to the dataset folder; expand the raster to show bands.
  - Drag band_1 into the Table of Contents.
  - Layer Properties > Symbology; set to Unique Values (confirm if prompted to calculate values).
  - Click Import and load the LCMcolours.lyr file supplied with the instructions.
  - OK to redraw the map with the correct classification.

- ArcGIS Pro
  - In the project Catalog, browse to the dataset folder and reveal raster bands.
  - Drag band_1 into the Table of Contents.
  - Layer Properties > Symbology; primary option: Unique values (Yes to building an attribute table if prompted).
  - Open the Symbology panel menu (hamburger) > Import; load LCMcolours.lyr.
  - The map will be redrawn with the correct classification.

## Files and provenance
- Style files accompany the document to ensure consistent visualization across platforms:
  - LCMcolours_QGIS.qml for QGIS
  - LCMcolours.lyr for ArcGIS Desktop and ArcGIS Pro

## Governance and data stewardship notes
- The guide reinforces consistent styling and interpretation of Band 1 across GIS tools, aiding reproducibility.
- Data stewards should ensure the appropriate style files are distributed with datasets and that metadata references the exact band definitions and visualization methods.
- While this guide covers visualization, refer to the full product documentation for comprehensive data description and governance considerations.