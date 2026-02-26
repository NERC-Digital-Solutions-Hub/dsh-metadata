# Visualising UKCEH Land Cover Class using a GIS application

- Overview
  - Land Cover Map rasters are multi-band formats.
  - 20m and 10m rasters have two bands: Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
  - 25m rasters have three bands: Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence indicators.
  - This document is a short guide for visualising the Land Cover Class data in Band 1 using common GIS applications. For a full data description, refer to the product documentation.

- What to visualise
  - Visualise Band 1 (the class identifiers) to display land cover classes.
  - Use the provided colour styles to map class identifiers to colours.

- Visualising in QGIS
  - Add the file to your project; the layer appears in the layers panel.
  - Double-click the layer name in the layers panel to open Layer Properties.
  - In Symbology, set Render type to Paletted/Unique Values and Band to Band 1.
  - Click the style button and choose Load style from the menu.
  - Browse to LCMcolours_QGIS.qml, select it, and click Open.
  - Click OK to redraw the map with the correct classification.

- Visualising in ArcGIS Desktop
  - In the Catalog window, locate the data folder and expand the raster to display its bands.
  - Drag band_1 into the Table of Contents.
  - Double-click the layer name to open Layer Properties; go to the Symbology tab.
  - Choose Unique Values (if prompted to build the attribute table, click YES).
  - Click Import and load the provided LCMcolours.lyr file.
  - Click OK to redraw the map with the correct classification.

- Visualising in ArcGIS Pro
  - In the Catalog, browse to the data folder and expand the file to show the raster bands.
  - Drag Band_1 into the Table of Contents.
  - Double-click the layer to open Layer Properties, then Appearance > Symbology.
  - Choose Unique Values as the primary symbology option (if prompted to build an attribute table, click Yes).
  - Open the hamburger menu in the Symbology panel and choose Import.
  - Load the provided LCMcolours.lyr file.
  - The map will be redrawn with the correct classification.

- Additional notes for analysts
  - The confidence bands (Band 2 and/or Band 3) are available for quality assessment but are not used for the primary classification visualization described here.
  - The colour styles (LCMcolours_QGIS.qml and LCMcolours.lyr) accompany these instructions for accurate representation of land cover classes.