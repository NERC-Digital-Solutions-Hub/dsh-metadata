# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover rasters for 2017-2020 are multiband datasets.
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 & 3 = classification confidence).
- This document is a short guide for visualising the Band 1 data in common GIS applications.
- For a full data description, refer to the product documentation.

## Supported GIS applications and workflow

### QGIS
- Add the file to your project; layer appears in the layers panel.
- Open layer properties > Symbology > render type: Paletted/Unique Values; band: Band 1.
- Use the Load style option and load the accompanying LCMcolours_QGIS.qml.
- The map is redrawn with the correct classification.

### ArcGIS Desktop
- In Catalog, locate the data folder, expand the raster bands, and drag band_1 into the Table of Contents.
- Layer properties > Symbology > Unique Values (if prompted to build an attribute table, click Yes).
- Use Import to load the provided LCMcolours.lyr.
- The map is redrawn with the correct classification.

### ArcGIS Pro
- Open Catalog, locate the data folder, expand the raster bands, drag band_1 into the Map contents.
- Layer properties > Symbology: set to Unique Values (if prompted to build an attribute table, click Yes).
- Use the Import option in the Symbology panel to load LCMcolours.lyr.
- The map is redrawn with the correct classification.

## Outputs and usage
- Visualisation produces a map showing the Land Cover Class classification (Band 1) with the intended color scheme.
- Style files required: LCMcolours_QGIS.qml (QGIS) and LCMcolours.lyr (ArcGIS variants).

## Additional notes
- This is a concise guide; refer to the product documentation for comprehensive data details.