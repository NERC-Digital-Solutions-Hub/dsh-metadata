# Visualising UKCEH Land Cover Class using a GIS application

- The Land cover map rasters for 2017-2020 are multiband rasters.
  - 20m and 10m rasters: two bands. Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
  - 25m rasters: three bands. Band 1 = dominant Land Cover Class; Bands 2 and 3 = classification confidence.
- Purpose: a short guide for visualising the Land Cover Class data contained in Band 1 using common GIS applications.
- For a full data description, refer to the product documentation.

## Visualising the data using QGIS

- Add the file to your project; it appears in the layers panel.
- Open Layer properties → Symbology.
- Render type: Paletted/Unique values.
- Band: Band 1.
- Click the style button → Load style from the menu.
- Browse to LCMcolours_QGIS.qml accompanying the document, select it, and Open.
- Click OK → map redraws with the correct classification.

## Visualising the data using ArcGIS Desktop

- In the Catalogue window, navigate to the data folder.
- Expand the raster to show its bands.
- Drag Band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties → Symbology tab.
- Choose Unique Values as the symbology type (if prompted to calculate values, click YES).
- Click Import → load the provided layer file LCMcolours.lyr.
- Click OK → map redraws with the correct classification.

## Visualising the data using ArcGIS Pro

- In ArcGIS Pro, open the Catalog window and browse to the data folder.
- Expand the file to show the raster bands.
- Drag Band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Contents, open Appearance → Symbology.
- Primary symbology: choose Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel → Import.
- Load the provided LCMcolours.lyr file.
- The map will be redrawn with the correct classification.