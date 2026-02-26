# Visualising UKCEH Land Cover Class using a GIS application

- This document explains how to visualize UKCEH Land Cover Class data contained in band 1 of land cover rasters from 2017–2020.
- Raster characteristics:
  - 20 m and 10 m datasets: two bands (Band 1 = Land Cover Class identifier; Band 2 = classification confidence).
  - 25 m datasets: three bands (Band 1 = dominant Land Cover Class; Bands 2 and 3 = classification confidence).
- A full data description is available in the product documentation.
- The guide provides step-by-step instructions for the most commonly used GIS applications and references accompanying style files:
  - QGIS: LCMcolours_QGIS.qml
  - ArcGIS (Desktop/Pro): LCMcolours.lyr

## Visualising in QGIS

- Add the Land Cover data file to your project; the layer appears in the layers panel.
- Open layer properties → Symbology:
  - Render type: Paletted/Unique Values
  - Band: Band 1
- Load color style:
  - Style menu → Load style → select LCMcolours_QGIS.qml → OK
- The map updates to show the correct land cover classification.

## Visualising in ArcGIS Desktop

- In the Catalogue, locate the data folder and expand the raster to view its bands.
- Drag Band_1 into the Table of Contents.
- Layer properties → Symbology:
  - Type: Unique Values (if prompted to build an attribute table, click YES)
- Import the provided color file:
  - Click Import and load LCMcolours.lyr
  - OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro

- In a project, use the Catalogue to locate the data folder and expand the raster bands.
- Drag Band_1 into the Contents.
- Layer properties → Symbology:
  - Primary option: Unique Values (if prompted, build attribute table)
- Import color style:
  - Use the hamburger menu in the Symbology panel → Import → load LCMcolours.lyr
- The map will redraw with the correct Land Cover classification.