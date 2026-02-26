# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Short guide for visualising the UKCEH Land Cover Class data in common GIS applications.
- Data covers 2017–2020 land cover rasters with band structures varying by resolution:
  - 20m and 10m rasters: two bands (Band 1 = Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant Land Cover Class identifier; Bands 2–3 = confidence indicators).
- Focus is on visualising Band 1 classifications; refer to the product documentation for full data descriptions.

## Data structure and interpretation
- Band 1 contains the primary Land Cover Class identifiers.
- Band 2 (and Band 3 for 25m) provide indicators of classification confidence.
- Full data details available in the accompanying product documentation.

## Visualization workflow by GIS platform

### Visualising with QGIS
- Add the Land Cover raster to your project.
- In Layers panel, double-click the layer name to open its properties.
- Choose Symbology > Paletted/unique values.
- In Band, select Band 1.
- Use the style option: Load style from the LCMcolours_QGIS.qml file provided with these instructions.
- Click OK to redraw the map with correct classifications.

### Visualising with ArcGIS Desktop
- In the Catalog window, locate the data folder and expand the raster to view its bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties, then select the Symbology tab.
- Choose Unique Values as the Symbology type.
- If prompted to build an attribute table, click YES.
- Click Import and load the provided LCMcolours.lyr file.
- Click OK to redraw the map with correct classifications.

### Visualising with ArcGIS Pro
- In the Catalog, locate the data folder and expand the raster to view its bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Contents > Appearance > Symbology, choose Unique Values.
- If prompted to build an attribute table, click Yes.
- Open the Symbology panel menu (hamburger) and choose Import.
- Load the provided LCMcolours.lyr file.
- The map will be redrawn with the correct classification.