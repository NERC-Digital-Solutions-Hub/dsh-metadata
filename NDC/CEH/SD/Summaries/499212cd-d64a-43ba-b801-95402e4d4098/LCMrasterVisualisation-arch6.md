# Visualising UKCEH Land Cover Class using a GIS application

- Purpose: A short guide for visualising UKCEH Land Cover Class data in common GIS applications, focusing on band 1. Encourages self-serve visualization and points to full product documentation for detailed data descriptions.
- Data structure:
  - Land cover rasters for 2017–2020 are multiband.
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant class; Bands 2–3 = classification confidence indicators).

- Visualising in QGIS:
  - Add file to project; open layer properties.
  - Set Render type to Paletted/Unique Values; Band 1.
  - Click Style > Load style from LCMcolours_QGIS.qml provided with this document.
  - OK to redraw the map with correct classification.

- Visualising in ArcGIS Desktop:
  - Browse to data folder in Catalog; display raster bands.
  - Drag Band_1 into Table of Contents; open layer properties.
  - Symbology > Unique Values; (if prompted) yes to build attribute table.
  - Click Import and load LCMcolours.lyr; OK to redraw the map with correct classification.

- Visualising in ArcGIS Pro:
  - Open Catalog; locate data folder; display raster bands.
  - Drag Band_1 into Table of Contents; open layer properties.
  - Contents > Appearance > Symbology; choose Unique Values.
  - Use the hamburger menu in the Symbology panel > Import; load LCMcolours.lyr; map redraws with correct classification.

- Notes:
  - The LCMcolours files accompanying this document provide the necessary styling to display the classifications accurately.
  - For full data descriptions, refer to the product documentation.