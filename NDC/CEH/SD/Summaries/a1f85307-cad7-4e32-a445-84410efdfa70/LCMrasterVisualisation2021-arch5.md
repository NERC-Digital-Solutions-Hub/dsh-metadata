# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Short guide for visualising Land Cover Class data contained in band 1 of the 2021 Land cover map raster products.
- Distinguishes 10m and 25m raster structures and directs users to the full product documentation for comprehensive data description.

## Data structure (bands)
- 10m rasters: two bands
  - Band 1: UKCEH Land Cover Class identifier
  - Band 2: classification confidence
- 25m rasters: three bands
  - Band 1: dominant UKCEH Land Cover Class identifier
  - Bands 2 and 3: classification confidence indicators

## Visualising with QGIS
- Add the file to your project; layer appears in the layers panel.
- Open layer properties → Symbology.
- Render as Paletted/Unique Values; Band 1 selected.
- Click the style button → Load style from LCMcolours_QGIS.qml (accompanies the document).
- Click OK to redraw the map with correct classification.

## Visualising with ArcGIS Desktop
- In Catalog, locate the data folder, expand to view raster bands.
- Drag band_1 into Table of Contents.
- Layer properties → Symbology → Unique Values (if prompted to build attribute table, choose YES).
- Click Import and load LCMcolours.lyr (provided with these instructions).
- Click OK to redraw the map with correct classification.

## Visualising with ArcGIS Pro
- Open Catalog in your ArcGIS Pro project; navigate to the data folder and expand to view raster bands.
- Drag band_1 into the Table of Contents.
- Layer properties → Symbology → set to Unique Values (if prompted to build an attribute table, select Yes).
- Use the hamburger menu in the Symbology panel → Import; load LCMcolours.lyr.
- Map will redraw with the correct classification.

## Practical notes for Data Stewards
- Ensure accompanying color style files (LCMcolours_QGIS.qml and LCMcolours.lyr) are included with the dataset to guarantee consistent visualization across platforms.
- Document band definitions (Band 1 as Land Cover Class identifier; additional bands as confidence indicators) in dataset metadata.
- Include guidance on when and how to use the classification confidence information (Band 2/3 for 25m rasters) for users and downstream analyses.
- Maintain alignment between visualization styles and the latest product documentation to support reproducibility and interoperability.

## Accessory materials
- LCMcolours_QGIS.qml for QGIS ( accompanies the document )
- LCMcolours.lyr for ArcGIS ( accompanies the document )