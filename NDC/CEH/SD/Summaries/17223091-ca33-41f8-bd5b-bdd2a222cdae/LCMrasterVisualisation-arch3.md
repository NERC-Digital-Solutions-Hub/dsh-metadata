# Visualising UKCEH Land Cover Class using a GIS application

- Overview of data structure
  - Land Cover Map rasters have bands: 20m and 10m rasters use two bands; 25m rasters use three bands.
  - Band 1: UKCEH Land Cover Class identifier (dominant class for 25m); Band 2 and 3 indicate classification confidence.
  - This guide focuses on visualising the Land Cover Class data contained in Band 1.
  - For full data description, refer to the product documentation.

- Using QGIS
  - Add the file to your project; layer appears in the layers panel.
  - Open Layer properties > Symbology.
  - Set Render type to Paletted/Unique Values; Band to Band 1.
  - Click Style > Load style, and select LCMcolours_QGIS.qml included with the instructions.
  - Click OK to redraw the map with the correct classification colors.

- Using ArcGIS Desktop
  - In Catalog, locate the data folder; expand the raster to show its bands.
  - Drag band_1 into the Table of Contents.
  - Open layer properties > Symbology; choose Unique Values (if prompted to build an attribute table, select Yes).
  - Click Import and load the provided LCMcolours.lyr file.
  - Click OK to redraw the map with the correct classification colors.

- Using ArcGIS Pro
  - Open Catalog and navigate to the data; expand to view the raster bands.
  - Drag band_1 into the Table of Contents.
  - Open layer properties > Symbology; set Primary Symbology to Unique Values (if prompted to build an attribute table, select Yes).
  - Use the hamburger menu in the Symbology panel and choose Import; load LCMcolours.lyr.
  - The map will be redrawn with the correct classification colors.

- Key takeaway for monitoring work
  - Use the provided style files to ensure consistent, interpretable visualisation of land cover classifications across GIS platforms, aiding clear communication of environmental health monitoring results.