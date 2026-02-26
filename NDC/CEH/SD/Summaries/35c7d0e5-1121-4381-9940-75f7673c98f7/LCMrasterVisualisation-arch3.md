# Visualising UKCEH Land Cover Class using a GIS application

- Purpose: A short guide to visualising UKCEH Land Cover Class data in common GIS applications, focusing on band 1 classifications to support interpretation and reporting within environmental monitoring.
- Data overview:
  - Land cover rasters for 2017-2020 are multi-band.
  - 20m and 10m rasters: two bands (Band 1 = Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant Land Cover Class; Bands 2 and 3 = classification confidence).
  - The guide concentrates on visualising band 1; refer to the product documentation for full data descriptions.
- Output and styles:
  - Pre-made style files accompany the guide to ensure consistent classification visuals across platforms:
    - QGIS: LCMcolours_QGIS.qml
    - ArcGIS Desktop/Pro: LCMcolours.lyr
  - Applying these styles yields a map coloured by the Land Cover Class identifiers.

- Visualisation in QGIS:
  - Add the file to your project; layer appears in the Layers panel.
  - Open layer properties > Symbology.
  - Render type: Paletted/Unique Values; Band: Band 1.
  - Use style: Load style, select LCMcolours_QGIS.qml, and apply.
  - The map is redrawn with the correct classification.

- Visualisation in ArcGIS Desktop:
  - In the catalogue, locate the data folder and expand the raster to view bands.
  - Drag band_1 into the Table of Contents.
  - Layer properties > Symbology: choose Unique Values (confirm if prompted to calculate values).
  - Import: load the provided LCMcolours.lyr.
  - Apply to redraw the map with the correct classification.

- Visualisation in ArcGIS Pro:
  - Open catalogue, browse to data folder, expand to view bands.
  - Drag band_1 into the Table of Contents.
  - Layer properties > Symbology: set to Unique Values (build attribute table if prompted).
  - Use the Import option in the Symbology menu to load LCMcolours.lyr.
  - Map is redrawn with the correct classification.

- Additional notes:
  - The document emphasizes using the accompanying style files to achieve consistent visual classification across GIS platforms.
  - For detailed data descriptions, refer to the product documentation.