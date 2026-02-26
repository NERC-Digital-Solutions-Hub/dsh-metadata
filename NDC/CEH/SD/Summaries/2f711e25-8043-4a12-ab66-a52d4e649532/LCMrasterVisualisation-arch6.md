# Visualising UKCEH Land Cover Class using a GIS application

## Purpose and data structure
- Short guide for visualising UKCEH Land Cover Class data contained in band 1 of land cover rasters (2017–2020).
- Raster datasets:
  - 20m and 10m: two bands — Band 1 identifier, Band 2 classification confidence.
  - 25m: three bands — Band 1 dominant identifier, Bands 2 and 3 classification confidence.
- For a full data description, refer to the product documentation.

## Visualising in QGIS
- Add the file to your project; it appears in the layers panel.
- Layer Properties > Symbology > Render type: Paletted/unique values > Band: Band 1.
- Click Style > Load style, select LCMcolours_QGIS.qml, and open.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Desktop
- In the Catalog, locate the data folder and expand the raster’s bands; drag band_1 into the Table of Contents.
- Layer Properties > Symbology > Unique Values (if prompted to build an attribute table, click Yes).
- Click Import and load LCMcolours.lyr provided with the instructions.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro
- Open Catalog, browse to the data folder, expand the raster bands, and drag band_1 into the Table of Contents.
- Layer properties > Appearance > Symbology; choose Unique Values.
- In the Symbology panel, use the hamburger menu and Import to load LCMcolours.lyr.
- The map will redraw with the correct classification.