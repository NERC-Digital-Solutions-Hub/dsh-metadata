# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Short guide to visualising Land Cover Class data in common GIS applications.
- Data are multi-band rasters with information on land cover classifications and classification confidence.

## Data structure details
- Land cover map rasters for 2017-2020 are multi-band rasters.
- 20m and 10m rasters: two bands.
  - Band 1: UKCEH Land Cover Class identifier.
  - Band 2: classification confidence indicator.
- 25m rasters: three bands.
  - Band 1: dominant UKCEH Land Cover Class identifier.
  - Bands 2 and 3: indicators of classification confidence.
- For full dataset description, refer to the product documentation.

## Visualization steps by software

- Visualising in QGIS
  - Add the file to the project; it appears in the layers panel.
  - Layer properties > Symbology > Render type: Paletted/unique values.
  - Band: Band 1.
  - Click style > Load style from the LCMcolours_QGIS.qml file accompanying this document.
  - Map redraws with correct classification.

- Visualising in ArcGIS Desktop
  - In the catalogue, locate the data and expand the raster’s bands.
  - Drag Band_1 into the Table of Contents.
  - Layer properties > Symbology > Unique Values (or prompt to calculate values → YES).
  - Import the LCMcolours.lyr file provided with these instructions.
  - OK to redraw the map with correct classification.

- Visualising in ArcGIS Pro
  - Open the project and use the catalogue to locate the data.
  - Expand the raster’s bands and drag Band_1 into the Table of Contents.
  - Layer properties > Contents > Appearance > Symbology.
  - Primary symbology: Unique values (if prompted to build an attribute table, click Yes).
  - Use the hamburger menu in the symbology panel > Import; load LCMcolours.lyr.
  - The map is redrawn with the correct classification.

## Notes
- The style files (LCMcolours_QGIS.qml and LCMcolours.lyr) accompany these instructions and should be loaded to ensure correct classification visuals.
- For a full data description, consult the product documentation.

## Relevance for monitoring frameworks
- Provides a standardized, clear visualization of land cover classifications for policy scrutiny and decision-making.
- Facilitates transparent communication of results to stakeholders through consistent color schemes and legends.
- Enables easy comparison across areas and time by using band 1 classifications, with optional confidence indicators visible when needed.