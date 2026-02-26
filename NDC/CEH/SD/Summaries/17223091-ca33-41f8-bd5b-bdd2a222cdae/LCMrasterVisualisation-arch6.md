# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Purpose: A short guide to visualise the Land Cover Class data stored in band 1 of UKCEH Land Cover Map rasters using common GIS applications.
- Data structure:
  - 20m and 10m rasters: two bands — Band 1 = Land Cover Class identifier; Band 2 = classification confidence.
  - 25m rasters: three bands — Band 1 = dominant Land Cover Class identifier; Bands 2–3 = confidence indicators.
- Output: Visual representations (classified maps) with consistent colour schemes to enable easy interpretation and self-serve analysis.

## Key guidance for data visualization
- Use the classification value in Band 1 to drive the visual classification.
- Load the provided colour/style files to ensure consistent mapping of classes to colours:
  - QGIS: LCMcolours_QGIS.qml
  - ArcGIS (Desktop and Pro): LCMcolours.lyr

## Visualising in QGIS
- Add the Land Cover raster to the project; the layer will appear in the Layers panel.
- Open Layer properties > Symbology.
- Set render type to Paletted/Unique values.
- Select Band 1 as the band.
- Click Style > Load style, then browse to LCMcolours_QGIS.qml and open.
- OK to redraw the map with the correct classification.

## Visualising in ArcGIS Desktop
- Locate the raster folder, expand to view bands, and drag band_1 into the Table of Contents.
- Open Layer Properties > Symbology.
- Choose Unique Values (allow building attribute table if prompted).
- Click Import and load LCMcolours.lyr.
- OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro
- Open Catalog, navigate to the data folder, expand to view raster bands.
- Drag band_1 into the Table of Contents.
- Open layer properties > Symbology (Appearance > Symbology).
- In Primary Symbology, choose Unique Values (Yes to build attribute table if prompted).
- Use the hamburger menu in the Symbology panel > Import to load LCMcolours.lyr.
- The map will redraw with the correct classification.

## Practical notes
- The document references the full data description in the product documentation.
- If prompted to build an attribute table during symbology setup, select Yes.
- These steps enable consistent, shareable visual outputs suitable for dashboards, reports, or public communication.