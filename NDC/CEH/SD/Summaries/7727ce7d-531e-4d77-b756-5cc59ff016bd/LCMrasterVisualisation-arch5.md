# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land Cover Map rasters come in multiple resolutions with different band structures:
  - 20m and 10m: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m: three bands (Band 1 = dominant Land Cover Class; Bands 2-3 = classification confidence indicators).
- This guide covers visualizing the Land Cover Class data using Band 1 in common GIS applications. For full data descriptions, refer to the product documentation.

## Visualisation workflow by GIS application

### QGIS
- Add the file to your project; it will appear in the layers panel.
- Open Layer Properties for the layer and select Symbology.
- In Render type, choose Paletted/Unique Values; set Band to Band 1.
- Click the style button, choose Load style, and select LCMcolours_QGIS.qml that accompanies these instructions.
- Click OK to redraw the map with the correct classification.

### ArcGIS Desktop
- In the Catalog window, locate the folder containing the data and expand the raster to view its bands.
- Drag band_1 into the Table of Contents.
- Open layer properties for the layer and go to Symbology; choose Unique Values (if prompted to build an attribute table, click Yes).
- Click Import and load the provided LCMcolours.lyr file.
- Click OK to redraw the map with the correct classification.

### ArcGIS Pro
- Open the Catalog, browse to the folder with the data, and expand the raster to view its bands.
- Drag band_1 into the Table of Contents.
- Open the layer's properties (Contents > Symbology).
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and select Import; load LCMcolours.lyr.
- The map will be redrawn with the correct classification.

## Reference style files
- LCMcolours_QGIS.qml (for QGIS)
- LCMcolours.lyr (for ArcGIS Desktop/Pro)

## Governance and reproducibility considerations
- The visualization relies on consistent color mapping provided by the style files; ensure the correct style file accompanies the dataset.
- Document the GIS workflow used to visualize Band 1 for reproducibility across teams.
- Refer to the product documentation for full data descriptions and metadata to support data stewardship and discovery.