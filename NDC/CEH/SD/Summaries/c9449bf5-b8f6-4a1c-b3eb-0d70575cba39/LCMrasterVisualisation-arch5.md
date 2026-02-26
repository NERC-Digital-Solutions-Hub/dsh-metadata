# Visualising UKCEH Land Cover Class using a GIS application

## Overview of the data

- Land Cover Map rasters come in multiple resolutions with different band configurations:
  - 20m and 10m rasters: two bands
    - Band 1: UKCEH Land Cover Class identifier
    - Band 2: classification confidence
  - 25m rasters: three bands
    - Band 1: dominant UKCEH Land Cover Class identifier
    - Bands 2 and 3: classification confidence indicators
- The document provides a short guide for visualising the Land Cover Class data based on band 1.
- For full data description, refer to the product documentation.
- Visualisation relies on accompanying style files to ensure consistent representation.

## Visualisation steps by GIS platform

- Visualising with QGIS
  - Add the file to your project; layer appears in the layers panel.
  - Open layer properties and choose Symbology.
  - Set render type to Paletted/Unique Values and select Band 1.
  - Load the style from LCMcolours_QGIS.qml (provided with this document) and apply.
  - The map will redraw with the correct classification.

- Visualising with ArcGIS Desktop
  - In the catalogue, locate the data folder and expand the raster to view its bands.
  - Drag band_1 into the Table of Contents.
  - Open layer properties → Symbology → Unique Values (if prompted, confirm value calculation).
  - Click Import and load LCMcolours.lyr (provided with these instructions).
  - The map will redraw with the correct classification.

- Visualising with ArcGIS Pro
  - Open the Catalog and locate the data folder.
  - Expand the raster to view its bands; drag band_1 into the Contents.
  - Open layer properties → Appearance → Symbology.
  - In Primary Symbology, choose Unique Values (create attribute table if prompted).
  - Use the hamburger menu in the Symbology panel to Import and load LCMcolours.lyr.
  - The map will redraw with the correct classification.

## Data governance considerations for Data Stewards

- Standardisation and reproducibility
  - Use the provided style files (LCMcolours_QGIS.qml, LCMcolours.lyr) to ensure consistent colour mapping across platforms and users.
  - Clear, band-1-focused visualization supports consistent interpretation of classifications.

- Metadata and data descriptions
  - Document band definitions (what Band 1 and, for some resolutions, Bands 2–3 represent) and the corresponding resolutions (20m, 10m, 25m).
  - Include references to the product documentation for a full data description.

- Data packaging and sharing
  - When distributing datasets, include the appropriate style files so downstream users can reproduce visuals accurately.
  - Maintain versioned guidance for which GIS platforms and versions are supported.

- Handling of different data configurations
  - Be mindful of the resolution-specific band structure (2-band vs 3-band datasets) when guiding users or integrating into workflows.

## Practical notes and cautions

- Ensure the accompanying style files (LCMcolours_QGIS.qml or LCMcolours.lyr) are available with the dataset; missing files can lead to inconsistent classifications.
- If naming differs (e.g., band names or layer names), adjust steps accordingly but preserve the concept of visualising Band 1 for classification.
- For comprehensive data characteristics and usage, refer to the product documentation beyond this visualisation guide.