# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Short guide for visualising UKCEH Land Cover Class data contained in band 1 of land cover raster datasets (2017–2020).
- Data structure: 20m and 10m rasters are 2-band (Band 1: Land Cover Class, Band 2: classification confidence); 25m rasters are 3-band (Band 1: dominant Land Cover Class, Bands 2–3: classification confidence).
- For full data description, refer to the product documentation.

## Data considerations
- Visualisation focuses on band 1 (the classification).
- Confidence bands (2 and 3, where present) indicate classification certainty but are not required for the primary visualisation step.
- Style files accompany the instructions to ensure consistent colour-coding across platforms.

## Visualization workflow by software

### Visualising the data using QGIS
- Add the file to your project; it will appear in the layers panel.
- Open layer properties, choose Symbology.
- Render as Paletted/Unique Values using Band 1.
- Load the style from LCMcolours_QGIS.qml to apply the correct classification colours.
- Map will redraw with the correct classification.

### Visualising the data using ArcGIS Desktop
- In the Catalogue, locate the raster folder and expand to view bands.
- Drag Band 1 into the Table of Contents.
- Open layer properties, go to Symbology, select Unique Values (confirm to build attribute table if prompted).
- Use Import to load LCMcolours.lyr provided with the instructions.
- Map will redraw with the correct classification.

### Visualising the data using ArcGIS Pro
- Open the Catalog, locate the data folder, and expand the raster bands.
- Drag Band 1 into the Table of Contents.
- Open layer properties, then Appearance > Symbology.
- Choose Unique Values (Yes to build attribute table if prompted).
- Use the Import option in the symbology panel to load LCMcolours.lyr.
- Map will redraw with the correct classification.

## Additional notes
- The colour styles (LCMcolours_QGIS.qml and LCMcolours.lyr) are provided with these instructions to ensure standardised visuals.
- This guide is intended for common GIS applications to support consistent monitoring visuals; refer to product documentation for full data descriptions.