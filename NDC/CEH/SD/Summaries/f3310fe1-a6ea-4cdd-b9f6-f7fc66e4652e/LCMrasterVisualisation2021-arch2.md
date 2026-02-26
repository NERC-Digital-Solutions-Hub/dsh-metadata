# Visualising UKCEH Land Cover Class using a GIS application

- The 2021 UKCEH Land Cover Class data are multiband rasters:
  - 10m rasters have two bands: Band 1 = Land Cover Class identifier; Band 2 = classification confidence.
  - 25m rasters have three bands: Band 1 = dominant Land Cover Class identifier; Bands 2–3 = classification confidence indicators.
- This document is a concise guide for visualising the Band 1 data in common GIS applications. A full data description is available in the product documentation.

- Visualising in QGIS:
  - Add the file to the project; layer will appear in the layers panel.
  - Open Layer > Symbology; set Render type to Paletted/Unique Values and Band to Band 1.
  - Load the accompanying LCMcolours_QGIS.qml style file to apply correct classification colours.
  - Apply and redraw the map.

- Visualising in ArcGIS Desktop:
  - In the Catalog, locate the data folder and expand the raster bands.
  - Drag Band_1 into the Table of Contents.
  - Layer Properties > Symbology > Unique Values (if prompted to build an attribute table, choose Yes).
  - Import the accompanying LCMcolours.lyr file and apply; redraw the map.

- Visualising in ArcGIS Pro:
  - Open Catalog, browse to the data folder, expand to view raster bands.
  - Drag Band_1 into the Table of Contents.
  - Layer Properties > Appearance > Symbology; choose Unique Values.
  - Use the hamburger menu in the Symbology panel to Import the LCMcolours.lyr file; the map updates to the correct classification.

- Note:
  - The style files (LCMcolours_QGIS.qml and LCMcolours.lyr) ensure consistent colour mapping for classification across platforms.
  - For a full data description, refer to the product documentation.