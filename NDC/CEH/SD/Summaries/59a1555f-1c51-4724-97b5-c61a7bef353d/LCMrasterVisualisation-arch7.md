# Visualising UKCEH Land Cover Class using a GIS application

- The Land Cover Map rasters come in two densities:
  - 20m and 10m rasters: two bands — Band 1 is the UKCEH Land Cover Class identifier; Band 2 is an indicator of classification confidence.
  - 25m rasters: three bands — Band 1 is the dominant Land Cover Class identifier; Bands 2 and 3 are indicators of classification confidence.
- This short guide covers visualising the Land Cover Class data contained in band 1 using common GIS applications.
- For a full data description, refer to the product documentation.
- Palette/style files accompanying these instructions:
  - QGIS: LCMcolours_QGIS.qml
  - ArcGIS: LCMcolours.lyr

## Visualising the data using QGIS

- Add the file to your project; the layer will appear in the layers panel.
- Double-click the layer name in the layers panel to open Layer Properties.
- In the left-hand menu, choose Symbology.
- In Render type, select Paletted/Unique values.
- In Band, select Band 1.
- Click the style button and choose Load style from the menu.
- Browse to the LCMcolours_QGIS.qml file accompanying this document, select it, and click Open.
- Click OK to redraw the map with the correct classification.

## Visualising the data using ArcGIS Desktop

- In the Catalog window, browse to the folder containing the data.
- Expand the file to display the raster's bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name in the Table of Contents to open Layer Properties.
- In the Layer Properties, select the Symbology tab.
- Choose Unique Values as the symbology type (if prompted to calculate the values, click YES).
- Click the Import button and load the provided LCMcolours.lyr file.
- Click OK to redraw the map with the correct classification.

## Visualising the data using ArcGIS Pro

- In your ArcGIS Pro project, open the Catalog window.
- Browse to the folder containing the data and expand the file to display the raster’s bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name in the Contents to open the Layer Properties.
- Select the layer in the Contents and open the Symbology (Appearance > Symbology).
- In the primary Symbology options, choose Unique Values (if prompted to build an attribute table, click Yes).
- Click the hamburger menu in the Symbology panel and choose Import.
- Load the LCMcolours.lyr file accompanying these instructions.
- The map will be redrawn with the correct classification.