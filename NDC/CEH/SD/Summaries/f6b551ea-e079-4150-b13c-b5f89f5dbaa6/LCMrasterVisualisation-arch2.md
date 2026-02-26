# Visualising UKCEH Land Cover Class using a GIS application

- Land cover map rasters for 2017-2020 are multiband rasters.
- 20m and 10m rasters have two bands:
  - Band 1: UKCEH Land Cover Class identifier
  - Band 2: classification confidence indicator
- 25m rasters have three bands:
  - Band 1: dominant UKCEH Land Cover Class identifier
  - Bands 2 and 3: indicators of classification confidence
- This document is a short guide for using common GIS applications to visualize the Land Cover Class data contained in Band 1.
- For a full description of the data, refer to the product documentation.

## Visualising the data using QGIS

- Add the file to your project; the data will appear in the layers panel.
- Double-click the layer name in the layers panel to open the layer properties.
- In the render type box, choose Palleted/unique values.
- In the band box, choose Band 1.
- Double-click the style button and choose Load style from the menu.
- Browse to the LCMcolours_QGIS.qml file that accompanies this document, select it, and click Open.
- Click OK and the map will be redrawn with the correct classification.

## Visualising the data using ArcGIS Desktop

- In the Catalogue window, browse to the folder where the data is stored.
- Expand the file to display the raster's bands.
- Drag band_1 into the Table of Contents window.
- Double-click the layer name in the Table of Contents to display the layer properties.
- In the Layer Properties box, select the Symbology tab.
- Choose Unique Values as the symbology type (if prompted to calculate the values, click YES).
- Click the Import button and load in the layer file (LCMcolours.lyr) provided with these instructions.
- Click OK and the map will be redrawn with the correct classification.

## Visualising the data using ArcGIS Pro

- In your ArcGIS Pro project, open the Catalog pane.
- Browse to the folder where the data is stored; expand the file to display the raster's bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name in the Contents pane to display the layer properties.
- Select the layer in the Contents window and open the Symbology under Appearance.
- In the primary Symbology options, choose Unique Values. (If prompted to build an attribute table, click Yes.)
- Click the hamburger menu in the Symbology panel and choose Import.
- Load in the layer file (LCMcolours.lyr) provided with these instructions.
- The map will be redrawn with the correct classification.