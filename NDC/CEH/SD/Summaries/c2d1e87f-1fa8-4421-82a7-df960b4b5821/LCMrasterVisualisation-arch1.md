# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land Cover Map rasters are multiband.
- 20m and 10m rasters have two bands: Band 1 is the UKCEH Land Cover Class identifier; Band 2 indicates classification confidence.
- 25m rasters have three bands: Band 1 is the dominant class; Bands 2 and 3 are classification confidence indicators.
- This guide covers visualising the Land Cover Class data contained in Band 1 across common GIS applications. For full data details, refer to the product documentation.

## Visualising with QGIS
- Add the file to your project; the layer will appear in the layers panel.
- Open Layer properties → Symbology.
- In Render type, select Paletted/Unique values; in Band, choose Band 1.
- Click the style button → Load style from the menu.
- Browse to the LCMcolours_QGIS.qml file accompanying this document, select it, and click Open.
- Click OK to redraw the map with the correct classification.

## Visualising with ArcGIS Desktop
- In the Catalog window, browse to the folder containing the data.
- Expand the file to expose the raster’s bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- Choose the Symbology tab → set Symbology to Unique Values (if prompted to build values, click YES).
- Click the Import button → load the LCMcolours.lyr file provided with these instructions.
- Click OK to redraw the map with the correct classification.

## Visualising with ArcGIS Pro
- In your ArcGIS Pro project, open the Catalog pane.
- Browse to the folder containing the data and expand the file to reveal the raster bands.
- Drag band_1 into the Map’s Contents pane.
- Double-click the layer name to open its properties.
- With the layer selected, open Symbology (Appearance > Symbology).
- In Primary Symbology options, choose Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and choose Import.
- Load the LCMcolours.lyr file provided with these instructions.
- The map will be redrawn with the correct classification.