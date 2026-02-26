# Visualising UKCEH Land Cover Class using a GIS application

- The Land Cover Map rasters are multiband:
  - 20m and 10m rasters: two bands — Band 1 is the Land Cover Class identifier; Band 2 is a classification confidence indicator.
  - 25m rasters: three bands — Band 1 is the dominant class; Bands 2 and 3 indicate classification confidence.
- This guide focuses on visualising the Land Cover Class data contained in Band 1 using common GIS applications. For a full data description, refer to the product documentation.

## Visualising the data using QGIS
- Add the file to your project; the layer appears in the layers panel.
- Open the layer properties and select Symbology.
- In Render type, choose Paletted/Unique values.
- In Band, select Band 1.
- Click the style button and choose Load style from the menu.
- Load the LCMcolours_QGIS.qml file accompanying this document, then OK. The map redraws with correct classification.

## Visualising the data using ArcGIS Desktop
- In the Catalogue window, locate the data folder, expand the raster to reveal its bands, and drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties, then go to the Symbology tab.
- Choose Unique Values as the symbology type (if prompted to calculate values, click YES).
- Click Import and load the provided Layer file (LCMcolours.lyr).
- Click OK to redraw the map with the correct classification.

## Visualising the data using ArcGIS Pro
- In the Catalog pane, locate the data folder and expand to view the raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties, then Appearance > Symbology.
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and Choose Import.
- Load the provided layer file (LCMcolours.lyr); the map will redraw with the correct classification.