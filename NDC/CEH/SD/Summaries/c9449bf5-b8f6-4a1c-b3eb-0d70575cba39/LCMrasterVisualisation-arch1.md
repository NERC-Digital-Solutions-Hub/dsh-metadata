# Visualising UKCEH Land Cover Class using a GIS application

## Overview of the data
- Land Cover Map rasters come in different resolutions:
  - 20m and 10m: two bands — Band 1 is the UKCEH Land Cover Class identifier; Band 2 is a classification confidence indicator.
  - 25m: three bands — Band 1 is the dominant Land Cover Class identifier; Bands 2 and 3 are confidence indicators.
- The guide focuses on visualising the Land Cover Class data contained in Band 1.
- For a full data description, refer to the product documentation.

## Purpose of the guide
- A short, practical guide to visualising Band 1 Land Cover Class data using common GIS applications.
- Style files needed for correct visualization are provided with the instructions.

## Visualising in QGIS
- Add the file to your project; the layer appears in the layers panel.
- Open the layer properties and select Symbology.
- Set render type to Paletted/Unique Values; select Band 1.
- Load the style from LCMcolours_QGIS.qml, then OK.
- The map will redraw with the correct classification.

## Visualising in ArcGIS Desktop
- In the Catalog window, navigate to the data folder and expand the raster’s bands.
- Drag band_1 into the Table of Contents.
- Open the layer properties and go to the Symbology tab; choose Unique Values.
- If prompted to build the attribute table, click Yes.
- Click Import and load LCMcolours.lyr provided with the instructions.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro
- Open the Catalog and browse to the data folder; expand to display the raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open layer properties.
- In Contents > Appearance > Symbology, choose Unique Values.
- If prompted to build an attribute table, click Yes.
- Use the hamburger menu in the symbology panel and choose Import.
- Load LCMcolours.lyr; the map will redraw with the correct classification.

## Additional notes
- The provided style files (LCMcolours_QGIS.qml and LCMcolours.lyr) accompany these instructions.
- This guide is specifically for visualising the Band 1 Land Cover Class data; refer to the product documentation for full data details.