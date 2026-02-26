# Visualising UKCEH Land Cover Class using a GIS application

- Multi-band land cover rasters (2017-2020) where:
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence)
  - 25m rasters: three bands (Band 1 = dominant Land Cover Class identifier; Bands 2 and 3 = classification confidence)
- Purpose: a short guide to visualising the Land Cover Class data contained in Band 1 using common GIS applications.
- For a full data description, refer to the product documentation.
- Visualisation relies on predefined colour styles:
  - QGIS: LCMcolours_QGIS.qml
  - ArcGIS: LCMcolours.lyr

## Visualising in QGIS

- Add the Land Cover raster to your project.
- In the Layers panel, double-click the layer name to open Layer Properties.
- Select Symbology.
- In Render Type, choose Paletted/Unique values.
- In Band, choose Band 1.
- Click the Style button and choose Load style from the menu.
- Browse to LCMcolours_QGIS.qml, select it, and click Open.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Desktop

- In the Catalog window, navigate to the folder containing the data.
- Expand the raster to display its bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Symbology, choose Unique Values (if prompted to calculate values, click YES).
- Click Import and load the provided LCMcolours.lyr file.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro

- In your ArcGIS Pro project, open the Catalog pane.
- Navigate to the folder with the data, expand the raster to display its bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open the Layer Properties.
- In Contents, select the layer and open Symbology (Appearance > Symbology).
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Click the hamburger menu in the Symbology panel and choose Import.
- Load the provided LCMcolours.lyr file.
- The map will be redrawn with the correct classification.