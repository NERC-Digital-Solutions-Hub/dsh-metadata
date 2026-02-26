# Visualising UKCEH Land Cover Class using a GIS application

- Overview
  - Short guide to visualising Land Cover Class data contained in band 1 of the UKCEH raster products (10m and 25m resolutions).
  - 10m rasters: two bands (Band 1 = Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant Land Cover Class identifier; Bands 2–3 = classification confidence).
  - Focus is on visualising the band 1 classifications using common GIS applications; refer to the full product documentation for complete data details.

- Visualising in QGIS
  - Add the file to your project; layer appears in the layers panel.
  - Open Layer Properties > Symbology.
  - Render type: Paletted/Unique values; Band: Band 1.
  - Click Style > Load style from the provided LCMcolours_QGIS.qml file, then OK to redraw the map with correct classification.

- Visualising in ArcGIS Desktop
  - In the Catalogue window, navigate to the data folder and expand the raster to show its bands.
  - Drag band_1 into the Table of Contents.
  - Double-click the layer name to open Layer Properties > Symbology.
  - Select Unique Values (if prompted to build values, click YES).
  - Click Import and load the provided LCMcolours.lyr file; OK to redraw the map with correct classification.

- Visualising in ArcGIS Pro
  - In your project, open the Catalog and browse to the data folder.
  - Expand the file to show the raster bands and drag band_1 into the Table of Contents.
  - Open the layer’s Symbology (Appearance > Symbology).
  - Choose Unique Values; if prompted to build an attribute table, click Yes.
  - Use the hamburger menu in the Symbology panel and choose Import to load LCMcolours.lyr; the map will redraw with the correct classification.

- Additional notes
  - The instructions focus on visualising band 1 for classification; refer to the accompanying data files and documentation for complete data details and legend mappings.