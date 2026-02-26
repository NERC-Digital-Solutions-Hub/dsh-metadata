# Visualising UKCEH Land Cover Class using a GIS application

- This document is a short guide for visualising UKCEH Land Cover Class data in common GIS applications, focusing on the Land Cover Class data contained in band 1 of the rasters for 2017–2020.
- Data structure:
  - 20m and 10m rasters: two bands
    - Band 1: UKCEH Land Cover Class identifier
    - Band 2: classification confidence indicator
  - 25m rasters: three bands
    - Band 1: dominant UKCEH Land Cover Class identifier
    - Bands 2 & 3: classification confidence indicators
- For a full data description, refer to the product documentation.

## Purpose and data considerations for Data Leaders

- Emphasises visualising the primary class (band 1) to understand land cover, with confidence indicators available but not the focus of the visualization.
- Ensures consistent, reproducible visual representation by using pre-packaged styling files.
- Highlights the need to locate accompanying style files to achieve correct classification colors (LCMcolours_QGIS.qml, LCMcolours.lyr).

## Visualising in QGIS

- Add the Land Cover data file to the project; layer appears in the layers panel.
- Open layer properties -> Symbology -> render as Paletted/Unique Values -> Band 1.
- Load the provided style:
  - Click style -> Load style from file
  - Select LCMcolours_QGIS.qml and open
- The map redraws with the correct classification colors.

## Visualising in ArcGIS Desktop

- In Catalog, locate the dataset folder; expand the raster to show bands.
- Drag band_1 into the Table of Contents.
- Open layer properties -> Symbology -> Unique Values (if prompted, click YES to build attribute table).
- Click Import -> load LCMcolours.lyr provided with the instructions.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro

- In the Catalog pane, navigate to the data folder and display the raster bands.
- Drag band_1 into the Contents window.
- Open layer properties -> Appearance -> Symbology -> Primary: Unique values (Yes to build attribute table if prompted).
- Use the hamburger menu in the Symbology panel -> Import -> load LCMcolours.lyr.
- The map will redraw with the correct classification.