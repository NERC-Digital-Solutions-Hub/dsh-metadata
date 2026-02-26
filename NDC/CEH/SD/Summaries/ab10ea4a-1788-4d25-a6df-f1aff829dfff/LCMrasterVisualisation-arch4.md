# Visualising UKCEH Land Cover Class using a GIS application

## Overview of the data
- Land Cover Map rasters come in 20m, 10m, and 25m resolutions.
- 20m and 10m rasters: two bands per raster.
  - Band 1: UKCEH Land Cover Class identifier.
  - Band 2: classification confidence indicator.
- 25m rasters: three bands per raster.
  - Band 1: dominant UKCEH Land Cover Class identifier.
  - Bands 2 and 3: indicators of classification confidence.
- The guide focuses on visualising Band 1 across common GIS applications; refer to the product documentation for full data details.

## Visualising in QGIS
- Add the file to your project; the layer appears in the layers panel.
- Open layer properties for the layer.
- In the Render type, select Paletted/Unique Values.
- Choose Band 1 in the band box.
- Click the style button and choose Load style from the menu.
- Browse to LCMcolours_QGIS.qml accompanying the document, select it, and open.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Desktop
- In the Catalog window, locate the data folder and expand the raster to show its bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open the layer properties.
- In Symbology, select Unique Values (if prompted to calculate values, click YES).
- Click the Import button and load the provided layer file (LCMcolours.lyr).
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro
- Open the Catalog pane in your ArcGIS Pro project.
- Browse to the data folder and expand to view the raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open the Layer Properties.
- In the Contents pane, open Appearance > Symbology.
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and choose Import.
- Load the provided layer file (LCMcolours.lyr).
- The map will be redrawn with the correct classification.

## Governance and usage notes
- This guide standardises visualization across tools by using a single classification scheme for Band 1, supporting consistent interpretation and communication of land cover classes.
- For a full understanding of the data’s structure, availability, and metadata, refer to the product documentation.
- The approach aligns with data leaders’ aims to ensure data products meet user needs, maintain discoverability, and support effective dissemination within the wider data community.