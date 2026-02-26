# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Short guide to visualize UKCEH Land Cover Class data in GIS applications.
- Data covers land cover rasters for 2017–2020; multi-band rasters have different band configurations by resolution.
- This guide focuses on visualizing band 1 (land cover class identifiers) across common GIS platforms.

## Data structure
- 20m and 10m rasters: two bands
  - Band 1: UKCEH Land Cover Class identifier
  - Band 2: classification confidence indicator
- 25m rasters: three bands
  - Band 1: dominant UKCEH Land Cover Class identifier
  - Bands 2–3: classification confidence indicators
- For full data description, refer to the product documentation.

## Platform-specific visualization

### QGIS
- Add the file to your project; layer appears in the layers panel.
- Right-click layer → Properties → Symbology.
- Render type: Paletted/Unique values; Band: Band 1.
- Click the style/Load style button → load LCMcolours_QGIS.qml → OK.
- Map redraws with correct classification colors.

### ArcGIS Desktop
- In Catalog, locate the data folder; expand raster to view bands.
- Drag band_1 into the Table of Contents.
- Layer properties → Symbology → Unique Values (confirm to build attribute table if prompted).
- Click Import → load LCMcolours.lyr → OK.
- Map redraws with correct classification.

### ArcGIS Pro
- Open catalog, locate data, expand raster to view bands.
- Drag band_1 into the Table of Contents.
- Layer properties → Appearance → Symbology → Unique Values (Yes to build attribute table if prompted).
- Open the hamburger menu in the Symbology panel → Import → load LCMcolours.lyr → OK.
- Map redraws with correct classification.

## Additional notes
- The LCM color style files (LCMcolours_QGIS.qml and LCMcolours.lyr) ensure consistent classification visualization across platforms.
- This guide provides a concise workflow; consult the full product documentation for comprehensive data details.