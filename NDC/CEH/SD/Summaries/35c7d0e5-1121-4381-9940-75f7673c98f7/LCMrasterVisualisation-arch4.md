# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover map rasters for 2017-2020 are multiband rasters.
  - 20m and 10m rasters: two bands — Band 1 is the UKCEH Land Cover Class identifier; Band 2 indicates classification confidence.
  - 25m rasters: three bands — Band 1 is the dominant Land Cover Class; Bands 2 and 3 indicate classification confidence.
- This document is a short guide for visualising the Land Cover Class data (Band 1) in common GIS applications; refer to the product documentation for full data description.

## Visualization in GIS platforms

- QGIS
  - Add the file to your project; layer appears in the layers panel.
  - Open layer properties, select Symbology.
  - Render as Paletted/Unique Values, select Band 1.
  - Click style > Load style, choose LCMcolours_QGIS.qml, open, OK.
  - Map redraws with correct classification.

- ArcGIS Desktop
  - In the catalogue, navigate to the data folder and expand the raster bands.
  - Drag band_1 into the Table of Contents.
  - Open layer properties, go to Symbology, choose Unique Values (if prompted, approve value calculation).
  - Click Import and load LCMcolours.lyr provided with these instructions.
  - Map redraws with correct classification.

- ArcGIS Pro
  - Open the catalog, browse to the data folder, expand raster bands.
  - Drag band_1 into the Table of Contents.
  - Open layer properties, Appearance > Symbology.
  - In Primary symbology, choose Unique Values (Yes to build attribute table if prompted).
  - Use the hamburger menu in the symbology panel and choose Import to load LCMcolours.lyr.
  - Map redraws with correct classification.

## Style files provided
- LCMcolours_QGIS.qml (for QGIS)
- LCMcolours.lyr (ArcGIS Desktop/Pro)

## Data governance and usage notes for Data Leaders
- The guidance supports consistent, cross-platform visualization of the Land Cover Class (Band 1), aiding coordination across teams.
- Full data description and additional metadata are available in the product documentation.
- Band 2 (and Band 3 on 25m rasters) provide classification confidence indicators; leverage as needed to assess data quality in analyses and reporting.
- Ensure to use the accompanying style files to maintain consistent classification schemes across platforms.