# Visualising UKCEH Land Cover Class using a GIS application

- Purpose: Quick guide to visualize the UKCEH Land Cover Class data in common GIS applications, focusing on band 1 across 10m and 25m raster products.
- Data structure:
  - 10m rasters: two bands
    - Band 1 = UKCEH Land Cover Class identifier
    - Band 2 = classification confidence
  - 25m rasters: three bands
    - Band 1 = dominant UKCEH Land Cover Class identifier
    - Bands 2-3 = classification confidence
- Reference: For full data description, consult the product documentation. Accompanying files used for styling: LCMcolours_QGIS.qml and LCMcolours.lyr.

## Visualising the data using QGIS

- Add the file to your project; the layer appears in the layers panel.
- Open layer properties and select Symbology.
- Set Render type to Paletted/unique values.
- Set Band to Band 1.
- Click the style button and choose Load style from the menu.
- Browse to LCMcolours_QGIS.qml, select it, and click Open.
- Click OK to redraw the map with the correct classification.

## Visualising the data using ArcGIS Desktop

- In the Catalogue window, locate the data folder, expand to view the raster’s bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open the Layer Properties.
- In Symbology, choose Unique Values (and, if prompted to build values, click YES).
- Click Import and load the provided LCMcolours.lyr.
- Click OK; the map will redraw with the correct classification.

## Visualising the data using ArcGIS Pro

- Open the Catalog and locate the data folder, expand to view raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Contents, open Appearance > Symbology.
- In Primary Symbology, choose Unique Values (and, if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and choose Import.
- Load LCMcolours.lyr; the map will redraw with the correct classification.