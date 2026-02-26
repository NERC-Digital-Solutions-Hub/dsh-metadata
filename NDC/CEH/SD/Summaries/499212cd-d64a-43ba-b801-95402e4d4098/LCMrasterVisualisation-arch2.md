# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Short guide for visualising Land Cover Class data in common GIS applications.
- Data: Land cover map rasters for 2017–2020, multi-band rasters with bands describing class identifiers and confidence.
- Use Band 1 (the dominant class identifier) to visualise classifications.
- Full data description available in product documentation.

## Data structure (bands)
- 20m and 10m rasters: two bands
  - Band 1: UKCEH Land Cover Class identifier
  - Band 2: classification confidence indicator
- 25m rasters: three bands
  - Band 1: dominant UKCEH Land Cover Class identifier
  - Bands 2 and 3: indicators of classification confidence

## Visualising in QGIS
- Add the file to your project; layer appears in the layers panel.
- Double-click the layer name to open Layer Properties.
- Symbology > render type: Paletted/unique values; Band: Band 1.
- Click style > Load style, browse to LCMcolours_QGIS.qml, open.
- OK to redraw the map with correct classification.

## Visualising in ArcGIS Desktop
- In Catalog, locate the data folder; expand to view raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- Symbology > type: Unique Values (if prompted to calculate values, click YES).
- Click Import and load the file LCMcolours.lyr provided with these instructions.
- OK to redraw the map with correct classification.

## Visualising in ArcGIS Pro
- Open the project and the Catalog; locate the data folder.
- Expand the file to view raster bands; drag band_1 to the Table of Contents.
- Double-click the layer to open Layer Properties.
- In Contents, open Appearance > Symbology; set Primary Symbology to Unique values (build attribute table if prompted).
- Open the hamburger menu in the Symbology panel → Import; load LCMcolours.lyr.
- The map will be redrawn with the correct classification.