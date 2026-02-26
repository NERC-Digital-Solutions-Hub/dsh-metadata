# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Short guide to visualizing Land Cover Class data (band 1) from UKCEH land cover rasters (2017–2020) using common GIS applications.
- For a full data description, refer to the product documentation.
- Visualizations aim to display standardized Land Cover Class classifications consistently across datasets and tools.

## Data structure
- 20m and 10m rasters: two bands
  - Band 1: UKCEH Land Cover Class identifier
  - Band 2: classification confidence indicator
- 25m rasters: three bands
  - Band 1: dominant UKCEH Land Cover Class identifier
  - Bands 2–3: indicators of classification confidence

## Visualization workflow by GIS

### QGIS
- Add the file to your project; the layer appears in the layers panel.
- Layer properties > Symbology: set render type to Paletted/unique values and select Band 1.
- Load style from LCMcolours_QGIS.qml; apply to redraw the map with correct classification.

### ArcGIS Desktop
- In Catalog, locate the data folder, expand to view raster bands.
- Drag band_1 into the Table of Contents; open layer properties > Symbology > Unique Values.
- Import LCMcolours.lyr; apply to redraw the map with correct classification.

### ArcGIS Pro
- Open the Catalog, browse to the data folder, expand to view raster bands.
- Drag band_1 into the Table of Contents; open layer properties > Appearance > Symbology.
- Choose Unique values; use the hamburger menu to Import LCMcolours.lyr; map redraws with correct classification.

## Resources
- LCMcolours_QGIS.qml (color style for QGIS)
- LCMcolours.lyr (color style for ArcGIS)

## Notes
- This guide focuses on visualizing band 1; refer to product documentation for full data description.
- The instructions support consistent, cross-platform visualization to aid environmental monitoring and policy evaluation.