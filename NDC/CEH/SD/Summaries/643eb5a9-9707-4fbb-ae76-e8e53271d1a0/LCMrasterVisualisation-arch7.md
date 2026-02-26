# Visualising UKCEH Land Cover Class using a GIS application

- Data: Land cover map rasters for 2017-2020 are multiband rasters.
  - 20m and 10m rasters: two bands
    - Band 1: UKCEH Land Cover Class identifier
    - Band 2: classification confidence indicator
  - 25m rasters: three bands
    - Band 1: dominant UKCEH Land Cover Class identifier
    - Bands 2–3: indicators of classification confidence
- Purpose: Short guide for visualising the Land Cover Class data contained in Band 1 using common GIS applications.
- Note: For a full data description, refer to the product documentation.

## Visualising with QGIS

- Add the file to your project; the layer appears in the layers panel.
- Double-click the layer name in the layers panel to open Layer Properties.
- In the left menu, choose Symbology.
- In Render type, select Paletted/Unique values.
- In Band, select Band 1.
- Click the style button and choose Load style from the menu.
- Browse to LCMcolours_QGIS.qml that accompanies this document, select it, and click Open.
- Click OK; the map will redraw with the correct classification.

## Visualising with ArcGIS Desktop

- In the Catalog window, browse to the folder containing the data.
- Expand the file to display the raster’s bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name in the table of contents to open the Layer Properties.
- In the Symbology tab, select Unique Values as the symbology type.
- If prompted to calculate values, click YES.
- Click Import and load the provided layer file (LCMcolours.lyr).
- Click OK; the map will redraw with the correct classification.

## Visualising with ArcGIS Pro

- In your ArcGIS Pro project, open the Catalog window and browse to the folder containing the data.
- Expand the file to display the raster’s bands and drag band_1 into the Table of Contents.
- Double-click the layer name in the Contents window to open its properties.
- Select Appearance > Symbology.
- In the primary symbology options, choose Unique values (if prompted to build an attribute table, click Yes).
- Click the hamburger menu in the symbology panel and choose Import.
- Load the provided layer file (LCMcolours.lyr).
- The map will redraw with the correct classification.