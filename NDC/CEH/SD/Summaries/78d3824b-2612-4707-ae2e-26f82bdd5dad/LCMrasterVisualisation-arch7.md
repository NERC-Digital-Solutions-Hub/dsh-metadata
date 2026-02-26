# Visualising UKCEH Land Cover Class using a GIS application

- Overview
  - The document provides a short guide to visualising UKCEH Land Cover Class data (contained in band 1) using common GIS applications.
  - Data specifics: land cover rasters for 2017-2020; 20m/10m rasters have two bands (Band 1 = Land Cover Class identifier; Band 2 = classification confidence). 25m rasters have three bands (Band 1 = dominant Land Cover Class identifier; Bands 2–3 = classification confidence indicators).
  - For a full data description, refer to the product documentation.

- Data structure to visualise
  - Visualisation focuses on Band 1 containing the Land Cover Class identifier.
  - Band structures:
    - 20m/10m: Band 1 = class ID; Band 2 = confidence.
    - 25m: Band 1 = dominant class ID; Bands 2 & 3 = confidence indicators.

- General workflow for visualisation
  - Use Band 1 to create the map visualisation.
  - The document is a quick guide for common GIS applications; refer to the product documentation for full details.

- Visualising in QGIS
  - Add the file to the project; layer appears in the layers panel.
  - Layer properties → Symbology → Render type: Paletted/Unique values; Band: Band 1.
  - Click style → Load style from the provided file LCMcolours_QGIS.qml → OK.
  - Map will redraw with correct classification.

- Visualising in ArcGIS Desktop
  - In Catalog, locate the data folder; expand the raster to view bands.
  - Drag Band 1 into the Table of Contents.
  - Layer properties → Symbology → Unique Values (confirm value table if prompted).
  - Click Import and load LCMcolours.lyr provided with the instructions.
  - OK to redraw the map with correct classification.

- Visualising in ArcGIS Pro
  - Open in Catalog, locate the data folder, expand to view bands, drag Band 1 into the Table of Contents.
  - Layer properties → Contents → Appearance → Symbology.
  - Primary Symbology: Unique Values (build attribute table if prompted).
  - Open the hamburger menu in the Symbology panel → Import → load LCMcolours.lyr.
  - Map will redraw with the correct classification.