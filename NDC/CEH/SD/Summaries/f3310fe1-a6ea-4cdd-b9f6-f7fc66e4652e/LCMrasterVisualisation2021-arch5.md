# Visualising UKCEH Land Cover Class using a GIS application

- Overview
  - Land cover map raster data products for 2021 are multiband rasters.
  - 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence indicator).
  - 25m rasters: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2–3 = classification confidence indicators).
  - This guide focuses on visualising the Land Cover Class data contained in Band 1; refer to the product documentation for full data description.

- Visualising the data using QGIS
  - Add the file to your project; the layer appears in the layers panel.
  - Double-click the layer name in the layers panel to open Layer properties.
  - In Symbology, set Render type to Paletted/Unique values and Band to Band 1.
  - Click the style button, choose Load style, and browse to LCMcolours_QGIS.qml accompanying the document; open.
  - Click OK to redraw the map with the correct classification.

- Visualising the data using ArcGIS Desktop
  - In the Catalog window, locate the folder containing the data and expand the raster to display its bands.
  - Drag Band_1 into the Table of Contents.
  - Double-click the layer to open Layer properties; go to the Symbology tab.
  - Choose Unique Values; if prompted to calculate values, click YES.
  - Click the Import button and load the provided layer file LCMcolours.lyr; OK.
  - The map will be redrawn with the correct classification.

- Visualising the data using ArcGIS Pro
  - Open the Catalogue window in the ArcGIS Pro project and browse to the data folder.
  - Expand to view the raster bands and drag Band_1 into the Table of Contents.
  - Double-click the layer in the Contents to open properties; go to Appearance > Symbology.
  - In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
  - Click the hamburger menu in the Symbology panel and choose Import; load LCMcolours.lyr.
  - The map will be redrawn with the correct classification.

- Key governance and usability notes for Data Stewards
  - The accompanying styling files (LCMcolours_QGIS.qml and LCMcolours.lyr) ensure consistent visualization across tools.
  - Providing standard styles supports discoverability and reuse by data users; ensure end users have access to these files alongside the data.
  - For comprehensive data understanding, direct users to the full product documentation beyond the visualization guide.