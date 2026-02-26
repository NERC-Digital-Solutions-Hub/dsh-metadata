# Visualising UKCEH Land Cover Class using a GIS application

## Data structure and purpose
- Land cover map rasters for 2017-2020 are multiband rasters.
- 20m and 10m rasters: two bands.
  - Band 1: UKCEH Land Cover Class identifier.
  - Band 2: classification confidence indicator.
- 25m rasters: three bands.
  - Band 1: dominant UKCEH Land Cover Class identifier.
  - Bands 2 and 3: classification confidence indicators.
- This document is a short guide for visualising the Land Cover Class data in band 1 using common GIS applications.
- For a full data description, refer to the product documentation.
- Style files accompanying the instructions: LCMcolours_QGIS.qml (for QGIS) and LCMcolours.lyr (for ArcGIS).

## Visualising in QGIS
- Add the file to your project; the layer appears in the layers panel.
- Open layer properties and select Symbology.
- In Render type, choose Paletted/Unique values; set Band to Band 1.
- Click the style button, choose Load style, and select LCMcolours_QGIS.qml; open.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Desktop
- In the Catalog window, locate the data folder and expand the raster to view its bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties, then choose the Symbology tab.
- Select Unique Values (and, if prompted to build an attribute table, click YES).
- Click Import and load the LCMcolours.lyr file provided with these instructions.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro
- In ArcGIS Pro, open the Catalog, browse to the data folder, and expand the raster to view its bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties, then Appearance > Symbology.
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Click the hamburger menu in the Symbology panel and choose Import.
- Load the LCMcolours.lyr file provided with these instructions.
- The map will be redrawn with the correct classification.