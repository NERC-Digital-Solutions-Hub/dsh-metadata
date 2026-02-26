# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover map rasters for 2017-2020 are multiband rasters.
- 20m and 10m datasets: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
- 25m datasets: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence).
- This document is a short guide for visualising the Land Cover Class data contained in Band 1 using common GIS applications; refer to the product documentation for full data description.

## Data structure details
- Band 1: Land Cover Class identifier (dominant class for 25m data).
- Band 2: Classification confidence (for 20m/10m).
- Band 3: Classification confidence (additional for 25m).

## Visualising with QGIS
- Add the file to your project; layer appears in the layers panel.
- Open layer properties and select Symbology.
- In Render type, choose Paletted/Unique values; set Band to Band 1.
- Click the style button, choose Load style from the menu.
- Load the LCMcolours_QGIS.qml file accompanying this document; click Open, then OK to redraw the map with correct classification.

## Visualising with ArcGIS Desktop
- In the Catalog window, locate the data folder and expand the raster to display its bands.
- Drag Band_1 into the Table of Contents.
- Open layer properties, go to Symbology, choose Unique Values (confirm values if prompted).
- Click Import and load the provided LCMcolours.lyr file.
- Click OK to redraw the map with the correct classification.

## Visualising with ArcGIS Pro
- In a project, open the Catalogue window and locate the data folder.
- Expand the raster to show its bands; drag Band_1 into the Table of Contents.
- Open layer properties (Contents) and go to Appearance > Symbology.
- In Primary Symbology, choose Unique values (answer Yes if prompted to build an attribute table).
- Use the hamburger menu in the Symbology panel and choose Import; load LCMcolours.lyr.
- The map will be redrawn with the correct classification.

## Data stewardship considerations
- The guide ensures consistent visualization across platforms by using standard style files (LCMcolours_QGIS.qml and LCMcolours.lyr).
- Visual consistency supports reliable interpretation of Land Cover Class data and alignment with user needs.
- For comprehensive data descriptions and provenance, refer to the full product documentation.
- Store and share the accompanying style files with datasets to maintain reproducible visual representations.