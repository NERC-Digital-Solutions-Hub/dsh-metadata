# Visualising UKCEH Land Cover Class using a GIS application

- This is a short guide for visualising the Land Cover Class data contained in band 1 of UKCEH Land Cover Map rasters using common GIS applications.
- For a full description of the data, refer to the product documentation.

## Data structure

- 20m and 10m rasters: two bands
  - Band 1: UKCEH Land Cover Class identifier
  - Band 2: classification confidence indicator
- 25m rasters: three bands
  - Band 1: dominant UKCEH Land Cover Class identifier
  - Bands 2 and 3: indicators of classification confidence

## Visualising in QGIS

- Add the file to your project; it appears in the layers panel.
- Open layer properties → Symbology.
- Render as Paletted/Unique Values; Band → Band 1.
- Click style → Load style from file, select LCMcolours_QGIS.qml, and apply.
- The map redraws with the correct classification.

## Visualising in ArcGIS Desktop

- In the Catalog, locate the data folder, expand the raster, and drag band_1 into the Table of Contents.
- Layer properties → Symbology → Unique Values (if prompted to calculate values, click YES).
- Click the Import button and load LCMcolours.lyr.
- Apply; the map redraws with the correct classification.

## Visualising in ArcGIS Pro

- Open Catalog in your ArcGIS Pro project and browse to the data folder.
- Expand the raster bands and drag band_1 into the Table of Contents.
- Layer properties → Appearance → Symbology → Primary: Unique Values (or Yes to build attribute table if prompted).
- Use the hamburger menu in the Symbology panel → Import; load LCMcolours.lyr.
- The map redraws with the correct classification.

## Notes

- The accompanying style files (LCMcolours_QGIS.qml and LCMcolours.lyr) standardise visualization across platforms.
- For comprehensive data details, consult the product documentation.