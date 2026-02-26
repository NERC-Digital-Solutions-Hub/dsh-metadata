# Visualising UKCEH Land Cover 2015 class using a GIS application

## Overview
- The 2015 25m raster is a two-band image: band 1 contains the land cover classification; band 2 contains the mean per-polygon probability value from the classification algorithm.
- This is a short guide for visualising the Land Cover Class data (band 1) using common GIS applications.
- For a full data description, refer to the product documentation.

## Visualising the data using QGIS
- Add the file to your project; it will appear in the layers panel.
- Double-click the layer name in the layers panel to open Layer Properties.
- In Symbology, set Render type to Paletted/Unique values and Band to Band 1.
- Click Classify; colours will be assigned to each land class.
- Edit colours as appropriate using the colour recipe found in the product documentation.
- Click OK to redraw the map with the correct classification.

## Visualising the data using ArcGIS Desktop
- In the Catalogue window, browse to the data folder and expand the raster’s bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties; go to the Symbology tab.
- Choose Unique Values as the symbology type (click YES if prompted to calculate values).
- Assign appropriate colours to the classes using the colour recipe from the product documentation.
- Click OK to redraw the map with the correct classification.

## Additional notes
- The guide focuses on visualising the Land Cover Class data from band 1; the second band provides the mean per-polygon probability and is not used in these visualization steps.
- Colouring guidance is referenced to the product documentation for consistency.