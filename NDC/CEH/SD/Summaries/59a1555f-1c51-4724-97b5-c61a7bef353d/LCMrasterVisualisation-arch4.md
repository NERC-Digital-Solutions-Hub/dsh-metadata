# Visualising UKCEH Land Cover Class using a GIS application

- The Land Cover Map rasters are multiband:
  - 20m and 10m rasters: two bands. Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
  - 25m rasters: three bands. Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence.
- This document is a short guide for visualising the Land Cover Class data contained in band 1. For full data descriptions, refer to the product documentation.

## Visualising in QGIS

- Add the file to your project; it will appear in the layers panel.
- Double-click the layer name to open Layer Properties.
- In Symbology, select Paletted/unique values; set Band to Band 1.
- Click the style button, choose Load style, and load the accompanying LCMcolours_QGIS.qml file.
- Click OK to redraw the map with correct classification.

## Visualising in ArcGIS Desktop

- In the Catalog window, navigate to the data folder and expand the raster’s bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties; go to the Symbology tab.
- Choose Unique Values; if prompted to build an attribute table, click YES.
- Click Import and load the provided LCMcolours.lyr file.
- Click OK to redraw the map with correct classification.

## Visualising in ArcGIS Pro

- In ArcGIS Pro, open the Catalog window and locate the data folder.
- Expand the file to show the raster’s bands and drag band_1 into the Contents.
- Open the layer's Symbology (Appearance > Symbology).
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and choose Import, then load the LCMcolours.lyr file.
- The map will be redrawn with the correct classification.

## Notes for Data Leaders

- The guidance centres on visualising data consistently across major GIS platforms using band 1 (classification) with the provided style files.
- The document references accompanying style files (LCMcolours_QGIS.qml and LCMcolours.lyr) to ensure accurate and shareable visual representation.
- For a full data description, consult the product documentation.