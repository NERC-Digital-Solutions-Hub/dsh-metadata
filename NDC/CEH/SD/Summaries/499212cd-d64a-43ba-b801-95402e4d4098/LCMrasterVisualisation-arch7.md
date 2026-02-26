# Visualising UKCEH Land Cover Class using a GIS application

## Data structure and purpose
- Land cover map rasters for 2017–2020 are multiband rasters.
- 20 m and 10 m rasters: two bands
  - Band 1: UKCEH Land Cover Class identifier
  - Band 2: classification confidence
- 25 m datasets: three bands
  - Band 1: dominant UKCEH Land Cover Class identifier
  - Bands 2–3: indicators of classification confidence
- This document is a short guide for visualising Band 1 data in common GIS applications.
- For a full description of the data, refer to the product documentation.

## Visualising in QGIS
- Add the file to your project; the layer appears in the layers panel.
- Double-click the layer name to open Layer Properties.
- Choose Symbology from the left menu.
- In Render Type, select Paletted/Unique values.
- In Band, select Band 1.
- Click the style button and choose Load style from the menu.
- Browse to LCMcolours_QGIS.qml that accompanies this document, select it, and open.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Desktop
- In the Catalogue window, navigate to the data folder.
- Expand the file to show the raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In the Symbology tab, select Unique Values (if prompted to calculate values, click YES).
- Click the Import button and load the provided LCMcolours.lyr.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro
- In an ArcGIS Pro project, open the Catalogue window and navigate to the data folder.
- Expand the file to show the raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Contents, open Appearance > Symbology.
- In Primary Symbology, choose Unique Values (if prompted, build the attribute table: Yes).
- Click the hamburger menu in the Symbology panel and choose Import.
- Load the LCMcolours.lyr file provided with these instructions.
- The map will be redrawn with the correct classification.