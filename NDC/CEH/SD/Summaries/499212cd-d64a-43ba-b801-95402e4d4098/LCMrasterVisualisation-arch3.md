# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Short guide for visualising the UKCEH Land Cover Class data in common GIS applications.
- Land cover map rasters for 2017–2020 are multiband rasters with band structure varying by resolution.
- Band 1 contains the Land Cover Class identifier; bands 2–3 provide classification confidence indicators depending on resolution.
- For full data description, refer to the accompanying product documentation.

## Data structure
- 20m and 10m rasters: two bands
  - Band 1: UKCEH Land Cover Class identifier
  - Band 2: classification confidence indicator
- 25m rasters: three bands
  - Band 1: dominant UKCEH Land Cover Class identifier
  - Bands 2 and 3: indicators of classification confidence

## Visualization approach
- Purpose: visualise the Land Cover Class data contained in band 1 in standard GIS applications.
- Emphasises using predefined color/styles to ensure consistent classification display.

## Visualising in QGIS
- Add the file to your project; layer appears in the layers panel.
- Open layer properties, choose Symbology.
- Set render type to Paletted/Unique values; select Band 1.
- Click style, choose Load style from the menu.
- Load the accompanying LCMcolours_QGIS.qml file; click OK to redraw with correct classification.

## Visualising in ArcGIS Desktop
- In the Catalogue window, locate the data folder and expand the raster bands.
- Drag Band 1 into the Table of Contents.
- Open layer properties, go to Symbology.
- Choose Unique Values; if prompted to calculate values, click YES.
- Click Import and load LCMcolours.lyr; click OK to redraw with correct classification.

## Visualising in ArcGIS Pro
- Open the Catalogues window in your ArcGIS Pro project; locate the data folder and expand the raster bands.
- Drag Band 1 into the Table of Contents.
- Open layer properties and the Symbology (Appearance > Symbology).
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel to Import; load LCMcolours.lyr and redraw the map with correct classification.

## Notes
- The visualisation relies on pre-defined colour/style files to ensure consistent representation across platforms.
- For a complete data description and guidance, refer to the accompanying product documentation.