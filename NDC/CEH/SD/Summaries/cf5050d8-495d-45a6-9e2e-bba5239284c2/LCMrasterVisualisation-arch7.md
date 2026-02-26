# Visualising UKCEH Land Cover Class using a GIS application

- The Land cover map rasters for 2017-2020 are multi-band rasters with:
  - 20m and 10m datasets: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence)
  - 25m datasets: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 & 3 = classification confidence indicators)
- This document provides a short guide for visualising the Land Cover Class data using common GIS applications, focusing on Band 1 visualization.
- For a full data description, refer to the product documentation.

## Visualising in QGIS

- Add the file to your project; the layer appears in the layers panel.
- Open Layer properties for the layer and go to Symbology.
- Set Render type to Paletted/Unique Values; select Band 1.
- Click the style button and choose Load style from the menu.
- Load the LCMcolours_QGIS.qml file that accompanies this document; click OK to redraw the map with correct classification.

## Visualising in ArcGIS Desktop

- In the Catalogue window, navigate to the data folder, expand the raster to show its bands.
- Drag band_1 into the Table of Contents.
- Open the layer’s properties and go to the Symbology tab.
- Choose Unique Values (if prompted to build an attribute table, click Yes).
- Click Import and load the provided LCMcolours.lyr file.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro

- In your ArcGIS Pro project, open the Catalog and locate the data folder.
- Expand the raster to display its bands and drag band_1 into the Contents window.
- Open the layer’s properties (Appearance > Symbology).
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and choose Import; load LCMcolours.lyr.
- The map will be redrawn with the correct classification.