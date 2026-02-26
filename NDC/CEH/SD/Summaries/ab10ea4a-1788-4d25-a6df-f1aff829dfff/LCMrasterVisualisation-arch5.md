# Visualising UKCEH Land Cover Class using a GIS application

- The Land Cover Map rasters are multiband:
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant Land Cover Class; Bands 2–3 = classification confidence).
- The guide focuses on visualising the Land Cover Class data contained in Band 1.
- For a full data description, refer to the product documentation.

## Visualising the data by GIS platform

### Visualising with QGIS
- Add the file to your project; the layer appears in the layers panel.
- Double-click the layer name in the layers panel.
- In Layer Properties → Symbology, choose Paletted/Unique Values.
- In the Band box, choose Band 1; double-click the style.
- Click the style button → Load style from the menu.
- Browse to LCMcolours_QGIS.qml, select it, click Open, then OK.
- The map will redraw with the correct classification.

### Visualising with ArcGIS Desktop
- In the Catalogue window, browse to the data folder.
- Expand the file to view the raster’s bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- Symbology → Unique Values (if prompted to calculate values, click Yes).
- Click Import and load the provided file LCMcolours.lyr.
- Click OK; the map will redraw with the correct classification.

### Visualising with ArcGIS Pro
- In the Catalog, browse to the data folder.
- Expand the file to view the raster’s bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Contents, Appearance → Symbology.
- Primary symbology: Unique Values (if prompted to build an attribute table, click Yes).
- Open the hamburger menu in the Symbology panel → Import.
- Load LCMcolours.lyr; the map will redraw with the correct classification.

## Data stewardship considerations

- Use the provided colour/style files (LCMcolours_QGIS.qml or LCMcolours.lyr) to ensure consistent, reproducible visualization across platforms.
- Ensure band1 is used for classification visualization, with metadata confirming the meaning of bands (class identifiers and confidence indicators).
- For full data description and metadata, refer to the product documentation and ensure accompanying style files are distributed with the dataset to enable reproducible visualization.