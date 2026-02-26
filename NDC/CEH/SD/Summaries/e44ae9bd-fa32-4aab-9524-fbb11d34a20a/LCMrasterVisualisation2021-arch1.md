# Visualising UKCEH Land Cover Class using a GIS application

- Purpose: Guide to visualising the Land Cover Class data from the UKCEH raster products (2021) using common GIS tools, focusing on band 1.

- Data structure:
  - 10m rasters: two bands
    - Band 1: UKCEH Land Cover Class identifier
    - Band 2: classification confidence indicator
  - 25m rasters: three bands
    - Band 1: dominant UKCEH Land Cover Class identifier
    - Bands 2 & 3: classification confidence indicators
  - This guide concentrates on visualising band 1; full data descriptions are in the product documentation.

- Visualisation guidance by software:

  - QGIS
    - Add the raster layer to the project and open its Layer Properties.
    - In Symbology, set render type to Paletted/Unique Values and Band to Band 1.
    - Load the provided LCMcolours_QGIS.qml style file to apply correct classification colours.

  - ArcGIS Desktop
    - In Catalog, locate the data and drag band_1 into the Table of Contents.
    - Open the layer’s Properties, go to Symbology, choose Unique Values, and import the supplied LCMcolours.lyr.
    - The map will redraw with the correct classification.

  - ArcGIS Pro
    - In Catalog, locate the data and expand to show the raster’s bands.
    - Drag band_1 into the Table of Contents, then open the layer’s Symbology.
    - Set primary symbology to Unique Values, then import the LCMcolours.lyr via the hamburger menu.
    - The map will redraw with the correct classification.

- Additional notes:
  - The LCMcolours files accompany these instructions.
  - A full description of the data is available in the product documentation.