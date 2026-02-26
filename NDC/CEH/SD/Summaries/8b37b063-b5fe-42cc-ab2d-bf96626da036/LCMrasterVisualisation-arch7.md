# Visualising UKCEH Land Cover Class using a GIS application

## Data structure and purpose
- Land cover rasters for 2017–2020 are multiband rasters.
  - 20m and 10m rasters: two bands. Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence indicator.
  - 25m rasters: three bands. Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = confidence indicators.
- This document provides a short guide for visualising band 1 data in common GIS applications; refer to the product documentation for full data description.

## Visualisation workflow by application

### QGIS
- Add the file to your project to appear in the layers panel.
- Layer properties > Symbology:
  - Render type: Paletted/Unique Values
  - Band: Band 1
- Click Style > Load style > select LCMcolours_QGIS.qml accompanying this document > Open.
- Click OK; the map redraws with the correct classification.

### ArcGIS Desktop
- In the Catalogue, locate the data folder; expand the raster bands.
- Drag band_1 into the Table of Contents.
- Layer properties > Symbology:
  - Type: Unique Values (if prompted to build values, click YES)
- Click Import and load LCMcolours.lyr provided with these instructions.
- Click OK; the map redraws with the correct classification.

### ArcGIS Pro
- Open the catalogue in your project; expand the raster to view bands.
- Drag band_1 into the Table of Contents.
- Layer properties > Contents > Appearance > Symbology:
  - Primary: Unique Values (if prompted to build an attribute table, click Yes)
- Open the hamburger menu in the Symbology panel > Import.
- Load LCMcolours.lyr; the map redraws with the correct classification.

## Additional notes
- The files LCMcolours_QGIS.qml and LCMcolours.lyr accompany these instructions.