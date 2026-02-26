# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover map raster data products for 2021 are multiband rasters.
- 10m rasters: two bands. Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
- 25m rasters: three bands. Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2–3 = classification confidence.
- This short guide covers visualising the Land Cover Class data contained in Band 1.
- For full data description, refer to the product documentation.

## Visualising in QGIS

- Add the file to your project; the data will appear in the layers panel.
- Double-click the layer name to open Layer Properties; choose Symbology from the left.
- In Render type, select Paletted/Unique Values.
- In Band, choose Band 1.
- Click the Style button and choose Load Style from the menu.
- Browse to LCMcolours_QGIS.qml that accompanies this document, select it, and open.
- Click OK; the map will be redrawn with the correct classification.

## Visualising in ArcGIS Desktop

- In the Catalogue window, browse to the folder where the data is stored.
- Expand the file to display the raster’s bands.
- Drag Band_1 into the Table of Contents.
- Double-click the layer name to open the Layer Properties; select the Symbology tab.
- Choose Unique Values as the Symbology type (if prompted to calculate values, click YES).
- Click the Import button and load the provided LCMcolours.lyr.
- Click OK; the map will be redrawn with the correct classification.

## Visualising in ArcGIS Pro

- In your ArcGIS Pro project, open the Catalog and browse to the data folder.
- Expand to display the raster’s bands; drag Band_1 into the Table of Contents.
- Double-click the layer name to open the Layer Properties.
- In the Contents window, select the layer and open Symbology (Appearance > Symbology).
- In the primary Symbology options, choose Unique Values (if prompted to build an attribute table, click Yes).
- Click the hamburger menu in the Symbology panel and choose Import.
- Load the provided LCMcolours.lyr; the map will be redrawn with the correct classification.