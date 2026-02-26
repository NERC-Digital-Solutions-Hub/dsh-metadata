# Visualising UKCEH Land Cover Class using a GIS application

- Purpose: Guide to visualise Land Cover Map data (band 1) in common GIS applications; notes that 20m/10m rasters have two bands (Band 1: class identifier; Band 2: classification confidence) and 25m rasters have three bands (Band 1: dominant class; Bands 2–3: confidence). Refer to full product documentation for complete data description.

- Key requirement: Visualisation focuses on Band 1 to display the Land Cover Class.

- QGIS instructions:
  - Add the file to the project; layer appears in the layers panel.
  - Open Layer Properties > Symbology.
  - Render as Paletted/Unique Values; select Band 1.
  - Click style > Load style from LCMcolours_QGIS.qml accompanying the document.
  - Click OK to redraw the map with correct classification.

- ArcGIS Desktop instructions:
  - In Catalog, locate the data folder and expand the raster to view bands.
  - Drag Band 1 into the Table of Contents.
  - Open Layer Properties > Symbology; choose Unique Values (OK to build attribute table if prompted).
  - Click Import and load LCMcolours.lyr provided with the instructions.
  - Click OK to redraw the map with correct classification.

- ArcGIS Pro instructions:
  - Open Catalog in the project and navigate to the data folder; expand raster bands.
  - Drag Band 1 into the Table of Contents.
  - Open layer’s Symbology (Appearance > Symbology); set primary to Unique Values (Yes to build attribute table if prompted).
  - Use the hamburger menu in the Symbology panel to Import and load LCMcolours.lyr.
  - Map will be redrawn with correct classification.

- Additional notes:
  - The accompanying style files (LCMcolours_QGIS.qml, LCMcolours.lyr) ensure consistent classification visuals across platforms.
  - For a full data description, refer to the product documentation.