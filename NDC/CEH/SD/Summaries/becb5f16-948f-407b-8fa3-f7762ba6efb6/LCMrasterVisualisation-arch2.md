# Visualising UKCEH Land Cover Class using a GIS application

- Overview
  - Land Cover Map rasters are multiband:
    - 20m and 10m: two bands (Band 1 = Land Cover Class identifier; Band 2 = classification confidence).
    - 25m: three bands (Band 1 = dominant Land Cover Class identifier; Bands 2 & 3 = classification confidence).
  - This guide focuses on visualising the Land Cover Class data contained in Band 1.
  - For a full data description, refer to the product documentation.

- Purpose
  - Provides a short guide for visualising Band 1 data using the most commonly used GIS applications.

- Visualising with QGIS
  - Add the file to your project; the layer appears in the layers panel.
  - Layer > Properties > Symbology.
  - Render type: Paletted/Unique values; Band: Band 1.
  - Click the style button > Load style from the accompanying LCMcolours_QGIS.qml.
  - Open; the map is redrawn with the correct classification.

- Visualising with ArcGIS Desktop
  - In Catalog, locate the data folder and expand the raster to view its bands.
  - Drag band_1 into the Table of Contents.
  - Layer properties > Symbology.
  - Set Symbology type to Unique Values (if prompted to build the attribute table, click Yes).
  - Click Import and load the provided LCMcolours.lyr.
  - OK; the map is redrawn with the correct classification.

- Visualising with ArcGIS Pro
  - In the project, open the Catalog; browse the data folder and expand the raster to view bands.
  - Drag Band_1 into the Table of Contents.
  - Double-click the layer name to open Layer Properties; go to Appearance > Symbology.
  - Primary symbology: Unique Values (if prompted to build an attribute table, click Yes).
  - Open the hamburger menu in the Symbology panel and choose Import.
  - Load the provided LCMcolours.lyr; the map is redrawn with the correct classification.