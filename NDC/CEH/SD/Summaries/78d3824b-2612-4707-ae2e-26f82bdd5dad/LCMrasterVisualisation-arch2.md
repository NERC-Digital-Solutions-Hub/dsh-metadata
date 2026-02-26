# Visualising UKCEH Land Cover Class using a GIS application

- The Land cover map rasters for 2017-2020 are multiband rasters.
  - 20m and 10m datasets: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m datasets: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence indicators).
- This short guide explains visualising the Land Cover Class data contained in Band 1 using commonly used GIS applications; for a full data description, refer to the product documentation.

## Visualising in QGIS

- Add the file to your project; the layer appears in the layers panel.
- Open layer properties, select Symbology.
- Render type: Paletted/Unique values; Band: Band 1.
- Click the style button, choose Load style from the menu.
- Load the LCMcolours_QGIS.qml file accompanying this document; click Open, then OK.
- The map will be redrawn with the correct classification.

## Visualising in ArcGIS Desktop

- In the Catalogue window, browse to the data folder and expand the raster to display its bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- Symbology tab: choose Unique Values (if prompted to calculate values, click YES).
- Click Import and load the provided LCMcolours.lyr file.
- Click OK; the map will be redrawn with the correct classification.

## Visualising in ArcGIS Pro

- In the project, open the Catalog and browse to the data folder; expand to view raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Contents, select the layer and open Appearance > Symbology.
- Primary symbology: choose Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and choose Import; load the provided LCMcolours.lyr.
- The map will be redrawn with the correct classification.