# Visualising UKCEH Land Cover Class using a GIS application

- Purpose: Short guide to visualize Land Cover Class data stored in Band 1 of UKCEH raster datasets using common GIS applications.
- Data layout:
  - 20m and 10m rasters: two bands
    - Band 1: UKCEH Land Cover Class identifier
    - Band 2: classification confidence
  - 25m rasters: three bands
    - Band 1: dominant UKCEH Land Cover Class identifier
    - Bands 2 and 3: classification confidence
- Reference: For a full data description, consult the product documentation.

## Visualising with QGIS

- Add the file to your project; layer appears in the layers panel.
- Open layer properties > Symbology.
- Render type: Paletted/Unique values; Band: Band 1.
- Click style > Load style from the menu; select LCMcolours_QGIS.qml provided with this document; open.
- Click OK to redraw the map with the correct classification.

## Visualising with ArcGIS Desktop

- In the catalog, locate the data folder and display the raster’s bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer to open the layer properties; go to Symbology.
- Choose Unique Values; if prompted to build an attribute table, click YES.
- Click Import and load LCMcolours.lyr provided with these instructions.
- Click OK to redraw the map with the correct classification.

## Visualising with ArcGIS Pro

- Open Catalog, locate the data folder; expand to show raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer to open Layer Properties; Appearance > Symbology.
- Primary options: Unique values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel to Import, and load LCMcolours.lyr provided with these instructions.
- The map will be redrawn with the correct classification.