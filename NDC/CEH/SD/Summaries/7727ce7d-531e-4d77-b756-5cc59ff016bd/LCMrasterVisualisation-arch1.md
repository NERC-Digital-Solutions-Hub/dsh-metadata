# Visualising UKCEH Land Cover Class using a GIS application

- The Land Cover Map rasters are multi-band datasets:
  - 20 m and 10 m rasters have two bands: Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
  - 25 m rasters have three bands: Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence indicators.
- This document is a short guide for visualising the Land Cover Class data contained in Band 1 using common GIS applications.
- For a full data description, refer to the product documentation.
- The visualisation relies on style files provided with the document:
  - QGIS: LCMcolours_QGIS.qml
  - ArcGIS: LCMcolours.lyr

## Visualising in QGIS

- Add the Land Cover raster to your project; it appears in the layers panel.
- Open Layer properties → Symbology.
- Set Render type to Paletted/Unique Values and select Band 1.
- Click the style button → Load style from LCMcolours_QGIS.qml → Open.
- The map will redraw with the correct classification.

## Visualising in ArcGIS Desktop

- In the Catalogue, navigate to the data folder and expand the raster to view its bands.
- Drag Band 1 (band_1) into the Table of Contents.
- Double-click the layer name to open Layer Properties → Symbology.
- Choose Unique Values (if prompted to build an attribute table, click Yes).
- Click Import → load the provided LCMcolours.lyr.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro

- In your ArcGIS Pro project, open the Catalog and browse to the data folder.
- Expand the raster to view its bands and drag Band 1 (band_1) into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Appearance → Symbology, set Primary symbology to Unique Values (if prompted, build the attribute table).
- Use the hamburger menu in the Symbology panel → Import → load LCMcolours.lyr.
- The map will be redrawn with the correct classification.