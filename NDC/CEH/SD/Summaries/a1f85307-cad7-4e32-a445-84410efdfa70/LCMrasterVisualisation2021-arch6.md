# Visualising UKCEH Land Cover Class using a GIS application

## Data description

- Land cover map raster data products for 2021 are multiband rasters.
- 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
- 25m rasters: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2–3 = classification confidence).
- The guide focuses on visualising data contained in Band 1.
- For full data description, refer to the product documentation.
- Accompanying colour/style files to ensure consistent visuals:
  - QGIS: LCMcolours_QGIS.qml
  - ArcGIS: LCMcolours.lyr

## Visualising in QGIS

- Add the file to your project; the layer appears in the layers panel.
- Double-click the layer name in the layers panel to open Layer Properties.
- Symbology: render as Paletted/Unique Values.
- Band: Band 1.
- Click the style button -> Load style from the LCMcolours_QGIS.qml file provided with this document.
- Click OK; the map redraws with the correct classification.

## Visualising in ArcGIS Desktop

- In the Catalogue window, locate the data folder.
- Expand the raster and drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- Symbology: Unique Values (if prompted to build an attribute table, click Yes).
- Click Import and load the provided LCMcolours.lyr.
- Click OK; the map redraws with the correct classification.

## Visualising in ArcGIS Pro

- Open the Catalogue in ArcGIS Pro and browse to the data folder.
- Expand the raster and drag Band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Contents, go to Appearance > Symbology.
- Primary symbology: Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and choose Import to load LCMcolours.lyr.
- The map will redraw with the correct classification.