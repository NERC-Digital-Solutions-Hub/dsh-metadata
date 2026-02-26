# Visualising UKCEH Land Cover Class using a GIS application

- Purpose: A short guide for visualising Land Cover Class data in common GIS applications, using band 1 of the rasters to display the dominant land cover class.
- Data structure:
  - 2017-2020 Land cover map rasters are multiband.
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence indicator).
  - 25m rasters: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 & 3 = confidence indicators).
- Visualisation approach: Use Band 1 to render the classification with standard colour styles provided by accompanying files to ensure consistent representation.

- Visualising in QGIS:
  - Add the file to your project.
  - Open layer properties, select Symbology.
  - Set Render type to Paletted/Unique Values.
  - Choose Band 1.
  - Load style from LCMcolours_QGIS.qml accompanying the document.
  - Apply to redraw the map with correct classification.

- Visualising in ArcGIS Desktop:
  - Browse to the data folder in the Catalog window, expand the raster, and drag Band_1 into the Table of Contents.
  - Open layer properties, go to Symbology, choose Unique Values (confirm if prompted to calculate values).
  - Click Import and load LCMcolours.lyr provided with the instructions.
  - OK to redraw the map with the correct classification.

- Visualising in ArcGIS Pro:
  - Open the Catalog, navigate to the data folder, expand raster bands, and drag Band_1 into the Table of Contents.
  - Open layer properties (Contents) and go to Appearance > Symbology.
  - In primary symbology, choose Unique Values (yes to build attribute table if prompted).
  - Use the hamburger menu in the symbology panel to Import and load LCMcolours.lyr.
  - Map will redraw with the correct classification.

- Additional notes:
  - For a full data description, refer to the product documentation.
  - Accompanying style files (LCMcolours_QGIS.qml and LCMcolours.lyr) ensure consistent colour mapping across platforms.