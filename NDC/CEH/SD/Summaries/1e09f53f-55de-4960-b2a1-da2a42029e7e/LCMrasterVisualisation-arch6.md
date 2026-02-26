# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Purpose: Visualise the Land Cover Class data contained in band 1 of UKCEH Land Cover Map rasters.
- Band structure:
  - 20m and 10m rasters: two bands — Band 1 = Land Cover Class identifier; Band 2 = classification confidence.
  - 25m rasters: three bands — Band 1 = dominant Land Cover Class identifier; Bands 2–3 = classification confidence.
- For full data description, refer to the product documentation.

## Visualising in QGIS
- Add the file to your project; the layer appears in the layers panel.
- Layer properties > Symbology.
- Render type: Paletted/Unique values; Band: Band 1.
- Click the style button > Load style from the menu.
- Load LCMcolours_QGIS.qml provided with the document; open.
- OK → map redraws with correct classification.

## Visualising in ArcGIS Desktop
- In the Catalogue window, locate the data folder and expand to the raster’s bands.
- Drag Band_1 into the Table of Contents.
- Layer properties > Symbology.
- Unique Values; if prompted to calculate values, click YES.
- Click Import and load LCMcolours.lyr provided with these instructions.
- OK → map redraws with correct classification.

## Visualising in ArcGIS Pro
- Open the Catalogues window; locate the data folder, expand to the raster’s bands.
- Drag Band_1 into the Table of Contents.
- Layer name > open layer properties; Symbology (Appearance > Symbology).
- Primary Symbology: Unique values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel > Import.
- Load LCMcolours.lyr provided with the instructions; map redraws with correct classification.