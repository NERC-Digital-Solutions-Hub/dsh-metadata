# Visualising UKCEH Land Cover Class using a GIS application

- Data description
  - Land Cover Map rasters have band structures:
    - 20m and 10m rasters: two bands; Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence indicator.
    - 25m rasters: three bands; Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence indicators.
  - This short guide covers visualising data from Band 1. For full data description, refer to the product documentation.

- Visualising with QGIS
  - Add the file to your project; the layer appears in the Layers panel.
  - Double-click the layer name in the Layers panel to open Layer Properties.
  - In Symbology, set Render type to Paletted/Unique Values.
  - In Band, select Band 1.
  - Click the style button and choose Load style from the menu.
  - Browse to LCMcolours_QGIS.qml that accompanies this document, select it, and click Open.
  - Click OK; the map will redraw with the correct classification.

- Visualising with ArcGIS Desktop
  - In the Catalog window, navigate to the data folder and expand the raster to display its bands.
  - Drag Band_1 into the Table of Contents.
  - Double-click the layer name to open Layer Properties; go to the Symbology tab.
  - Choose Unique Values as the symbology type (if prompted to calculate values, click YES).
  - Click the Import button and load the LCMcolours.lyr file provided with these instructions.
  - Click OK; the map will redraw with the correct classification.

- Visualising with ArcGIS Pro
  - In a project, open the Catalog and browse to the data folder.
  - Expand the raster to display its bands; drag Band_1 into the Table of Contents.
  - Double-click the layer name to open Layer Properties; in the Contents window, open Appearance > Symbology.
  - In primary symbology options, choose Unique Values (and if prompted to build an attribute table, click Yes).
  - Use the hamburger menu in the Symbology panel and select Import.
  - Load the LCMcolours.lyr file provided with these instructions.
  - The map will redraw with the correct classification.