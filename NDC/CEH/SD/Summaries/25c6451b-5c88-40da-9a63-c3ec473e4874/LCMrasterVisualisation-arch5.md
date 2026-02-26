# Visualising UKCEH Land Cover Class using a GIS application

- The Land cover map rasters for 2017-2020 are multiband rasters with:
  - 20m and 10m: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence).
- This document provides a short guide for visualising the data contained in Band 1 using common GIS applications; a full data description is in the product documentation.

## Visualising with QGIS

- Add the file to your project; the layer appears in the layers panel.
- Open layer properties -> Symbology.
- Render type: Paletted/Unique Values; Band: Band 1.
- Choose the style -> Load style from the provided LCMcolours_QGIS.qml file, then OK.
- The map will redraw with the correct classification.

## Visualising with ArcGIS Desktop

- In the catalogue, navigate to the data folder and expand the raster to display its bands.
- Drag band_1 into the Table of Contents.
- Open the layer properties -> Symbology -> Unique Values (if prompted to build an attribute table, click YES).
- Click Import and load the accompanying LCMcolours.lyr file.
- OK to redraw the map with the correct classification.

## Visualising with ArcGIS Pro

- In the catalog, browse to the data folder and expand the raster to view its bands.
- Drag band_1 into the Table of Contents.
- Open layer properties -> Symbology (Appearance > Symbology).
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and choose Import, then load the LCMcolours.lyr file provided.
- The map will redraw with the correct classification.

## Relevance for Data Stewards

- Ensures consistent visualization across GIS tools by using standardized color styles and band definitions.
- Uses dedicated style files (LCMcolours_QGIS.qml, LCMcolours.lyr) to maintain uniform interpretation and improve data discoverability and reuse.
- Documents which band contains the classification identifiers (Band 1) to support metadata accuracy and user guidance.