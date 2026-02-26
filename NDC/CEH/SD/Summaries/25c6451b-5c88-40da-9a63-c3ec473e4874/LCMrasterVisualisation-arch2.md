# Visualising UKCEH Land Cover Class using a GIS application

- Purpose
  - Short guide to visualise the Land Cover Class data contained in band 1 using common GIS applications.
  - Data cover 2017–2020 land cover rasters with standardized band structures; see product documentation for full data description.

- Data structure (bands)
  - 20 m and 10 m rasters: two bands
    - Band 1: UKCEH Land Cover Class identifier
    - Band 2: classification confidence indicator
  - 25 m rasters: three bands
    - Band 1: dominant UKCEH Land Cover Class identifier
    - Bands 2 and 3: classification confidence indicators

- Visualization in QGIS
  - Add the file to the project to appear in the layers panel
  - Layer > Properties > Symbology
  - Render type: Paletted/unique values
  - Band: Band 1
  - Style: Load style from LCMcolours_QGIS.qml to apply correct classification

- Visualization in ArcGIS Desktop
  - In Catalog, locate the data folder and expand to reveal raster bands
  - Drag Band_1 into the Table of Contents
  - Layer properties > Symbology
  - Choose Unique Values (if prompted to calculate values, click YES)
  - Import and load LCMcolours.lyr
  - OK to redraw the map with the correct classification

- Visualization in ArcGIS Pro
  - Open Catalog and locate data; expand to view raster bands
  - Drag Band_1 into the Table of Contents
  - Layer properties (Contents) > Symbology
  - Primary: Unique values (if prompted to build an attribute table, click Yes)
  - Use the hamburger menu in the Symbology panel > Import
  - Load LCMcolours.lyr and redraw the map with correct classification

- Additional note
  - For a full data description, refer to the product documentation.