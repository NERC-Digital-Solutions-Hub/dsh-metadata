# Visualising UKCEH Land Cover Class using a GIS application

- Overview
  - A short guide to visualizing UKCEH Land Cover Class data in common GIS applications.
  - Land cover map rasters for 2017-2020 are multi-band rasters; band structures differ by resolution.
  - Focuses on visualizing Band 1 (Land Cover Class identifier); full data description available in product documentation.
  - Includes accompanying style files to ensure correct classification visuals (for QGIS and ArcGIS).

- Data structure (bands)
  - 20m and 10m rasters: two bands
    - Band 1: UKCEH Land Cover Class identifier
    - Band 2: classification confidence indicator
  - 25m rasters: three bands
    - Band 1: dominant UKCEH Land Cover Class identifier
    - Bands 2 and 3: classification confidence indicators

- Visualising in QGIS
  - Add the file to your project; the layer appears in the layers panel.
  - Double-click the layer name to open Layer properties.
  - In Symbology, set Render type to Paletted/Unique Values.
  - In Band, select Band 1.
  - Click the style button, choose Load style from the menu.
  - Browse to LCMcolours_QGIS.qml (provided with the document), select and open.
  - Click OK; the map redraws with the correct classification.

- Visualising in ArcGIS Desktop
  - In the Catalog window, navigate to the data folder.
  - Expand the raster to display its bands.
  - Drag band_1 into the Table of Contents.
  - Double-click the layer name to open Layer Properties.
  - Symbology tab: choose Unique Values (if prompted to calculate values, click YES).
  - Click Import and load LCMcolours.lyr (provided with these instructions).
  - Click OK; the map redraws with the correct classification.

- Visualising in ArcGIS Pro
  - Open the Catalog and navigate to the data folder.
  - Expand the raster to display its bands.
  - Drag band_1 into the Table of Contents.
  - Double-click the layer name to open Layer Properties.
  - In Contents -> Appearance -> Symbology, choose Unique Values.
  - If prompted to build an attribute table, click Yes.
  - Use the hamburger menu in the Symbology panel to Import the LCMcolours.lyr file provided with the instructions.
  - The map will redraw with the correct classification.

- Additional notes
  - For a full description of the data, refer to the product documentation.
  - Style files (LCMcolours_QGIS.qml and LCMcolours.lyr) accompany the instructions to ensure consistent visualization.