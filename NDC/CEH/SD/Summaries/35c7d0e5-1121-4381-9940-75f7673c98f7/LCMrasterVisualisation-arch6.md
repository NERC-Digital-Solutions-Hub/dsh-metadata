# Visualising UKCEH Land Cover Class using a GIS application

- This short guide explains how to visualise the Land Cover Class data contained in band 1 of multi-band land cover rasters (2017–2020) using common GIS applications.
- Data structure:
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2–3 = confidence indicators).
- For full data description, refer to the product documentation.

## Visualization in QGIS

- Add the file to your project; the layer appears in the layers panel.
- Open layer properties → Symbology.
- Render type: Paletted/Unique values; Band: Band 1.
- Click Style → Load style from the menu.
- Load LCMcolours_QGIS.qml, select Open, OK.
- The map redraws with the correct classification.

## Visualization in ArcGIS Desktop

- In the Catalogue, locate the data folder and expand the raster to show its bands.
- Drag band_1 into the Table of Contents.
- Layer properties → Symbology: Unique Values (if prompted to calculate values, click YES).
- Import: load LCMcolours.lyr provided with these instructions.
- OK; the map redraws with the correct classification.

## Visualization in ArcGIS Pro

- Open Catalogue, navigate to the data folder, expand to display raster bands.
- Drag band_1 into the Contents window.
- Layer properties → Appearance → Symbology: Unique values (if prompted, Yes to build attribute table).
- Use the hamburger menu in the Symbology panel → Import; load LCMcolours.lyr.
- The map redraws with the correct classification.