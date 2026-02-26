# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover map rasters for 2017-2020 are multiband rasters.
- 20m and 10m rasters: Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
- 25m rasters: Band 1 = dominant Land Cover Class; Bands 2-3 = confidence indicators.
- This document is a short guide for visualising Band 1 data in common GIS applications.
- For full data description, refer to the product documentation.
- Accompanying style files: LCMcolours_QGIS.qml and LCMcolours.lyr.

## Visualising with QGIS
- Add the file to your project; layer appears in the layers panel.
- Double-click the layer name to open Layer Properties → Symbology.
- Render type: Paletted/Unique Values; Band: Band 1.
- Click Style → Load Style from the menu.
- Browse to LCMcolours_QGIS.qml, select it, and click Open.
- Click OK; the map is redrawn with the correct classification.

## Visualising with ArcGIS Desktop
- In Catalog, locate the data folder; expand to display raster bands.
- Drag Band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties → Symbology.
- Choose Unique Values (if prompted to calculate values, click YES).
- Click Import and load the provided LCMcolours.lyr.
- Click OK; the map is redrawn with the correct classification.

## Visualising with ArcGIS Pro
- In ArcGIS Pro, open the Catalog, browse to the data folder, and expand to view raster bands.
- Drag Band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Contents, select the layer and open Symbology (Appearance > Symbology).
- Set primary symbology to Unique Values (and confirm to build the attribute table if prompted).
- Click the hamburger menu in the Symbology panel and choose Import; load LCMcolours.lyr.
- The map is redrawn with the correct classification.