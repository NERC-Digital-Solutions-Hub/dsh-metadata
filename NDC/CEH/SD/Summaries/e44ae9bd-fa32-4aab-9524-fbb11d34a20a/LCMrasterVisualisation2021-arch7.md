# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Provides guidance for visualising UKCEH Land Cover Class data in common GIS applications.
- Data are 2021 land cover rasters; 10m rasters have 2 bands (Band 1: Land Cover Class identifier; Band 2: classification confidence), 25m rasters have 3 bands (Band 1: dominant class; Bands 2–3: confidence indicators).
- Focuses on visualising band 1 (Land Cover Class) and applying provided styling to render classes correctly.
- For full data description, refer to the product documentation.

## Data structure highlights
- 10m rasters: Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
- 25m rasters: Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 & 3 = classification confidence indicators.

## Visualization instructions by software

### QGIS
- Add the file to your project; layer appears in the layers panel.
- Double-click the layer name to open Layer properties.
- Select Symbology from the left menu.
- In Render Type, choose Paletted/Unique values.
- In Band, select Band 1.
- Click the style button and choose Load style from the menu.
- Browse to LCMcolours_QGIS.qml provided with the document, select it, and open.
- Click OK to redraw the map with correct classification.

### ArcGIS Desktop
- In Catalog, navigate to the data folder; expand the raster to view its bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Symbology, select Unique Values (if prompted to calculate values, click YES).
- Click Import and load the provided layer file (LCMcolours.lyr).
- Click OK to redraw the map with correct classification.

### ArcGIS Pro
- Open Catalog in your ArcGIS Pro project and navigate to the data folder.
- Expand the file to display raster bands and drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Contents, open Appearance > Symbology.
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Click the hamburger menu in the Symbology panel and choose Import.
- Load the provided layer file (LCMcolours.lyr).
- The map will be redrawn with the correct classification.