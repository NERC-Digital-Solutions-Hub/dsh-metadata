# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land Cover Map rasters are multiband.
  - 20m and 10m rasters: band 1 = UKCEH Land Cover Class identifier; band 2 = classification confidence.
  - 25m rasters: band 1 = dominant Land Cover Class identifier; bands 2 and 3 = classification confidence indicators.
- The guide focuses on visualising the Land Cover Class data in band 1.
- For a full description of the data, refer to the product documentation.

## Visualising the data using QGIS
- Add the file to your project; the layer appears in the layers panel.
- Open Layer properties > Symbology.
- In the render type, select Paletted/Unique values.
- In the band, choose Band 1.
- Click the style button > Load style from the menu.
- Browse to LCMcolours_QGIS.qml provided with the document, select and open.
- Click OK; the map redraws with the correct classification.

## Visualising the data using ArcGIS Desktop
- In the Catalog pane, browse to the data folder and expand the raster to display its bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties > Symbology.
- Choose Unique Values as the symbology type (if prompted to calculate values, click YES).
- Click the Import button and load the layer file LCMcolours.lyr provided with these instructions.
- Click OK; the map redraws with the correct classification.

## Visualising the data using ArcGIS Pro
- In the Catalog pane, browse to the data folder and expand the raster to display its bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties > Appearance > Symbology.
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Click the hamburger menu in the Symbology panel and choose Import.
- Load LCMcolours.lyr provided with these instructions.
- The map will be redrawn with the correct classification.