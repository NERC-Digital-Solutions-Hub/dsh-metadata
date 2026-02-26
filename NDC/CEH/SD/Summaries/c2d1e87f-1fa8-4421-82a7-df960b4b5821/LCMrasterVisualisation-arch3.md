# Visualising UKCEH Land Cover Class using a GIS application

- Land Cover Map rasters come in different resolutions and band configurations:
  - 20 m and 10 m rasters: two bands
    - Band 1: UKCEH Land Cover Class identifier
    - Band 2: classification confidence indicator
  - 25 m rasters: three bands
    - Band 1: dominant UKCEH Land Cover Class identifier
    - Bands 2 and 3: classification confidence indicators
- The guide focuses on visualising the Land Cover Class data contained in Band 1.
- For a full dataset description, refer to the product documentation.

## Visualisation workflows

- QGIS
  - Add the file to your project; the layer appears in the layers panel
  - Double-click the layer name to open Layer Properties
  - Symbology > Render type: Paletted/Unique Values
  - Band: Band 1
  - Click the style button > Load style from: LCMcolours_QGIS.qml
  - Open the file and click OK; the map redraws with the correct classification

- ArcGIS Desktop
  - In Explorer/folder view, locate the data and expand the raster to show its bands
  - Drag Band_1 into the Table of Contents
  - Layer Properties > Symbology
  - Choose Unique Values (if prompted to build an attribute table, click YES)
  - Click Import and load LCMcolours.lyr
  - Click OK; the map redraws with the correct classification

- ArcGIS Pro
  - Open Catalog and browse to the data folder
  - Expand the raster to display its bands and drag Band_1 into the Table of Contents
  - Layer Properties > Appearance > Symbology
  - Primary: Unique Values (if prompted to build an attribute table, click Yes)
  - Open the hamburger menu in the Symbology panel and choose Import
  - Load LCMcolours.lyr; the map redraws with the correct classification

## Files and assets

- LCMcolours_QGIS.qml: colour style file for QGIS
- LCMcolours.lyr: pre-defined colour style for ArcGIS Desktop/Pro
- These accompany the instructions and standardise visualisation across platforms

## Notes for monitoring framework authors

- Use Band 1 visualisations to maintain consistent classification representations across outputs.
- The provided style files facilitate reproducibility and comparability of visual outputs.
- Ensure access to the accompanying style files and refer to the product documentation for comprehensive data descriptions.
- If needed, consider integrating Band 2/3 information (confidence) separately to assess uncertainty in visual outputs.