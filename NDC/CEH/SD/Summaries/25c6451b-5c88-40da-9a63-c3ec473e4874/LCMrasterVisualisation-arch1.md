# Visualising UKCEH Land Cover Class using a GIS application

- Land cover map rasters for 2017-2020 are multiband rasters.
  - 20m and 10m datasets: two bands. Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
  - 25m datasets: three bands. Band 1 = dominant Land Cover Class; Bands 2 and 3 = classification confidence indicators.
- Purpose of this guide: visualise the Land Cover Class data contained in Band 1 using common GIS applications.
- For a full data description, refer to the product documentation.
- Style files accompany the instructions:
  - QGIS: LCMcolours_QGIS.qml
  - ArcGIS: LCMcolours.lyr

## Visualising the data using QGIS
- Add the file to your project; it appears in the layers panel.
- Open layer properties > Symbology.
- Render type: Paletted/Unique Values; Band: Band 1.
- Click Style > Load style, browse to LCMcolours_QGIS.qml, open.
- Click OK to redraw the map with the correct classification.

## Visualising the data using ArcGIS Desktop
- In the Catalogue window, locate the data folder and expand to view raster bands.
- Drag Band 1 (band_1) into the Table of Contents.
- Double-click the layer name to open Layer Properties > Symbology.
- Choose Unique Values (if prompted to calculate values, choose YES).
- Click Import and load LCMcolours.lyr.
- Click OK to redraw the map with the correct classification.

## Visualising the data using ArcGIS Pro
- In the Catalog pane, navigate to the data folder.
- Expand the file to display the raster bands and drag Band 1 (band_1) into the Contents.
- Double-click the layer to open Layer Properties.
- In Contents > Appearance > Symbology, select Unique Values.
- If prompted to build an attribute table, click YES.
- Use the hamburger menu in the Symbology panel and choose Import; load LCMcolours.lyr.
- The map will be redrawn with the correct classification.