# Visualising UKCEH Land Cover Class using a GIS application

- Data overview
  - Land cover map rasters for 2017-2020 are multiband rasters.
  - 20m and 10m rasters: two bands
    - Band 1 = UKCEH Land Cover Class identifier
    - Band 2 = classification confidence indicator
  - 25m rasters: three bands
    - Band 1 = dominant UKCEH Land Cover Class identifier
    - Bands 2 and 3 = indicators of classification confidence
- Purpose
  - A short guide for visualising the Land Cover Class data in Band 1 using common GIS applications.
  - For a full data description, refer to the product documentation.

- Visualising in QGIS
  - Add the file to your project; layer appears in the layers panel.
  - Open layer properties → Symbology.
  - Render as Paletted/Unique Values; select Band 1.
  - Use Load style and select LCMcolours_QGIS.qml to redraw with correct classification.

- Visualising in ArcGIS Desktop
  - In Catalog, browse to data folder; expand raster bands.
  - Drag band_1 to the Table of Contents.
  - Layer properties → Symbology tab → Unique Values (confirm if prompted to build attribute table).
  - Import the LCMcolours.lyr file and apply to redraw with correct classification.

- Visualising in ArcGIS Pro
  - Open Catalog in the project; locate data folder and expand raster bands.
  - Drag band_1 to the Table of Contents.
  - Layer properties → Contents → Symbology (Appearance → Symbology).
  - Set to Unique Values; use Import to load LCMcolours.lyr.
  - Map will redraw with correct classification.

- Additional note
  - The LCM colours files accompany these instructions to ensure consistent classification visuals across platforms.

- Outcome for analysts
  - Enables consistent, standardised visualization of environmental land cover classifications for monitoring environmental health and policy performance over time.