# Visualising UKCEH Land Cover Class using a GIS application

- Purpose and data structure
  - Land Cover Map rasters are multi-band.
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant Land Cover Class; Bands 2 and 3 = classification confidence).
  - Guide focuses on visualising the Land Cover Class data contained in Band 1.
  - For full data description, refer to the product documentation.

- Visualization workflow by GIS tool
  - QGIS
    - Add the file to the project.
    - Open Layer Properties > Symbology > Render type: Paletted/Unique Values; Band: Band 1.
    - Load style from LCMcolours_QGIS.qml; apply to redraw map with correct classification.
  - ArcGIS Desktop
    - In Catalog, locate data folder; expand raster bands; drag band_1 into Table of Contents.
    - Layer Properties > Symbology > Unique Values; click Import and load LCMcolours.lyr; map redraws with correct classification.
  - ArcGIS Pro
    - Open Catalog, drag Band 1 into Table of Contents.
    - Layer Properties > Symbology (Appearance > Symbology); set to Unique Values.
    - Use Import from the hamburger menu to load LCMcolours.lyr; map redraws with correct classification.

- Style assets and data governance
  - Style files provided with the instructions (LCMcolours_QGIS.qml for QGIS; LCMcolours.lyr for ArcGIS).
  - These styles ensure consistent classification visuals across tools.
  - If needed, refer to the accompanying product documentation for full data details and metadata.

- Relevance for Data Leaders
  - Data is structured for cross-platform visualization via a single band (Band 1) representing class identifiers, with separate confidence bands where applicable.
  - The guide supports consistent user-facing outputs and discoverability by providing ready-made style files.
  - Highlights the importance of metadata, documentation, and standardized visuals to enable efficient data use across teams and partner networks.