# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Short guide for visualising the Land Cover Class data (Band 1) contained in the UKCEH land cover rasters for 2017–2020.
- Data come in different resolutions with specific band structures:
  - 20 m and 10 m rasters: two bands (Band 1 = Land Cover Class identifier; Band 2 = classification confidence).
  - 25 m rasters: three bands (Band 1 = dominant Land Cover Class; Bands 2 and 3 = classification confidence).
- For a full data description, refer to the product documentation.
- The document provides platform-specific steps to ensure consistent visualization, leveraging pre-made style files.

## Data structure details
- 20 m and 10 m rasters: Band 1 identifies the UKCEH Land Cover Class; Band 2 indicates confidence.
- 25 m rasters: Band 1 identifies the dominant UKCEH Land Cover Class; Bands 2 and 3 indicate confidence.

## Visualisation by GIS platform

### Visualising with QGIS
- Add the file to your project; the data appears in the layers panel.
- Open layer properties -> Symbology.
- Set Render type to Paletted/Unique values; Band to Band 1.
- Click the style button -> Load style from the menu.
- Browse to LCMcolours_QGIS.qml (accompanying file), open.
- Click OK; the map redraws with the correct classification.

### Visualising with ArcGIS Desktop
- In the Catalogue, locate the data folder and expand to display the raster bands.
- Drag Band_1 into the Table of Contents.
- Open layer properties -> Symbology.
- Choose Unique Values; if prompted to calculate values, choose YES.
- Import the provided layer file: LCMcolours.lyr.
- OK; the map redraws with the correct classification.

### Visualising with ArcGIS Pro
- Open the Catalog, locate the data folder, and expand to view raster bands.
- Drag Band_1 into the Table of Contents.
- Open layer properties -> Appearance > Symbology.
- In Primary symbology, select Unique values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and choose Import; load LCMcolours.lyr.
- The map will redraw with the correct classification.

## Practical considerations for monitoring frameworks
- Ensures consistent visual interpretation across GIS platforms using standard style files.
- Highlights the importance of correct Band 1 identification for accurate classification visualization.
- Underlines the need to reference accompanying style files and the product documentation for full data context.

## Additional information
- The guide directs users to the accompanying style files (LCMcolours_QGIS.qml and LCMcolours.lyr) and notes the necessity of the full product documentation for detailed data descriptions.