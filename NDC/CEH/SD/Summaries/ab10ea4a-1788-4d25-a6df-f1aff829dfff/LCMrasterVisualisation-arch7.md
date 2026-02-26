# Visualising UKCEH Land Cover Class using a GIS application

- The Land Cover Map rasters come in 20m and 10m with two bands: Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
- 25m rasters have three bands: Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence indicators.
- The document is a short guide focused on visualising data contained in Band 1; refer to the full product documentation for complete data descriptions.

## Visualising the data using QGIS

- Add the file to your project; the layer appears in the layers panel.
- Double-click the layer name in the layers panel to open Layer Properties.
- In the left menu, choose Symbology.
- In the Render type box, select Paletted/Unique Values.
- In the Band box, choose Band 1.
- Double-click the style section.
- Click the style button and choose Load style from the menu.
- Browse to LCMcolours_QGIS.qml that accompanies this document, select it, and open.
- Click OK; the map will redraw with the correct classification.

## Visualising the data using ArcGIS Desktop

- In the Catalogue window, browse to the folder containing the data.
- Expand the file to display the raster’s bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name in the Table of Contents to open Layer Properties.
- In the Layer Properties, select the Symbology tab.
- Choose Unique Values as the symbology type (if prompted to calculate values, click YES).
- Click the Import button and load the provided layer file (LCMcolours.lyr).
- Click OK; the map will redraw with the correct classification.

## Visualising the data using ArcGIS Pro

- In your ArcGIS Pro project, open the Catalogue window.
- Browse to the folder containing the data.
- Expand the file to display the raster’s bands.
- Drag Band_1 into the Table of Contents.
- Double-click the layer name in the Table of Contents to open Layer Properties.
- Select the layer in Contents and open Symbology (Appearance > Symbology).
- In the Primary Symbology options, choose Unique Values (if prompted to build an attribute table, click Yes).
- Click the hamburger menu in the Symbology panel and choose Import.
- Load the provided layer file (LCMcolours.lyr).
- The map will redraw with the correct classification.