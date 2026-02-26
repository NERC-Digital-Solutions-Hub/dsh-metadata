# Visualising UKCEH Land Cover Class using a GIS application

- Purpose and data structure
  - The Land Cover Map rasters are multiband.
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant Land Cover Class; Bands 2 and 3 = classification confidence indicators).
  - This guide focuses on visualising Land Cover Class data contained in Band 1.
  - For a full data description, refer to the product documentation.

- General workflow for GIS visualisation
  - Add the raster to your project.
  - Use Band 1 for classification visualisation.
  - Apply the appropriate colour style file to display correct classifications.
  - The guide includes specific steps and style files for common GIS applications.

- Visualising in QGIS
  - Add the file to your project; layer appears in the layers panel.
  - Layer properties > Symbology > Render type: Paletted/unique values; Band: Band 1.
  - Click style > Load style from the accompanying file.
  - Browse to LCMcolours_QGIS.qml, select, open, then OK.
  - The map will redraw with the correct classification.

- Visualising in ArcGIS Desktop
  - In Catalog, locate the data folder and expand the raster to view its bands.
  - Drag band_1 into the Table of contents.
  - Double-click the layer name to open Layer Properties > Symbology.
  - Choose Unique Values; if prompted to build an attribute table, click Yes.
  - Use Import to load the provided layer file (LCMcolours.lyr).
  - Click OK to redraw the map with correct classification.

- Visualising in ArcGIS Pro
  - In Project, open Catalog and navigate to the data folder.
  - Expand to view the raster bands and drag band_1 into the Table of Contents.
  - Open layer properties > Appearance > Symbology.
  - Primary symbology: Unique values (Yes to build attribute table if prompted).
  - Use the menu to Import and load LCMcolours.lyr.
  - The map will redraw with correct classification.