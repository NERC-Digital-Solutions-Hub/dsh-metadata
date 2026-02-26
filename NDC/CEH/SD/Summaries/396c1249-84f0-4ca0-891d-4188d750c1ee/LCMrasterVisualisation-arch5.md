# Visualising UKCEH Land Cover Class using a GIS application

- Data structure
  - 2017-2020 land cover map rasters are multiband.
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2–3 = classification confidence).
- Purpose
  - This is a short guide for visualising the Land Cover Class data contained in Band 1 using common GIS applications.
  - For a full data description, refer to the product documentation.

- Visualising with QGIS
  - Add the file to the project; it will appear in the layers panel.
  - Open layer properties for the layer; select Symbology.
  - Set render type to Paletted/Unique Values; choose Band 1.
  - Click style, choose Load style, and load LCMcolours_QGIS.qml provided with the document.
  - Apply; map redraws with correct classification.

- Visualising with ArcGIS Desktop
  - In Catalog, locate the data folder and expand the raster’s bands.
  - Drag band_1 into the Table of Contents.
  - Open layer properties; go to Symbology.
  - Choose Unique Values; if prompted to calculate values, confirm.
  - Click Import and load LCMcolours.lyr supplied with the instructions.
  - OK; map redraws with correct classification.

- Visualising with ArcGIS Pro
  - In a project, open the Catalog; navigate to the data folder.
  - Expand the raster to view its bands; drag band_1 into the Table of Contents.
  - Open layer properties (Contents → Symbology).
  - In primary symbology, select Unique values (if prompted to build an attribute table, choose Yes).
  - Use the hamburger menu in the Symbology panel to Import, and load LCMcolours.lyr.
  - Map will redraw with correct classification.