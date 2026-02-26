# Visualising UKCEH Land Cover Class using a GIS application

- Data overview
  - Land cover map rasters for 2017–2020 are multiband rasters.
  - 20m and 10m datasets: two bands — Band 1 is the UKCEH Land Cover Class identifier; Band 2 is a classification confidence indicator.
  - 25m datasets: three bands — Band 1 is the dominant Land Cover Class; Bands 2 and 3 indicate confidence.
  - This guide focuses on visualising Band 1; refer to full product documentation for a complete data description.

- Visualisation workflow by platform
  - QGIS
    - Add the file to the project; layer appears in the layers panel.
    - Layer properties > Symbology.
    - Render as Paletted/Unique Values; Band 1 selected.
    - Use Load Style to import LCMcolours_QGIS.qml.
    - OK to redraw the map with correct classification.
  - ArcGIS Desktop
    - In Catalog, locate the data folder; expand to expose bands.
    - Drag band_1 into the Table of Contents.
    - Layer properties > Symbology > Unique Values (Yes to calculate values if prompted).
    - Import to load LCMcolours.lyr; OK to redraw with correct classification.
  - ArcGIS Pro
    - In Catalog, navigate to the data folder and view raster bands.
    - Drag band_1 into the Table of Contents.
    - Layer properties > Symbology (Appearance > Symbology).
    - Primary symbology: Unique values; if prompted, build the attribute table.
    - Use the Import option from the hamburger menu to load LCMcolours.lyr.
    - The map will redraw with the correct classification.

- Additional notes
  - The LCMcolours style files accompany the instructions (LCMcolours_QGIS.qml and LCMcolours.lyr).
  - For a complete data description, consult the product documentation.