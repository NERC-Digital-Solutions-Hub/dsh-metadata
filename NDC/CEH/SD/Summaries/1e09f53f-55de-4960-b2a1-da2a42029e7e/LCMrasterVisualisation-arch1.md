# Visualising UKCEH Land Cover Class using a GIS application

- The Land Cover Map rasters are multi-band: 20m and 10m rasters have two bands (Band 1 = Land Cover Class identifier; Band 2 = classification confidence); 25m rasters have three bands (Band 1 = dominant class; Bands 2–3 = classification confidence).
- This guide focuses on visualising the data contained in Band 1.
- For full data descriptions, refer to the product documentation.
- Visuals rely on pre-made color/style files to ensure consistent classification: LCMcolours_QGIS.qml for QGIS and LCMcolours.lyr for ArcGIS.

## Visualising the data using QGIS

- Add the file to the project; layer appears in the layers panel.
- Open layer properties > Symbology.
- Render type: Paletted/Unique values; Band: Band 1.
- Click Style > Load style, browse to LCMcolours_QGIS.qml, open, OK.
- The map redraws with the correct classification.

## Visualising the data using ArcGIS Desktop

- In Catalog, browse to the data folder; expand to display raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties > Symbology.
- Choose Unique Values (if prompted to calculate values, click YES).
- Click Import and load LCMcolours.lyr; OK.
- The map redraws with the correct classification.

## Visualising the data using ArcGIS Pro

- In the Catalog, browse to the data folder and expand to display raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties; in Contents, open Appearance > Symbology.
- Primary symbology: Unique values (if prompted to build an attribute table, click Yes).
- Open the hamburger menu in the Symbology panel and choose Import; load LCMcolours.lyr.
- The map redraws with the correct classification.