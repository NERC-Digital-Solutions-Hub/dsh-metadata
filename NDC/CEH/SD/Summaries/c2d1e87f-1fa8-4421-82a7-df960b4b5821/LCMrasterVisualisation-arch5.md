# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- This guide explains how to visualize the Land Cover Class data from UKCEH Land Cover Map rasters using common GIS applications.
- Data organization: band 1 contains the Land Cover Class identifier; band 2 (and band 3 for 25m data) provide classification confidence.
- For full data description, refer to the product documentation.
- Visualization uses provided style files to ensure a consistent, usable classification display across platforms.

## Data structure and interpretation
- 20 m and 10 m rasters: two bands
  - Band 1: UKCEH Land Cover Class identifier
  - Band 2: classification confidence indicator
- 25 m rasters: three bands
  - Band 1: dominant UKCEH Land Cover Class identifier
  - Bands 2 and 3: classification confidence indicators

## Visualization workflow by GIS platform

### Visualising the data using QGIS
- Add the file to your project; the layer appears in the layers panel.
- Open layer properties and choose Symbology.
- Set render type to Paletted/Unique values; select Band 1.
- Click Load style and browse to LCMcolours_QGIS.qml provided with the document; open.
- OK to redraw the map with the correct classification.

### Visualising the data using ArcGIS Desktop
- In the Catalogue window, locate the data folder and expand the raster to reveal its bands.
- Drag band_1 into the Table of Contents.
- Open layer properties; go to the Symbology tab.
- Choose Unique Values; if prompted to calculate values, confirm.
- Use Import to load LCMcolours.lyr provided with the instructions.
- OK to redraw the map with the correct classification.

### Visualising the data using ArcGIS Pro
- In the Catalog pane, locate the data folder and expand the raster bands.
- Drag band_1 into the Table of Contents.
- Open layer properties and the Symbology (Appearance > Symbology).
- Set primary symbology to Unique Values (agree to build attribute table if prompted).
- Use the hamburger menu in the Symbology panel and choose Import to load LCMcolours.lyr.
- Map will redraw with the correct classification.

## Data governance and stewardship considerations
- Standardization: Use the provided style files (QGIS QML, ArcGIS LYR) to ensure a consistent classification appearance across platforms, aiding discoverability and reuse.
- Metadata and provenance: The guide references specific band structure and the purpose of each band, which should be captured in data catalogs and metadata records.
- Reproducibility: Steps are explicit to reproduce visuals exactly, supporting data sharing and downstream analyses.
- Updates and versioning: The workflow relies on standard styles; ensure versioning of style files is tracked alongside the dataset.
- Documentation alignment: For a complete understanding of data semantics and usage constraints, consult the full product documentation.

## Additional notes
- The document highlights only the most commonly used GIS applications for visualization; refer to the product documentation for a full data description.
- Ensure you have the accompanying style files (LCMcolours_QGIS.qml and LCMcolours.lyr) accessible alongside the dataset when implementing these visuals.