# Visualising UKCEH Land Cover Class using a GIS application

- Data structure overview
  - Land Cover Map rasters are multi-band.
  - 20m and 10m rasters: two bands
    - Band 1 = UKCEH Land Cover Class identifier
    - Band 2 = classification confidence indicator
  - 25m rasters: three bands
    - Band 1 = dominant UKCEH Land Cover Class identifier
    - Bands 2–3 = classification confidence indicators
  - This guide focuses on visualizing the Land Cover Class data contained in Band 1
  - For full data description, refer to the product documentation

- Visualisation workflow (general)
  - Use the accompanying style files to ensure correct colour mapping
  - The workflow differs slightly by GIS application but all aim to display Band 1 classifications with a predefined colour style

- Visualising the data using QGIS
  - Add the file to your project; layer appears in the layers panel
  - Open layer properties and select Symbology
  - Render as Paletted/Unique Values; Band = Band 1
  - Click Style > Load style from the menu
  - Load LCMcolours_QGIS.qml and open
  - OK; map will redraw with correct classification

- Visualising the data using ArcGIS Desktop
  - In Catalog, locate the data folder; expand to view raster bands
  - Drag band_1 into the Table of Contents
  - Open layer properties and go to the Symbology tab
  - Choose Unique Values (if prompted to build an attribute table, click Yes)
  - Click Import and load LCMcolours.lyr provided with these instructions
  - OK; map will redraw with correct classification

- Visualising the data using ArcGIS Pro
  - In the project, open the Catalog pane and browse to the data folder
  - Expand to display raster bands; drag band_1 into the Table of Contents
  - Open layer properties (Appearance > Symbology)
  - In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes)
  - Use the hamburger menu in the Symbology panel and choose Import
  - Load LCMcolours.lyr provided with these instructions
  - Map will redraw with correct classification

- Additional notes
  - This guide accompanies the data; for a full description, consult the product documentation