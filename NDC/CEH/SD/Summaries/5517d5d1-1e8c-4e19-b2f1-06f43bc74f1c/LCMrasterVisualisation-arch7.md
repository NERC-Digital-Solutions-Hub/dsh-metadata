# Visualising UKCEH Land Cover Class using a GIS application

## Data overview
- Land cover map rasters for 2017-2020 are multi-band rasters.
  - 20m and 10m rasters: two bands. Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence indicator.
  - 25m rasters: three bands. Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = confidence indicators.
- This document is a short guide for visualising the land cover data contained in Band 1 using common GIS applications; refer to product documentation for full data description.

## Intended use
- Provide a practical, map-based visualization workflow for GIS users to view and interpret Land Cover Class data.

## Visualising in QGIS
- Add the file to your project; the layer appears in the layers panel.
- Open Layer Properties > Symbology.
- Set Render type to Paletted/Unique values; Band to Band 1.
- Click Style > Load Style from the menu.
- Browse to LCMcolours_QGIS.qml accompanying this document, select it, and open.
- Click OK; the map redraws with the correct classification.

## Visualising in ArcGIS Desktop
- In the Catalog window, browse to the data folder and expand the raster to display its bands.
- Drag Band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties > Symbology.
- Choose Unique Values (if prompted to calculate values, click YES).
- Click Import and load the provided LCMcolours.lyr file.
- Click OK; the map redraws with the correct classification.

## Visualising in ArcGIS Pro
- In your ArcGIS Pro project, open the Catalog window and browse to the data folder.
- Expand the file to display the raster bands; drag Band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties; under Contents, open Symbology.
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Open the hamburger menu in the Symbology panel and choose Import; load LCMcolours.lyr.
- The map will be redrawn with the correct classification.

## Notes
- For a full description of the data, refer to the product documentation.
- The workflow focuses on visualising Band 1; confidence indicators are available in other bands but are not required for these visuals.