# Visualising UKCEH Land Cover Class using a GIS application

- Purpose and data context
  - Short guide for visualising Land Cover Class data contained in band 1 of UKCEH Land Cover maps for 2017-2020.
  - Datasets have multiple bands: 20m and 10m rasters are two-band (Band 1: class identifier; Band 2: classification confidence), 25m rasters are three-band (Band 1: dominant class; Bands 2–3: confidence indicators).
  - For full data description, refer to the product documentation.

- Visualising with QGIS
  - Add the file to your project; layer appears in the layers panel.
  - Open layer properties → Symbology.
  - Render type: Paletted/Unique Values; Band: Band 1.
  - Click style → Load style from the provided LCMcolours_QGIS.qml file.
  - Confirm to redraw the map with the correct classification.

- Visualising with ArcGIS Desktop
  - In Catalog, browse to the data folder and expand the raster to reveal its bands.
  - Drag Band_1 into the Table of Contents.
  - Layer properties → Symbology → Unique Values.
  - If prompted to calculate values, click Yes.
  - Click Import and load the provided LCMcolours.lyr.
  - Click OK to redraw the map with the correct classification.

- Visualising with ArcGIS Pro
  - Open Catalog, browse to the data folder and expand the raster bands.
  - Drag Band_1 into the Table of Contents.
  - Layer properties → Appearance > Symbology; set to Unique Values.
  - Use the hamburger menu in the Symbology panel → Import; load LCMcolours.lyr.
  - Map will redraw with the correct classification (and note prompts about building an attribute table).

- Additional considerations for monitoring/framework authors
  - Uses standard colour/style files provided with the instructions to ensure consistent classification visualization.
  - Emphasizes the need to reference the accompanying style files and product documentation for full data description.
  - Demonstrates cross-platform steps (QGIS, ArcGIS Desktop, ArcGIS Pro) to support consistent visualization in monitoring workflows.