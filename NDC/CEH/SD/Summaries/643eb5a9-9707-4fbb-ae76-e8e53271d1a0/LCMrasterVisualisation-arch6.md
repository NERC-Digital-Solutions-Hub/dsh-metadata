# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover map rasters for 2017-2020 are multiband rasters.
- 20m and 10m rasters: two bands; Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
- 25m rasters: three bands; Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence indicators.
- This short guide focuses on visualising the Land Cover Class data contained in Band 1.
- For a full data description, refer to the product documentation.

## Visualising in QGIS
- Add the file to your project; the layer appears in the layers panel.
- Open layer properties, choose Symbology.
- Render as Paletted/Unique values; set Band to Band 1.
- Click style > Load style, select LCMcolours_QGIS.qml, and open.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Desktop
- In the Catalogue, locate the data folder and expand the raster to show its bands.
- Drag band_1 into the Table of Contents.
- Open layer properties, select the Symbology tab, choose Unique Values (if prompted to build an attribute table, click Yes).
- Click Import and load LCMcolours.lyr provided with these instructions.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro
- In the Catalog, browse to the data folder and expand the raster bands.
- Drag band_1 into the Table of Contents.
- Open layer properties, then Appearance > Symbology.
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel to Import and load LCMcolours.lyr.
- The map will be redrawn with the correct classification.