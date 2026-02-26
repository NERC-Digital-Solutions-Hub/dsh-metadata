# Visualising UKCEH Land Cover Class using a GIS application

## Data overview
- Land cover map rasters for 2017-2020 are multi-band datasets.
- 20m and 10m rasters: two bands; Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence indicator.
- 25m rasters: three bands; Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence indicators.
- Document is a short guide for visualising the Land Cover Class data in common GIS applications; refer to product documentation for full data description.

## Visualising the data using QGIS
- Add the file to your project; layer appears in the layers panel.
- Open layer properties, select Symbology.
- In render type, choose Paletted/Unique values; set Band to Band 1.
- Click Load style and browse to LCMcolours_QGIS.qml accompanying the document; open.
- The map is redrawn with the correct classification.

## Visualising the data using ArcGIS Desktop
- In the Catalog window, locate the data folder and expand the raster to view its bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer in the Table of Contents to open Layer Properties; go to Symbology.
- Choose Unique Values (accept prompt to calculate values if asked).
- Click Import and load LCMcolours.lyr provided with these instructions.
- The map is redrawn with the correct classification.

## Visualising the data using ArcGIS Pro
- In ArcGIS Pro, open the Catalog and locate the data folder.
- Expand the raster to display its bands and drag band_1 into the Table of Contents.
- Open layer properties, navigate to Symbology (Appearance > Symbology).
- Select Unique Values (if prompted to build an attribute table, choose Yes).
- Use the hamburger menu in the Symbology panel and choose Import.
- Load LCMcolours.lyr; the map updates to display the correct classification.