# Visualising UKCEH Land Cover Class using a GIS application

- Purpose: Short guide for visualising UKCEH Land Cover Class data in common GIS applications to support consistent environmental monitoring outputs.
- Data structure overview:
  - 2017-2020 land cover map rasters are multiband.
  - 20m and 10m rasters: two bands
    - Band 1: UKCEH Land Cover Class identifier
    - Band 2: classification confidence indicator
  - 25m rasters: three bands
    - Band 1: dominant UKCEH Land Cover Class identifier
    - Bands 2 and 3: classification confidence indicators
- Visualisation focus: Use Band 1 for most common visualisations; refer to product documentation for full data descriptions.
- Available styling resources: accompanying style files to standardise classification colours (LCMcolours_QGIS.qml for QGIS; LCMcolours.lyr for ArcGIS). 

## Visualising in QGIS

- Add the land cover data file to the project; the layer appears in the layers panel.
- Open the layer’s properties → Symbology.
- Set Render type to Paletted/Unique Values; select Band 1.
- Click Style → Load style from the provided LCMcolours_QGIS.qml file; open.
- The map is redrawn with the correct classification colours.

## Visualising in ArcGIS Desktop

- In the Catalog, locate the folder containing the data; expand the raster to reveal bands.
- Drag Band 1 (band_1) into the Table of Contents.
- Open the layer’s properties → Symbology.
- Choose Unique Values (confirm to calculate values if prompted).
- Use Import to load the provided LCMcolours.lyr file.
- Click OK to redraw the map with the correct classification colours.

## Visualising in ArcGIS Pro

- Open the catalogue and navigate to the data folder; expand the raster bands.
- Drag Band 1 (band_1) into the Contents pane.
- Open Layer Properties → Appearance → Symbology.
- Set Primary Symbology to Unique Values (and Yes to build attribute table if prompted).
- Use the hamburger menu in the Symbology panel → Import; load LCMcolours.lyr.
- The map is redrawn with the correct classification colours.

## Additional notes

- The LCMcolours style files accompany these instructions to ensure consistent visualisation across platforms.
- For a full description of the data, refer to the product documentation.