# Visualising UKCEH Land Cover Class using a GIS application

- Purpose: Short guide to visualise the Land Cover Class data contained in band 1 of UKCEH land cover rasters (2017–2020) across common GIS tools.
- Data structure:
  - 20 m and 10 m rasters: two bands
    - Band 1: UKCEH Land Cover Class identifier
    - Band 2: classification confidence
  - 25 m rasters: three bands
    - Band 1: dominant UKCEH Land Cover Class identifier
    - Bands 2 and 3: indicators of classification confidence
- Intended use for Data Stewards:
  - Provides a reproducible, tool-specific workflow to visualize the standardized band 1 classification.
  - Supports consistent interpretation by users through shared style files and symbols.
  - Highlights the need to reference the full product documentation for complete data descriptions (data governance and metadata context).

## Visualization workflows by GIS tool

- Visualising with QGIS
  - Add the file to your project; layer appears in layers panel.
  - Open layer properties, select Symbology.
  - Set Render type to Paletted/unique values; Band to Band 1.
  - Load styling from LCMcolours_QGIS.qml to apply correct classification colors.
  - Re-draw the map.

- Visualising with ArcGIS Desktop
  - In Catalog, locate the data folder and expand to view raster bands.
  - Drag band_1 into the Table of Contents.
  - Open layer properties and go to Symbology.
  - Choose Unique Values; if prompted, confirm to calculate values.
  - Import the provided LCMcolours.lyr and apply; re-draw the map.

- Visualising with ArcGIS Pro
  - Open project and use Catalog to locate the data folder.
  - Expand the raster and drag band_1 into the Table of Contents.
  - Open layer properties (Contents > Symbology).
  - Set primary symbology to Unique values (confirm to build attribute table if prompted).
  - Use the hamburger menu in the symbology panel to Import and load LCMcolours.lyr; re-draw the map.

## Shared assets and reproducibility

- Style resources accompanying the document:
  - LCMcolours_QGIS.qml (QGIS)
  - LCMcolours.lyr (ArcGIS environments)
- These files enable consistent, repeatable visualization across tools, aiding data discoverability and reuse for governance, validation, and downstream analysis.

## Notes for Data Governance

- The guide emphasizes standardized visualization of the primary classification (band 1) to ensure consistent interpretation across stakeholders.
- Users should refer to the full product documentation for comprehensive data details, metadata, and any updates to the dataset structure or classifications.