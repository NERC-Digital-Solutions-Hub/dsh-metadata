# Visualising UKCEH Land Cover 2015 class using a GIS application

## Overview
- The 2015 Land Cover data is a 25m raster with two bands: Band 1 contains the land cover classification; Band 2 contains the mean per-polygon probability from the classifier.
- This is a short guide for visualising the Land Cover Class data in Band 1 using common GIS applications; refer to the product documentation for full data description.

## Visualising with QGIS
- Add the file to your project; the layer appears in the layers panel.
- Double-click the layer name in the layers panel to open Layer Properties.
- In the left menu, choose Symbology.
- In Render type, select Paletted/Unique values.
- In Band, choose Band 1.
- Click Classify.
- Colours will be assigned to each land class; edit colours as appropriate using the colour recipe in the product documentation.
- Click OK to redraw the map with the correct classification.

## Visualising with ArcGIS Desktop
- In the Catalogue window, browse to the data location.
- Expand the file to show the raster’s bands; drag Band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- Go to the Symbology tab.
- Choose Unique Values as the symbology type (if prompted to calculate values, click YES).
- Assign appropriate colours to the classes using the colour recipe from the product documentation.
- Click OK to redraw the map with the correct classification.

## Additional notes
- The colour recipe for visualisation is documented in the product documentation.
- The guide focuses on visualising land cover classifications contained in Band 1.

## Relevance for Data Leaders
- Provides a clear, repeatable workflow to visualise land cover classifications, aiding consistent dissemination of data products.
- Uses standard GIS practices to support discoverability, user-friendly presentation, and alignment with documented colour schemes.
- Reinforces the importance of linking visualisation steps to the underlying data description and governance materials in the product documentation.