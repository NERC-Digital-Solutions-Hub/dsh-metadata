# Visualising UKCEH Land Cover Class using a GIS application

## Dataset structure and purpose
- The Land cover map rasters for 2017-2020 are multi-band rasters.
- 20m and 10m raster datasets have two bands: Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
- 25m datasets have three bands: Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = indicators of classification confidence.
- This document is a short guide for visualising the Land Cover Class data contained in band 1; refer to the product documentation for a full data description.

## Visualisation workflow by GIS application
- Visualising with QGIS
  - Add the file to your project; the data appears in the layers panel.
  - Open layer properties, select Symbology.
  - In Render type, choose Paletted/unique values; Band = Band 1.
  - Click style > Load style from the menu; load LCMcolours_QGIS.qml; click OK; map redraws with correct classification.
- Visualising with ArcGIS Desktop
  - In Catalogue, locate the data folder; expand the raster to display bands.
  - Drag band_1 into the Table of Contents.
  - Open layer properties, Symbology tab; choose Unique Values; if prompted to calculate values, click YES.
  - Click Import and load LCMcolours.lyr; OK; map redraws with correct classification.
- Visualising with ArcGIS Pro
  - In the Catalog, open the project and browse to the data folder.
  - Expand the raster to display bands; drag band_1 into the Contents.
  - Open layer properties, Appearance > Symbology; select Unique values (if prompted to build an attribute table, click Yes).
  - Use the hamburger menu in the Symbology panel and choose Import; load LCMcolours.lyr; map redraws with correct classification.