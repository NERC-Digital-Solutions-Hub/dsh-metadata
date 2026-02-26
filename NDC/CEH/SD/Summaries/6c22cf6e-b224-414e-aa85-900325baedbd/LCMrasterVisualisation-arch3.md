# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Short guide for visualising the UKCEH Land Cover Class (LCM) data in common GIS applications.
- Datasets (land cover rasters) are multi-band:
  - 20m and 10m rasters: two bands (Band 1 = Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant Land Cover Class; Bands 2–3 = confidence indicators).
- Focus is on visualising Band 1; refer to product documentation for full data descriptions.

## Visualising in QGIS
- Add the file to your project; layer appears in the layers panel.
- Open layer properties -> Symbology -> Render type: Paletted/Unique Values -> Band: Band 1.
- Click style -> Load style from the menu.
- Browse to LCMcolours_QGIS.qml (supplied with the document), select and open.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Desktop
- In the Catalog window, locate the data folder and expand the raster to view its bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties -> Symbology tab.
- Choose Unique Values (if prompted to calculate values, click YES).
- Click Import -> load LCMcolours.lyr (provided with these instructions).
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro
- Open the Catalogue window in ArcGIS Pro and locate the data folder.
- Expand the raster to view its bands; drag band_1 into the Table of Contents.
- Double-click the layer in the Contents window to open Layer Properties.
- Select the layer and open Symbology (Appearance > Symbology).
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and choose Import, then load LCMcolours.lyr.
- The map will be redrawn with the correct classification.

## Data and governance notes
- Style files (LCMcolours_QGIS.qml and LCMcolours.lyr) are provided to standardize visualization.
- For full data descriptions and metadata, refer to the accompanying product documentation.
- The process supports reproducible visual outputs aligned with monitoring/framework reporting needs.