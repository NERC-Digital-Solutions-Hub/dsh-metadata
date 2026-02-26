# Visualising UKCEH Land Cover 2015 class using a GIS application

- Dataset: 2015 Land Cover raster at 25 m resolution, two-band image
  - Band 1: classification layer (land cover classes)
  - Band 2: mean per-polygon probability value from the classification algorithm (not used for visualization of band 1 in this guide)
- Purpose: Short guide for visualising the Land Cover Class data contained in band 1 using common GIS applications; refer to the product documentation for a full data description

## Visualising with QGIS

- Add the file to your project; the layer appears in the layers panel
- Double-click the layer name to open Layer Properties
- In Symbology, set Render type to Paletted/Unique Values
- Select Band 1
- Click Classify
- Colours will be assigned to each land class; edit colours as needed using the colour recipe in the product documentation
- Click OK to redraw the map with the correct classification

## Visualising with ArcGIS Desktop

- In the Catalog window, browse to the data folder and expand the raster’s bands
- Drag band_1 into the Table of Contents
- Double-click the layer name to open Layer Properties
- In Symbology, choose Unique Values
- If prompted to calculate values, click YES
- Assign colours to classes (use the colour recipe from the product documentation)
- Click OK to redraw the map with the correct classification

## Additional notes

- This guide focuses on visualising band 1; for a full data description, refer to the product documentation
- Colour schemes and class definitions are provided in the product documentation referenced in the guide