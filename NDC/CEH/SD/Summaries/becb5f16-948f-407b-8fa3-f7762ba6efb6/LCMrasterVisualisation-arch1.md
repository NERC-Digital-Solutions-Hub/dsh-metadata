# Visualising UKCEH Land Cover Class using a GIS application

- Overview of data structure:
  - 20m and 10m rasters: two bands
    - Band 1: UKCEH Land Cover Class identifier
    - Band 2: classification confidence indicator
  - 25m rasters: three bands
    - Band 1: dominant UKCEH Land Cover Class identifier
    - Bands 2–3: classification confidence indicators
  - Full data description available in the product documentation

- Purpose:
  - Short guide to visualising Land Cover Class data contained in band 1 using common GIS applications

- Color styles and reproducibility:
  - Use accompanying style files to ensure correct classification display
    - QGIS: LCMcolours_QGIS.qml
    - ArcGIS: LCMcolours.lyr

- Visualising in QGIS:
  - Add the file to your project
  - In Layer properties > Symbology:
    - Render type: Paletted/Unique Values
    - Band: Band 1
  - Load style: LCMcolours_QGIS.qml
  - OK to redraw with correct classification

- Visualising in ArcGIS Desktop:
  - Locate data folder and expand the raster
  - Drag band_1 into Table of Contents
  - Layer properties > Symbology:
    - Type: Unique Values
    - If prompted to build table, choose YES
  - Import: load LCMcolours.lyr
  - OK to redraw with correct classification

- Visualising in ArcGIS Pro:
  - Open Catalogues and navigate to data folder
  - Expand raster and drag band_1 into Table of Contents
  - Layer properties > Appearance > Symbology:
    - Primary options: Unique Values
  - Open hamburger menu in Symbology and Import
  - Load LCMcolours.lyr and redraw the map

- Additional guidance:
  - This guide focuses on Band 1; refer to product documentation for full data description
  - Ensure data sources and metadata are documented for reproducibility and reuse