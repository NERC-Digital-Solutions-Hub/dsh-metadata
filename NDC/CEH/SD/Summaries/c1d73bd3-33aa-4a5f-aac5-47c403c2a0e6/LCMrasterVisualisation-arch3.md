# Visualising UKCEH Land Cover Class using a GIS application

## What this guide does
- Provides a quickstep guide to visualising UKCEH Land Cover Class data in common GIS applications.
- Focuses on displaying the classification (band 1) for 2017–2020 land cover rasters, with guidance on using provided styling files to ensure consistent visuals.

## Data structure

- 20m and 10m rasters
  - Two bands
  - Band 1: UKCEH Land Cover Class identifier
  - Band 2: classification confidence indicator
- 25m rasters
  - Three bands
  - Band 1: dominant UKCEH Land Cover Class identifier
  - Bands 2–3: confidence indicators

- The guide focuses on visualising band 1; refer to product documentation for full data description.

## Visualising in QGIS

- Add the file to your project; the layer appears in the layers panel.
- Layer properties → Symbology → Render type: Paletted/unique values → Band: Band 1.
- Click style → Load style from the LCMcolours_QGIS.qml file accompanying this document → Open.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Desktop

- In the Catalogue, locate the data folder and expand the raster to display its bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name → Layer properties → Symbology tab.
- Choose Unique Values; if prompted to calculate values, click YES.
- Click Import and load the provided LCMcolours.lyr file.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro

- Open the catalog in the project; browse to the data folder.
- Expand the raster's bands; drag band_1 into the Table of Contents.
- Double-click the layer → Layer properties.
- In Contents/Symbology, set primary option to Unique values (create attribute table if prompted).
- Use the hamburger menu in the Symbology panel → Import; load LCMcolours.lyr.
- The map will be redrawn with the correct classification.