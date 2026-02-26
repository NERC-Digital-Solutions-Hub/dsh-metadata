# Visualising UKCEH Land Cover Class using a GIS application

- Purpose of the document
  - Short guide to visualise the Land Cover Class data (band 1) from UKCEH Land Cover Map rasters using common GIS applications.
  - Note: 20m and 10m rasters have two bands (Band 1: Land Cover Class; Band 2: classification confidence). 25m rasters have three bands (Band 1: dominant Land Cover Class; Bands 2–3: confidence indicators).
  - For a full data description, refer to the product documentation.

- Visualisation in QGIS
  - Add the file to your project; layer appears in the layers panel.
  - Open Layer Properties -> Symbology.
  - Render as Paletted/Unique Values -> Band 1.
  - Load style from accompanying LCMcolours_QGIS.qml file.
  - Click OK to redraw the map with correct classification.

- Visualisation in ArcGIS Desktop
  - In Catalog, locate the data folder; expand the raster to view its bands.
  - Drag band_1 into the Table of Contents.
  - Layer Properties -> Symbology -> Unique Values (if prompted to calculate values, click YES).
  - Click Import and load LCMcolours.lyr provided with the instructions.
  - Click OK to redraw the map with correct classification.

- Visualisation in ArcGIS Pro
  - Open Catalog -> browse to data folder -> expand raster to view bands.
  - Drag band_1 into the Table of Contents.
  - Layer Properties -> Contents -> Symbology (Appearance > Symbology).
  - Primary symbology: Unique Values (if prompted to build an attribute table, click Yes).
  - Use the hamburger menu in the Symbology panel and choose Import; load LCMcolours.lyr.
  - Map will be redrawn with the correct classification.