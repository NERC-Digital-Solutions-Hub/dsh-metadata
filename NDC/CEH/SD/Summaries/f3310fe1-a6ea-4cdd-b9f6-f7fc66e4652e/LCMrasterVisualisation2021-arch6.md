# Visualising UKCEH Land Cover Class using a GIS application

- Data context
  - Land cover map raster data products for 2021
  - 10m rasters: two bands
    - Band 1 = UKCEH Land Cover Class identifier
    - Band 2 = classification confidence
  - 25m rasters: three bands
    - Band 1 = dominant UKCEH Land Cover Class identifier
    - Bands 2–3 = classification confidence indicators
  - This guide focuses on visualising the Land Cover Class data contained in Band 1
  - For full data description, refer to the product documentation

- Visualization goal
  - Create clear, consistent visualizations of Land Cover Class data across GIS platforms
  - Use provided color styles to ensure accurate and shareable classification

- Required styling files
  - QGIS: LCMcolours_QGIS.qml
  - ArcGIS (Desktop/Pro): LCMcolours.lyr

- Visualising with QGIS
  - Add the data file to your QGIS project; layer appears in the layers panel
  - Layer → Layer properties → Symbology
  - Render type: Paletted/unique values
  - Band: Band 1
  - Click the style button → Load style from file
  - Browse to LCMcolours_QGIS.qml → Open
  - OK to redraw with the correct classification

- Visualising with ArcGIS Desktop
  - In the Catalog, locate the data folder and expand the raster to show its bands
  - Drag Band_1 into the Table of Contents
  - Layer Properties → Symbology
  - Choose Unique Values (if prompted to build an attribute table, click YES)
  - Click Import and load LCMcolours.lyr
  - OK to redraw with the correct classification

- Visualising with ArcGIS Pro
  - Open Catalog and browse to the data folder
  - Expand the raster to display its bands and drag Band_1 into the Table of Contents
  - Layer (in Contents) → Appearance → Symbology
  - Primary symbology: Unique values (if prompted to build an attribute table, click Yes)
  - Open the hamburger menu in the Symbology panel → Import
  - Load LCMcolours.lyr
  - Map redraws to show the correct classification

- Practical notes
  - The steps enable consistent, self-serve visualization of Land Cover Class data across GIS platforms
  - Use the provided style files to ensure colors and categories align with the official classification
  - If needed, refer to the full product documentation for additional data details and context