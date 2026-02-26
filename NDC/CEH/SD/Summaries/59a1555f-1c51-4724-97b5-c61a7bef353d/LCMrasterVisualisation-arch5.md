# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Short guide for visualising the Land Cover Class data contained in band 1 using common GIS applications.
- The full data description is available in the product documentation.

## Data structure (bands)
- 20m and 10m rasters: two bands — Band 1 is the UKCEH Land Cover Class identifier; Band 2 is a classification confidence indicator.
- 25m rasters: three bands — Band 1 is the dominant UKCEH Land Cover Class identifier; Bands 2 and 3 are indicators of classification confidence.
- Visualisation focuses on band 1 for the classification.

## Visualisation workflow by GIS application

- QGIS
  - Add the file to the project; layer appears in the layers panel.
  - Layer properties > Symbology.
  - Render type: Paletted/Unique values; Band: Band 1.
  - Load style from LCMcolours_QGIS.qml; apply to redraw the map with correct classification.

- ArcGIS Desktop
  - In Catalog, locate the data folder; expand to reveal raster bands.
  - Drag Band_1 into the Table of Contents.
  - Layer properties > Symbology: Unique Values (Yes to any value calculation prompt).
  - Import the file LCMcolours.lyr; OK to redraw with correct classification.

- ArcGIS Pro
  - Open Catalogue, locate data folder; expand raster bands.
  - Drag Band_1 into the Table of Contents.
  - Layer properties > Appearance > Symbology: Primary -> Unique Values (Yes to build attribute table if prompted).
  - Use the hamburger menu in the Symbology panel > Import; load LCMcolours.lyr; map redraws with correct classification.

## Notes for data governance and usability
- The accompanying style files (LCMcolours_QGIS.qml and LCMcolours.lyr) are used to ensure consistent, correct classification visuals across platforms.
- This visualization approach supports usability and discoverability by presenting a consistent colour mapping for the Land Cover Class identifiers.
- For a complete description of the data, refer to the product documentation.