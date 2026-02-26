# Visualising UKCEH Land Cover Class using GIS

- This document is a short guide for visualising the UKCEH Land Cover Class data in common GIS applications, focusing on band 1. For a full data description, refer to the product documentation.

## Data specifications

- Land cover map rasters for 2017-2020 are multiband rasters.
  - 20m and 10m rasters: two bands
    - Band 1: UKCEH Land Cover Class identifier
    - Band 2: classification confidence indicator
  - 25m rasters: three bands
    - Band 1: dominant UKCEH Land Cover Class identifier
    - Bands 2 and 3: classification confidence indicators
- The guide demonstrates visualisation using Band 1 only.
- Style files provided with the document enable correct classification colours; refer to the accompanying files (LCMcolours_QGIS.qml and LCMcolours.lyr).

## Visualising in QGIS

- Add the file to your project; the layer appears in the layers panel.
- Open layer properties for the layer.
- Symbology: render type = Paletted/Unique Values; Band = Band 1.
- Click the style button and choose Load style from the menu.
- Load the accompanying LCMcolours_QGIS.qml file and open.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Desktop

- In the Catalogue, locate the data folder and expand the raster to view its bands.
- Drag Band 1 into the Table of Contents.
- Open the layer’s properties and go to Symbology.
- Choose Unique Values; if prompted to build the attribute table, click YES.
- Click Import and load the accompanying LCMcolours.lyr file.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro

- Open the Catalog and navigate to the data folder.
- Expand the raster and drag Band 1 into the Contents.
- Open the layer’s properties and go to Appearance > Symbology.
- In Primary Symbology, choose Unique Values (if prompted, click Yes to build the attribute table).
- Use the Import option in the symbology panel and load LCMcolours.lyr.
- The map will redraw with the correct classification.