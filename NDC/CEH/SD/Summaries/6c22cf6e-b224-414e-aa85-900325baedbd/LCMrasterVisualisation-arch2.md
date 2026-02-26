# Visualising UKCEH Land Cover Class using a GIS application

- Overview of data
  - Land cover map rasters for 2017-2020 are multiband rasters.
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = confidence indicators).
  - Purpose: a short guide to visualising Land Cover Class data contained in Band 1 using common GIS applications.
  - For full data description, refer to the product documentation.

- Visualising with QGIS
  - Add the file to your project; layer appears in the layers panel.
  - Open layer properties and choose Symbology.
  - Set Render type to Paletted/Unique Values; select Band 1.
  - Click the style button and choose Load style from the menu.
  - Load the accompanying LCMcolours_QGIS.qml file and OK.
  - The map will redraw with the correct classification.

- Visualising with ArcGIS Desktop
  - In the Catalog window, locate the data folder and expand the raster to view its bands.
  - Drag band_1 into the Table of Contents.
  - Open the layer properties, go to the Symbology tab, and choose Unique Values.
  - If prompted to calculate values, click YES.
  - Click Import and load LCMcolours.lyr provided with these instructions.
  - The map will redraw with the correct classification.

- Visualising with ArcGIS Pro
  - In the catalog, browse to the data folder and expand the raster’s bands.
  - Drag band_1 into the Table of Contents.
  - Double-click the layer to open Layer Properties; in Contents, open Symbology (Appearance > Symbology).
  - Select Unique Values; if prompted to build an attribute table, click Yes.
  - Use the hamburger menu in the Symbology panel and choose Import.
  - Load LCMcolours.lyr; the map will redraw with the correct classification.