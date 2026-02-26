# Visualising UKCEH Land Cover Class using a GIS application

## Overview of the data
- Land cover map rasters for 2017-2020 are multiband rasters.
- 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
- 25m rasters: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2–3 = classification confidence indicators).
- This guide focuses on visualising band 1; refer to product documentation for full data descriptions.

## Visualising in QGIS
- Add the file to your project; the layer appears in the layers panel.
- Layer properties > Symbology.
- Render type: Paletted/Unique Values; Band: Band 1.
- Click Style > Load style and select LCMcolours_QGIS.qml accompanying the document.
- OK to redraw the map with correct classification.

## Visualising in ArcGIS Desktop
- In Catalog, locate the data folder and expand the raster to view its bands.
- Drag band_1 into the Table of Contents.
- Layer properties > Symbology; set to Unique Values (confirm if prompted to build attribute table).
- Import the provided LCMcolours.lyr file; OK to redraw with the correct classification.

## Visualising in ArcGIS Pro
- In Catalog, locate the data folder and expand the raster bands.
- Drag band_1 into the Table of Contents.
- Layer properties > Symbology (Appearance > Symbology); choose Unique Values.
- Use the hamburger menu in the symbology panel > Import; load LCMcolours.lyr.
- Map will be redrawn with the correct classification.