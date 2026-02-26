# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover map raster data products for 2021 are multiband rasters.
- 10m rasters: two bands. Band 1 is the UKCEH Land Cover Class identifier; Band 2 indicates classification confidence.
- 25m rasters: three bands. Band 1 is the dominant UKCEH Land Cover Class identifier; Bands 2 and 3 indicate classification confidence.
- This short guide focuses on visualising the data using common GIS applications, concentrating on Band 1. For a full data description, refer to the product documentation.

## Data structure details
- Band 1: Land Cover Class identifier (dominant class for 25m).
- Bands 2-3: classification confidence indicators.
- Style files accompany the instructions to aid visualisation (e.g., LCMcolours_QGIS.qml, LCMcolours.lyr).

## Visualisation workflow by software

### QGIS
- Add the file to your project; layer appears in the layers panel.
- Double-click the layer name in the layers panel to open Layer Properties.
- Symbology: render as Paletted/Unique Values; Band: Band 1.
- Click Style > Load style from the LCMcolours_QGIS.qml file provided with the document; open.
- OK; the map is redrawn with the correct classification.

### ArcGIS Desktop
- In the Catalogue window, locate the data folder and expand to show the raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties; Symbology tab.
- Choose Unique Values (and if prompted to build an attribute table, click Yes).
- Click Import and load the provided LCMcolours.lyr.
- OK; the map is redrawn with the correct classification.

### ArcGIS Pro
- In the Catalog pane, navigate to the data folder and expand to display the raster bands.
- Drag Band_1 into the Table of Contents.
- Open the layer's Properties and go to Symbology (Appearance > Symbology).
- Set the primary symbology to Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and choose Import; load the provided LCMcolours.lyr.
- The map will be redrawn with the correct classification.