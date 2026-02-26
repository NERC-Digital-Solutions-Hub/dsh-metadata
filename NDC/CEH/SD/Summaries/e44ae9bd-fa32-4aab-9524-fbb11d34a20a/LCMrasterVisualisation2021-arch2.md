# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Short guide for visualising Land Cover Class (band 1) from the 2021 Land cover map raster data products.
- 10m rasters have two bands: Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
- 25m rasters have three bands: Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence.
- For a full data description, refer to the product documentation.

## Data details
- Band 1 holds the land cover class classification used for visualisation.
- Bands 2 and 3 (in 25m rasters) provide confidence indicators to accompany the dominant class.

## Visualising the data using QGIS
- Add the file to your project; the layer appears in the layers panel.
- Open Layer Properties for the layer; go to Symbology.
- In Render type, choose Paletted/Unique Values; set Band to Band 1.
- Click Style and choose Load style from the menu.
- Load the accompanying LCMcolours_QGIS.qml file and apply; the map redraws with the correct classification.

## Visualising the data using ArcGIS Desktop
- In the Catalog, locate the data folder and expand the file to display raster bands.
- Drag band_1 into the Table of Contents.
- Open the layer’s properties; select Symbology.
- Choose Unique Values; if prompted to build an attribute table, click Yes.
- Click Import and load the provided LCMcolours.lyr file; the map redraws with correct classification.

## Visualising the data using ArcGIS Pro
- In the Catalog, navigate to the data folder and expand the raster bands.
- Drag band_1 into the Table of Contents.
- Open the layer's properties (Appearance > Symbology).
- In Primary Symbology, choose Unique Values; if prompted to build an attribute table, click Yes.
- Use the hamburger menu in the Symbology panel to Import; load the LCMcolours.lyr file; the map redraws with correct classification.

## Additional notes
- The LCMcolours style files accompany these instructions and ensure consistent classification visuals across GIS platforms.