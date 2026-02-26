# Visualising UKCEH Land Cover Class using a GIS application

- The Land cover map rasters for 2017-2020 are multiband rasters:
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant UKCEH Land Cover Class; Bands 2–3 = confidence indicators).
- This document is a short guide for visualising the Land Cover Class data contained in Band 1 using common GIS applications; refer to the product documentation for full data description.

## Visualising in QGIS

- Add the file to your project; layer appears in the layers panel.
- Open layer properties, choose Symbology.
- Render as Paletted/unique values; set Band to Band 1.
- Click Style, select Load style, and load LCMcolours_QGIS.qml accompanying the document.
- Apply; the map redraws with the correct classification.

## Visualising in ArcGIS Desktop

- In the Catalogue window, browse to the data folder and expand the raster to display its bands.
- Drag Band_1 into the Table of Contents.
- Open the layer properties; go to Symbology.
- Choose Unique Values (if prompted to calculate values, click YES).
- Click Import and load LCMcolours.lyr provided with the instructions.
- Click OK; the map redraws with the correct classification.

## Visualising in ArcGIS Pro

- In the project, open the Catalogue; browse to the data folder and expand to display the raster bands.
- Drag Band_1 into the Table of Contents.
- Open the layer in the Contents pane; in Appearance > Symbology, set the primary option to Unique Values.
- Open the hamburger menu in the Symbology panel and choose Import.
- Load LCMcolours.lyr; the map redraws with the correct classification.