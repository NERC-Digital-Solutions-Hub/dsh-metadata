# Visualising UKCEH Land Cover Class using a GIS application

- The Land cover map raster data products for 2021 are multiband rasters:
  - 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2–3 = classification confidence indicators).
- The short guide focuses on visualising the Land Cover Class data contained in Band 1.
- For a full data description, refer to the product documentation.

## Visualising the data using QGIS

- Add the file to your project; it appears in the layers panel.
- Double-click the layer name in the layers panel to open Layer Properties.
- In the Symbology section, set Render type to Paletted/Unique Values.
- Set Band to Band 1.
- Click Style, choose Load style from the menu.
- Browse to LCMcolours_QGIS.qml (provided with this document), select it, and open.
- Click OK to redraw the map with the correct classification.

## Visualising the data using ArcGIS Desktop

- In the Catalog window, locate the folder containing the data and expand the raster to show its bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Symbology, choose Unique Values (if prompted to build values, click YES).
- Click Import and load the provided layer file (LCMcolours.lyr).
- Click OK to redraw the map with the correct classification.

## Visualising the data using ArcGIS Pro

- Open the Catalog, browse to the folder containing the data, and expand the raster to display its bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Appearance > Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Open the hamburger menu in the Symbology panel and choose Import.
- Load the provided layer file (LCMcolours.lyr).
- The map will be redrawn with the correct classification.