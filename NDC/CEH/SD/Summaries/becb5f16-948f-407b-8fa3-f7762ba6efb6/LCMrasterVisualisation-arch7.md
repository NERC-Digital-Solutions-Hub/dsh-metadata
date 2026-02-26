# Visualising UKCEH Land Cover Class using a GIS application

- A short guide for visualising Land Cover Class data contained in band 1 of multi-band rasters in common GIS applications.
- Data characteristics:
  - 20m and 10m rasters: two bands total; Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
  - 25m rasters: three bands total; Band 1 = dominant UKCEH Land Cover Class; Bands 2 and 3 = classification confidence indicators.
- For a full data description, refer to the product documentation.

## Visualising in QGIS

- Add the file to your project; the layer appears in the layers panel.
- Open Layer properties -> Symbology.
- Set Render type to Paletted/Unique values; Band to Band 1.
- Use Load style and select LCMcolours_QGIS.qml provided with the document.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Desktop

- In the Catalogue, browse to the data folder, expand the raster to view its bands.
- Drag Band 1 (band_1) into the Table of Contents.
- Open Layer properties -> Symbology.
- Choose Unique Values; if prompted to build an attribute table, click Yes.
- Click Import and load the provided LCMcolours.lyr.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro

- In the project, open the Catalog, browse to the data folder, expand to view raster bands.
- Drag Band 1 (band_1) into the Table of Contents.
- Open Layer properties -> Symbology (Appearance > Symbology).
- Set Primary symbology to Unique Values (if prompted to build an attribute table, click Yes).
- Use the Hamburger menu in the Symbology panel -> Import, and load LCMcolours.lyr.
- The map will be redrawn with the correct classification.