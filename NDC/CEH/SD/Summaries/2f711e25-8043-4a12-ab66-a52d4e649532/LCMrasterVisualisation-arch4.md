# Visualising UKCEH Land Cover Class using a GIS application

- Key data structure
  - Land cover map rasters for 2017–2020 are multiband.
  - 20m and 10m rasters: two bands — Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence indicator.
  - 25m rasters: three bands — Band 1 = dominant Land Cover Class; Bands 2 and 3 = classification confidence indicators.
  - This document is a short guide for visualising the Land Cover Class data contained in Band 1; refer to the product documentation for full data description.

- Visualising in QGIS
  - Add the file to your project; layer appears in the layers panel.
  - Open Layer Properties > Symbology.
  - Select Paletted/Unique Values; set Band to Band 1.
  - Click the style button > Load style from the LCMcolours_QGIS.qml accompanying this document; OK to redraw with correct classification.

- Visualising in ArcGIS Desktop
  - In the Catalogue window, locate the data folder and expand to expose raster bands.
  - Drag Band_1 into the Table of Contents.
  - Open Layer Properties > Symbology; choose Unique Values (YES to any prompt about building the attribute table).
  - Click Import and load LCMcolours.lyr provided with these instructions; OK to redraw with correct classification.

- Visualising in ArcGIS Pro
  - Open Catalog, locate the data folder, expand to reveal raster bands.
  - Drag Band_1 into the Contents.
  - Open Layer Properties > Symbology; set Primary Symbology to Unique Values (Yes to build attribute table if prompted).
  - Use the hamburger menu in the Symbology panel > Import; load LCMcolours.lyr to redraw with correct classification.

- Additional notes
  - The LCM colours files (LCMcolours_QGIS.qml and LCMcolours.lyr) accompany this document and are used to apply consistent classification styling.
  - For a full data description, refer to the product documentation.