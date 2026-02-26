# Visualising UKCEH Land Cover Class using a GIS application

## Purpose and data structure
- A short guide for visualising Land Cover Class data contained in band 1 across common GIS applications.
- Data structure by raster resolution:
  - 20m and 10m rasters: two bands — Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
  - 25m rasters: three bands — Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2–3 = classification confidence indicators.
- For full data description, refer to the product documentation.

## Visualising in QGIS
- Add the file to your project; the layer appears in the layers panel.
- Open layer properties and go to Symbology.
- Render as Paletted/Unique Values and select Band 1.
- Click the style button, choose Load style, and load LCMcolours_QGIS.qml.
- Confirm to redraw the map with correct classification.

## Visualising in ArcGIS Desktop
- In the Catalog window, locate the data folder and expand the raster to view its bands.
- Drag band_1 into the Table of Contents.
- Open layer properties and go to the Symbology tab.
- Choose Unique Values (confirm to build attribute table if prompted).
- Use Import to load LCMcolours.lyr, then OK to redraw with correct classification.

## Visualising in ArcGIS Pro
- In the Catalog, locate the data folder and expand the raster bands.
- Drag band_1 into the Table of Contents.
- Open layer properties and in Contents, access Appearance > Symbology.
- Set Primary Symbology to Unique Values (Yes to build the attribute table if prompted).
- Use the Import option in the Symbology panel to load LCMcolours.lyr and redraw the map with correct classification.

## Additional notes for analysts
- The styling files (LCMcolours_QGIS.qml for QGIS and LCMcolours.lyr for ArcGIS products) accompany these instructions.
- The guide focuses on Band 1 visualization; refer to the full product documentation for deeper data details.