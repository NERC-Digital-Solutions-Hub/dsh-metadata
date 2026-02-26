# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- This document is a short guide for visualising the UKCEH Land Cover Class (LCM) data using common GIS applications.
- Land cover map rasters for 2017–2020 are multi-band:
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2–3 = classification confidence).
- The guide focuses on visualising Band 1; for full data descriptions, refer to the product documentation.
- Style files accompany the instructions to ensure consistent colour mapping (LCMcolours_QGIS.qml for QGIS; LCMcolours.lyr for ArcGIS).

## How to visualize

### Visualising in QGIS
- Add the file to your project; the layer appears in the layers panel.
- Open layer properties and select Symbology.
- In Render type, choose Paletted/Unique values; set Band to Band 1.
- Click Load style and browse to LCMcolours_QGIS.qml, then open.
- Click OK to redraw the map with the correct classification.

### Visualising in ArcGIS Desktop
- In the Catalog window, navigate to the data folder and expand the raster to show its bands.
- Drag Band_1 into the Table of Contents.
- Open the layer properties; go to the Symbology tab and choose Unique Values (accept any prompts to build the attribute table).
- Click Import and load LCMcolours.lyr.
- Click OK to redraw the map with the correct classification.

### Visualising in ArcGIS Pro
- In the Catalog window, navigate to the data folder and expand the raster bands.
- Drag Band_1 into the Table of Contents.
- Open the layer's properties (Contents) and go to Appearance > Symbology; choose Unique Values.
- If prompted to build an attribute table, click Yes.
- Click the hamburger menu in the Symbology panel and choose Import; load LCMcolours.lyr.
- The map will be redrawn with the correct classification.

## Data details (recap)
- 2017–2020 UKCEH Land Cover Class rasters are multi-band:
  - 20m/10m: Band 1 = class identifier; Band 2 = confidence.
  - 25m: Band 1 = dominant class; Bands 2–3 = confidence.

## Governance considerations for Data Stewards
- Use standardized style files (LCMcolours_QGIS.qml, LCMcolours.lyr) to ensure consistent visualization across platforms.
- Ensure Band 1 is used for classification visualization to maintain comparability across datasets and users.
- Document and share the specific style files and any software/version steps to enable reproducibility.
- Note that only Band 1 visualization is described; refer to product documentation for comprehensive data details and metadata.