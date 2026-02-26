# Visualising UKCEH Land Cover Class using a GIS application

- Purpose: A short guide to visualise the Land Cover Class data (band 1) from UKCEH Land Cover Map rasters in common GIS software.
- Data structure:
  - 20 m and 10 m rasters: two bands — band 1 = Land Cover Class identifier; band 2 = classification confidence.
  - 25 m rasters: three bands — band 1 = dominant Land Cover Class; bands 2–3 = classification confidence indicators.
- Scope: Focuses on visualising band 1; refer to the full product documentation for complete data descriptions.
- Colour styles: Uses companion style files to ensure correct classification colours:
  - QGIS: LCMcolours_QGIS.qml
  - ArcGIS (Desktop/Pro): LCMcolours.lyr

- Visualising the data using QGIS
  - Add the file to your project; layer appears in the layers panel.
  - Open layer properties → Symbology.
  - Render type: Paletted/unique values; Band: Band 1.
  - Click Style → Load style from LCMcolours_QGIS.qml; select OK.
  - Map redraws with correct classification.

- Visualising the data using ArcGIS Desktop
  - In Catalog, locate the data folder, expand to view raster bands.
  - Drag band_1 into the Table of Contents.
  - Layer properties → Symbology → Unique Values (if prompted to build attribute table, Yes).
  - Click Import → load LCMcolours.lyr provided with these instructions.
  - Click OK to redraw the map with correct classification.

- Visualising the data using ArcGIS Pro
  - In a project, open Catalog and browse to the data folder.
  - Expand to display the raster bands; drag band_1 into the Table of Contents.
  - Layer properties (Contents) → Appearance → Symbology; select Unique Values.
  - Use the hamburger menu in the Symbology panel → Import; load LCMcolours.lyr.
  - Map will be redrawn with the correct classification.