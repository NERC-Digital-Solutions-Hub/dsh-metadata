# Visualising UKCEH Land Cover 2015 class using a GIS application

- The 2015 Land Cover dataset is a 25m raster with two bands: Band 1 contains the land cover classification, Band 2 contains the mean per-polygon probability from the classification algorithm.
- This guide explains how to visualize the Land Cover Class data in Band 1 using commonly used GIS applications.
- For a full data description, refer to the product documentation.

## Visualising the data using QGIS

- Add the file to your QGIS project; the layer will appear in the layers panel.
- Double-click the layer name in the layers panel to open Layer Properties.
- In the left menu, select Symbology.
- In Render type, choose Paletted/Unique Values.
- In Band, select Band 1.
- Click Classify.
- Colours will be assigned to each land class; edit colours as appropriate using the colour recipe from the product documentation.
- Click OK to redraw the map with the correct classification.

## Visualising the data using ArcGIS Desktop

- In the Catalog window, browse to the folder containing the data.
- Expand the raster to expose its bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In the Symbology tab, choose Unique Values as the symbology type (if prompted to calculate values, click YES).
- Assign appropriate colours to the classes using the colour recipe from the product documentation.
- Click OK to redraw the map with the correct classification.