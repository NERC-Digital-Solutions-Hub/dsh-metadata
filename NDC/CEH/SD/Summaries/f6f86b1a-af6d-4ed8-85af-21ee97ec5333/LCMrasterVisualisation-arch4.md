# Visualising UKCEH Land Cover Class using a GIS application

- The Land cover map rasters for 2017-2020 are multiband rasters.
  - 20m and 10m rasters have two bands: Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence indicator.
  - 25m rasters have three bands: Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence indicators.
- This short guide focuses on visualising the Land Cover Class data contained in Band 1; refer to the product documentation for a full data description.

## Visualising in QGIS

- Add the file to your project; it will appear in the layers panel.
- Open layer properties and choose Symbology.
- In the render type, select Paletted/unique values.
- In the band, choose Band 1.
- Click the style button and choose Load style from the menu.
- Browse to the LCMcolours_QGIS.qml file accompanying this document, select it, and open.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Desktop

- In the Catalogue window, browse to the folder containing the data.
- Expand the file to display the raster’s bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open the layer properties.
- In Symbology, choose Unique Values (if prompted to calculate values, click YES).
- Click the Import button and load the provided LCMcolours.lyr file.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Pro

- In the Catalogs window, browse to the folder containing the data.
- Expand the file to display the raster’s bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open the layer properties.
- In Contents, select the layer and open Symbology (Appearance > Symbology).
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and choose Import.
- Load the LCMcolours.lyr file provided with these instructions.
- The map will be redrawn with the correct classification.

## Notes for data governance and usability

- Consistent visualization across GIS platforms is enabled by standard style files (LCMcolours_QGIS.qml and LCMcolours.lyr).
- For complete data context and metadata, refer to the full product documentation.