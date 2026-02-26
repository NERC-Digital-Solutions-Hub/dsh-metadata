# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- This is a short guide for visualising the Land Cover Class data (band 1) in common GIS applications.
- For a full description of the data, refer to the product documentation.

## Data structure
- Land cover map rasters for 2017-2020 are multi-band rasters.
- 20m and 10m rasters: two bands
  - Band 1: UKCEH Land Cover Class identifier
  - Band 2: classification confidence
- 25m rasters: three bands
  - Band 1: dominant UKCEH Land Cover Class identifier
  - Bands 2 and 3: indicators of classification confidence

## Visualising the data in GIS applications

### QGIS
- Add the file to your project; the layer appears in the layers panel.
- Double-click the layer name in the layers panel to open Layer properties.
- In Symbology, select Paletted/Unique Values.
- In the Band box, choose Band 1.
- Click the style button, choose Load style from the menu.
- Browse to LCMcolours_QGIS.qml, select it, and click open.
- Click OK; the map is redrawn with the correct classification.

### ArcGIS Desktop
- In the Catalog window, locate the folder containing the data.
- Expand the file to display the raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer properties.
- In Symbology, choose Unique Values (if prompted to calculate values, click YES).
- Click Import and load the provided layer file (LCMcolours.lyr).
- Click OK; the map is redrawn with the correct classification.

### ArcGIS Pro
- In your ArcGIS Pro project, open the Catalog window.
- Browse to the folder containing the data and expand the raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer properties.
- In Contents, open Symbology (Appearance > Symbology).
- In Primary Symbology, choose Unique Values (if prompted to build a attribute table, click Yes).
- Click the hamburger menu in the Symbology panel and choose Import.
- Load the provided layer file (LCMcolours.lyr).
- The map is redrawn with the correct classification.

## Additional notes
- The colour styles files referenced are LCMcolours_QGIS.qml and LCMcolours.lyr, provided with these instructions.