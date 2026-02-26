# Visualising UKCEH Land Cover Class using a GIS application

- This document is a short guide for visualising Land Cover Class data contained in band 1 of land cover rasters for 2017–2020.
- Raster specifics:
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant Land Cover Class identifier; Bands 2–3 = classification confidence).
- For a full description of the data, refer to the product documentation.

## Data structure and purpose

- Band 1 contains the class identifiers used for visualization.
- Bands 2 and 3 (where present) provide indicators of classification confidence.
- The guide focuses on visualising the Band 1 classifications using common GIS applications.

## Visualising the data using QGIS

- Add the file to your project; it will appear in the layers panel.
- Open layer properties > Symbology.
- In Render type, select Paletted/unique values; set Band to Band 1.
- Load the provided style: LCMcolours_QGIS.qml; select it and apply.
- The map will redraw with the correct classification.

## Visualising the data using ArcGIS Desktop

- In the Catalog, locate the data folder and expand the raster to show its bands.
- Drag Band_1 into the Table of Contents.
- Open layer properties > Symbology.
- Choose Unique Values (if prompted to calculate values, click YES).
- Use Import to load the accompanying style: LCMcolours.lyr.
- Apply; the map will redraw with the correct classification.

## Visualising the data using ArcGIS Pro

- In the Catalog, locate the data folder and expand the raster’s bands.
- Drag Band_1 into the Table of Contents.
- Open layer properties (Contents) and go to Appearance > Symbology.
- In Primary Symbology select Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and choose Import; load LCMcolours.lyr.
- The map will redraw with the correct classification.