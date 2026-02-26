# Visualising UKCEH Land Cover Class using a GIS application

- Overview of data:
  - Land cover map rasters for 2017–2020, presented as multiband rasters.
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2–3 = classification confidence indicators).
  - Purpose: short guide for visualising Land Cover Class data in Band 1 using common GIS applications; refer to product documentation for full data description.

- Visualising the data using QGIS:
  - Add the file to your project; layer appears in the layers panel.
  - Open layer properties → Symbology.
  - Render as Paletted/Unique Values; Band = Band 1.
  - Load style from LCMcolours_QGIS.qml; apply to redraw the map with correct classification.

- Visualising the data using ArcGIS Desktop:
  - In Catalog, locate the data folder and expand the raster bands.
  - Drag band_1 into the Table of Contents.
  - Layer properties → Symbology; set to Unique Values (confirm value table if prompted).
  - Import the provided LCMcolours.lyr; apply to redraw the map with correct classification.

- Visualising the data using ArcGIS Pro:
  - In Catalog, navigate to the data folder and expand the raster bands.
  - Drag band_1 into the Contents.
  - Layer properties → Appearance → Symbology; choose Unique Values (build attribute table if prompted).
  - Use the Import option in the symbology panel to load LCMcolours.lyr; map updates to show correct classification.