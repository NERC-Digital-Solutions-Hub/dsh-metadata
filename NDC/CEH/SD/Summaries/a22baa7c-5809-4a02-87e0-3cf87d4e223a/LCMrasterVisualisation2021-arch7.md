# Visualising UKCEH Land Cover Class using a GIS application

- Overview
  - Land cover map raster data products for 2021 are multiband rasters.
  - 10m rasters have two bands: Band 1 is the UKCEH Land Cover Class identifier; Band 2 is an indicator of classification confidence.
  - 25m rasters have three bands: Band 1 is the dominant UKCEH Land Cover Class identifier; Bands 2 and 3 are indicators of classification confidence.
  - This document is a short guide for visualising the Land Cover Class data contained in band 1 using common GIS applications.
  - For a full description of the data, refer to the product documentation.
  - Colour styling files accompany the guide:
    - QGIS: LCMcolours_QGIS.qml
    - ArcGIS: LCMcolours.lyr

- Visualising the data using QGIS
  - Add the file to your project; the layer appears in the layers panel.
  - Open layer properties and select Symbology.
  - In Render type, choose Paletted/Unique Values; in Band, select Band 1.
  - Click the style button and choose Load style from the menu.
  - Browse to LCMcolours_QGIS.qml, select it, and click Open.
  - Click OK to redraw the map with the correct classification.

- Visualising the data using ArcGIS Desktop
  - In the Catalogue window, navigate to the data folder, expand the raster to show its bands.
  - Drag Band_1 into the Table of Contents.
  - Double-click the layer name to open Layer Properties; go to the Symbology tab.
  - Choose Unique Values as the symbology type; if prompted to calculate values, click YES.
  - Click the Import button and load the provided LCMcolours.lyr.
  - Click OK to redraw the map with the correct classification.

- Visualising the data using ArcGIS Pro
  - In the Catalog, browse to the data folder and expand to view the raster’s bands.
  - Drag Band_1 into the Table of Contents.
  - Double-click the layer to open Layer Properties; go to Appearance > Symbology.
  - In Primary Symbology, choose Unique Values (and if prompted, build an attribute table, click Yes).
  - Open the hamburger menu in the Symbology panel and choose Import.
  - Load the provided LCMcolours.lyr; the map will redraw with the correct classification.