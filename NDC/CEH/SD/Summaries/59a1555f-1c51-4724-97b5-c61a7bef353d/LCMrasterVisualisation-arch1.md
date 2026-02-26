# Visualising UKCEH Land Cover Class using a GIS application

- Land Cover Map rasters are multi-band:
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2–3 = classification confidence).
- The guide focuses on visualising data contained in Band 1.
- For a full data description, refer to the product documentation.

## Visualising in QGIS
- Add the file to your project; it will appear in the layers panel.
- Double-click the layer name in the layers panel to open Layer Properties.
- In Symbology, set Render type to Paletted/Unique Values.
- In Band, select Band 1.
- Click the style button and choose Load style from the menu.
- Browse to the LCMcolours_QGIS.qml file accompanying this document, select it, and click Open.
- Click OK; the map will be redrawn with the correct classification.

## Visualising in ArcGIS Desktop
- In the Catalogue window, browse to the folder containing the data.
- Expand the file to reveal the raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name in the Table of Contents to open the Layer Properties.
- In the Symbology tab, choose Unique Values (if prompted to calculate values, click YES).
- Click Import and load the provided LCMcolours.lyr file.
- Click OK; the map will be redrawn with the correct classification.

## Visualising in ArcGIS Pro
- In your ArcGIS Pro project, open the Catalog pane and browse to the folder with the data.
- Expand the file to display the raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open the Layer Properties.
- With the layer selected, open Symbology (Appearance > Symbology).
- In Primary Symbology, choose Unique Values. If prompted to build an attribute table, click Yes.
- Open the hamburger menu in the Symbology panel and choose Import.
- Load the provided LCMcolours.lyr file.
- The map will be redrawn with the correct classification.