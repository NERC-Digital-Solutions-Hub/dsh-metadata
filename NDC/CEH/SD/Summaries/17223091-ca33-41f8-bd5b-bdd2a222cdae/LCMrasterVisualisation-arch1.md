# Visualising UKCEH Land Cover Class using a GIS application

- The Land Cover Map rasters have multiple bands:
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence)
  - 25m rasters: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence)
- Purpose: Visualise the Land Cover Class data contained in Band 1.

## Visualising the data using QGIS
- Add the file to your project; it will appear in the layers panel.
- Open layer properties, choose Symbology.
- Set Render type to Paletted/Unique Values, Band to Band 1.
- Click Style > Load style, browse to LCMcolours_QGIS.qml, select it, and open.
- Click OK; the map will be redrawn with the correct classification.

## Visualising the data using ArcGIS Desktop
- In the Catalog window, navigate to the data folder, expand the raster to show its bands.
- Drag Band_1 into the Table of Contents.
- Open the layer properties, go to the Symbology tab.
- Choose Unique Values (if prompted to calculate values, click YES).
- Click Import and load the provided layer file LCMcolours.lyr.
- Click OK; the map will be redrawn with the correct classification.

## Visualising the data using ArcGIS Pro
- In the Catalog window, browse to the data folder.
- Expand the raster to display its bands, drag Band_1 into the Table of Contents.
- Open layer properties, then Appearance > Symbology.
- In Primary Symbology, select Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and choose Import.
- Load the provided layer file LCMcolours.lyr; the map will be redrawn with the correct classification.

## Additional notes
- For a full description of the data, refer to the product documentation.
- The guidance ensures visualisation reflects the Band 1 Land Cover Class identifier accurately.