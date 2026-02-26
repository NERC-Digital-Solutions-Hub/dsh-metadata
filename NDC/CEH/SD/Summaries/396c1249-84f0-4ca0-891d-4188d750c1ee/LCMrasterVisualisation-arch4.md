# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover map rasters for 2017–2020 are multiband rasters.
- Raster band structure by resolution:
  - 20 m and 10 m: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25 m: three bands (Band 1 = dominant Land Cover Class identifier; Bands 2–3 = classification confidence).
- The document is a short guide for visualising the Land Cover Class data in Band 1 using common GIS applications; full data description is in the product documentation.

## Visualising the data by GIS platform

- QGIS
  - Add the file to the project; layer appears in the layers panel.
  - Open layer properties > Symbology.
  - Render type: Paletted/Unique values; Band: Band 1.
  - Load style from LCMcolours_QGIS.qml; apply and redraw the map to show correct classification.

- ArcGIS Desktop
  - In the Catalog, locate the data folder and expand to see the raster bands.
  - Drag band_1 into the Table of Contents.
  - Layer properties > Symbology: Unique Values.
  - If prompted to build an attribute table, select Yes; Import the LCMcolours.lyr style file; apply to redraw the map with correct classification.

- ArcGIS Pro
  - In the Catalog, open the folder and expand the raster bands; drag band_1 into the Table of Contents.
  - Layer properties > Symbology: Primary option = Unique Values.
  - Use the Import option from the hamburger menu in the Symbology panel; load LCMcolours.lyr.
  - The map is redrawn with the correct classification.

## Additional notes
- Style files provided: LCMcolours_QGIS.qml for QGIS and LCMcolours.lyr for ArcGIS Desktop/Pro.
- For a full description of the data, refer to the product documentation.