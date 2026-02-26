# Visualising UKCEH Land Cover Class using a GIS application

- Overview
  - This is a short guide for visualising the Land Cover Class data contained in band 1 of the UKCEH land cover rasters (2017–2020).
  - Raster data characteristics by resolution:
    - 20m and 10m: two bands (Band 1 = Land Cover Class identifier; Band 2 = classification confidence).
    - 25m: three bands (Band 1 = dominant Land Cover Class identifier; Bands 2–3 = classification confidence).
  - A full data description is available in the product documentation.
  - The document provides workflow to ensure consistent visualization across common GIS platforms using supplied styling files.

- Visualising in QGIS
  - Add the file to your project; layer will appear in the layers panel.
  - Double-click the layer name to open Layer Properties.
  - In Symbology, set Render type to Paletted/Unique Values and Band to Band 1.
  - Click the style "load" button and load LCMcolours_QGIS.qml provided with the document.
  - Click OK to redraw the map with the correct classification.

- Visualising in ArcGIS Desktop
  - In the Catalogue window, navigate to the data folder and expand the raster to show its bands.
  - Drag band_1 into the Table of Contents.
  - Double-click the layer name to open Layer Properties; choose the Symbology tab.
  - Select Unique Values (if prompted to calculate values, confirm YES).
  - Click Import and load the accompanying LCMcolours.lyr file.
  - Click OK to redraw the map with the correct classification.

- Visualising in ArcGIS Pro
  - Open the Catalog, browse to the data folder, and expand the raster to display its bands.
  - Drag band_1 into the Table of Contents.
  - Double-click the layer name to open Layer Properties; go to Appearance > Symbology.
  - Choose Unique Values as the primary symbology (if prompted to build an attribute table, select Yes).
  - Open the hamburger menu in the Symbology panel and choose Import; load LCMcolours.lyr.
  - The map will be redrawn with the correct classification.