# Visualising UKCEH Land Cover Class using a GIS application

- This is a short guide for visualising the UKCEH Land Cover Class data (band 1) in common GIS applications. For full data description, refer to the product documentation.
- Data characteristics:
  - 20m and 10m rasters: two bands (band 1 = Land Cover Class identifier; band 2 = classification confidence).
  - 25m rasters: three bands (band 1 = dominant Land Cover Class; bands 2 and 3 = classification confidence).
- The document provides practical steps to display the band 1 classifications correctly using accompanying style files. These tools help users quickly explore and interpret land cover data.

## Visualization in QGIS

- Add the data to your project; it will appear in the layers panel.
- Open layer properties > Symbology > Render type: Paletted/Unique values > Band: Band 1.
- Click the style button > Load style from the menu.
- Load the accompanying LCMcolours_QGIS.qml file and apply it.
- The map will be redrawn with the correct classification colors.

## Visualization in ArcGIS Desktop

- In the Catalog, locate the data folder and expand the raster to show its bands.
- Drag band_1 into the Table of Contents; open layer properties.
- Symbology tab > choose Unique Values (if prompted to build an attribute table, say Yes).
- Use Import to load the provided LCMcolours.lyr file.
- Apply and the map will reflect the correct classification.

## Visualization in ArcGIS Pro

- Open Catalog and locate the data folder; expand to view raster bands.
- Drag band_1 into the Table of Contents.
- Open layer properties > Appearance > Symbology; select Unique Values (if prompted to build an attribute table, say Yes).
- Use the hamburger menu in the symbology panel > Import.
- Load the provided LCMcolours.lyr file; the map will redraw with the correct classification.