# Visualising UKCEH Land Cover 2015 class using a GIS application

## Overview
- The 2015 25m raster is two-band: band 1 contains the classification; band 2 contains the mean per-polygon probability from the classification algorithm.
- This document is a short guide for visualising the Land Cover Class data contained in band 1 using common GIS applications.
- For a full data description, refer to the product documentation.

## Visualising with QGIS
- Add the file to your project; the layer appears in the layers panel.
- Double-click the layer name to open Layer Properties.
- In Symbology, set Render type to Paletted/Unique Values.
- In Band, select Band 1.
- Click Classify.
- Colours will be assigned to each land class.
- Edit colours as appropriate (colour recipe available in the product documentation).
- Click OK; the map is redrawn with the correct classification.

## Visualising with ArcGIS Desktop
- In the Catalog window, browse to the data folder and expand the raster’s bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In the Symbology tab, choose Unique Values.
- If prompted to calculate values, click YES.
- Assign colours to the classes (colour recipe in the product documentation).
- Click OK; the map is redrawn with the correct classification.

## Additional notes
- For a full description of the data, refer to the product documentation.