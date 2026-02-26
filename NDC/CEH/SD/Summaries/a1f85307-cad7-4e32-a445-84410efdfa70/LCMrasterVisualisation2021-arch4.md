# Visualising UKCEH Land Cover Class using a GIS application

## Overview

- This is a short guide for visualising UKCEH Land Cover Class data from 2021 using common GIS applications.
- Data are raster products with multiple bands: 10m rasters have 2 bands (Band 1 = class identifier; Band 2 = classification confidence), while 25m rasters have 3 bands (Band 1 = dominant class; Bands 2–3 = confidence).
- The visualization focus is on Band 1 to display the land cover classification. Refer to the product documentation for a full data description.

## Data structure and band mapping

- 10m rasters: Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
- 25m rasters: Band 1 = dominant Land Cover Class identifier; Bands 2 and 3 = classification confidence.

## Visualization steps by software

- QGIS
  - Add data to your project; select the layer.
  - Layer properties -> Symbology -> Paletted/Unique values; Band 1.
  - Click the style button, choose Load style, and load LCMcolours_QGIS.qml to apply correct classification colours.
  - The map will redraw with the correct classification.

- ArcGIS Desktop
  - In the Catalogue, navigate to the data folder and drag band_1 into the Table of Contents.
  - Layer properties -> Symbology -> Unique Values (choose Yes if prompted to build an attribute table).
  - Click Import and load LCMcolours.lyr to apply the color scheme; OK to redraw the map.

- ArcGIS Pro
  - In the Catalog, navigate to the data folder and drag band_1 into the Table of Contents.
  - Layer properties -> Appearance > Symbology -> Unique Values (Yes to build an attribute table if prompted).
  - Use the Import option in the symbology panel to load LCMcolours.lyr; the map will redraw with the correct classification.

## Governance and reuse considerations

- The provided color style files (LCMcolours_QGIS.qml, LCMcolours.lyr) ensure consistent visualization across tools and teams.
- For a complete understanding of the data, refer to the product documentation.
- Band 1 visualisation supports clear communication of classification, with the option to explore Band 2/3 (confidence) for quality assessment and more advanced analyses.