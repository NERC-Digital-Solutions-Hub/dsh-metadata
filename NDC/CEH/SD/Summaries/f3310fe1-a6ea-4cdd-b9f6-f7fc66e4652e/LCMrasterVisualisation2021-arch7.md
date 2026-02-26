# Visualising UKCEH Land Cover Class using a GIS application

- Overview
  - Land cover map raster data products for 2021.
  - 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence).
  - Focus of the guide: visualising the Land Cover Class data contained in Band 1.
  - For full data description, refer to the product documentation.

- Visualising in QGIS
  - Add the file to the project; layer appears in the layers panel.
  - Open Layer Properties -> Symbology.
  - Render type: Paletted/Unique Values; Band: Band 1.
  - Click the style button -> Load style from LCMcolours_QGIS.qml accompanying the document.
  - OK to redraw the map with correct classification.

- Visualising in ArcGIS Desktop
  - In Catalog, locate the data folder, expand to expose raster bands.
  - Drag band_1 into the Table of Contents.
  - Layer Properties -> Symbology -> Unique Values (accept prompt to build attribute table if asked).
  - Import the LCMcolours.lyr file provided with the instructions.
  - OK to redraw the map with correct classification.

- Visualising in ArcGIS Pro
  - Open Catalog within ArcGIS Pro and locate the data folder.
  - Expand to view raster bands and drag band_1 into the Table of Contents.
  - Layer properties -> Symbology (Appearance > Symbology) -> Primary: Unique Values (Yes to build attribute table if prompted).
  - Use the hamburger menu in the Symbology panel -> Import, and load LCMcolours.lyr.
  - Map will redraw with correct classification.