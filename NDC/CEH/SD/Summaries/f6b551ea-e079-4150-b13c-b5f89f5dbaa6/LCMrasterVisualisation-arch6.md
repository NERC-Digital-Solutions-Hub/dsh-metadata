# Visualising UKCEH Land Cover Class using a GIS application

- The Land cover map rasters for 2017-2020 are multiband rasters with different band configurations by resolution:
  - 20m and 10m rasters: two bands
    - Band 1: UKCEH Land Cover Class identifier
    - Band 2: classification confidence
  - 25m rasters: three bands
    - Band 1: dominant UKCEH Land Cover Class identifier
    - Bands 2 and 3: indicators of classification confidence
- Purpose: A short guide for visualizing the Land Cover Class data in common GIS applications using band 1, with accompanying color styles.
- Full data description: Refer to the product documentation.

## Visualising in QGIS
- Add the file to your project; layer appears in the layers panel.
- Open layer properties > Symbology.
- Render as Paletted/unique values.
- Set Band to Band 1.
- Load style from the provided LCMcolours_QGIS.qml file.
- Apply to redraw the map with the correct classification.

## Visualising in ArcGIS Desktop
- In the Catalogue window, locate the data folder and expand the raster to show its bands.
- Drag band_1 into the Table of Contents.
- Open layer properties > Symbology.
- Choose Unique Values (if prompted to build values, confirm YES).
- Import the provided LCMcolours.lyr file.
- OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro
- Open the Catalog and navigate to the data folder.
- Expand the raster to reveal its bands and drag band_1 into the Contents.
- Open layer properties > Appearance > Symbology.
- Select Unique Values.
- Use the hamburger menu in the Symbology panel and choose Import.
- Load the provided LCMcolours.lyr file.
- The map will be redrawn with the correct classification.