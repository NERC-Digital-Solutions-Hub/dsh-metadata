# Visualising UKCEH Land Cover 2015 class using a GIS application

- Purpose: A short guide for visualising the Land Cover Class data from the UKCEH Land Cover 2015 raster in common GIS applications, to support interpretation and communication of environmental data for monitoring and decision-making.
- Data basics: 2015 25m raster with two bands:
  - Band 1: classification layer (land cover classes)
  - Band 2: mean per-polygon probability value produced by the classification algorithm
- Key note: For a full data description and the colour recipe, refer to the product documentation.

## Visualising the data using QGIS

- Add the file to your project; the layer appears in the layers panel.
- Double-click the layer name in the layers panel to open Layer Properties.
- In the left menu, select Symbology.
- In the render type box, choose Paletted/Unique Values.
- In the Band box, choose Band 1.
- Click the Classify button.
- Colours will be assigned to each land class; edit colours as appropriate (colour recipe in the product documentation).
- Click OK; the map is redrawn with the correct classification.

## Visualising the data using ArcGIS Desktop

- In the Catalogue window, browse to the folder containing the data.
- Expand the raster’s bands and drag band_1 into the Table of Contents.
- Double-click the layer name in the Table of Contents to open Layer Properties.
- In the Layer Properties box, select the Symbology tab.
- Choose Unique Values as the symbology type (if prompted to calculate values, click YES).
- Assign appropriate colours to the classes (colour recipe in the product documentation).
- Click OK; the map is redrawn with the correct classification.