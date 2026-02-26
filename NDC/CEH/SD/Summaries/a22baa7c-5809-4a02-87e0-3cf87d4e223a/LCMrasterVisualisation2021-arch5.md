# Visualising UKCEH Land Cover Class using a GIS application

- Data context:
  - Land cover map raster data products for 2021 are multiband rasters.
  - 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2–3 = classification confidence).
  - The guide focuses on visualising data contained in Band 1; refer to product documentation for full data description.

- Purpose from a Data Steward perspective:
  - Provide clear, repeatable instructions to visualise the key class data so users can readily discover and interpret land cover classifications.
  - Ensure consistent styling by using provided style files, enabling accurate cross-tool comparisons and usability.

- Visualisation steps by GIS tool:

  - QGIS
    - Add the data to the project; layer appears in the layers panel.
    - Open Layer Properties > Symbology.
    - Render as Paletted/Unique Values; Band = Band 1.
    - Load style from LCMcolours_QGIS.qml accompanying the document; apply to redraw the map with correct classification.

  - ArcGIS Desktop
    - In Catalog, locate the data and expand the raster’s bands.
    - Drag Band_1 into the Table of Contents.
    - Layer Properties > Symbology > Unique Values; if prompted to calculate values, click Yes.
    - Use Import to load LCMcolours.lyr provided with the instructions; map redraws with correct classification.

  - ArcGIS Pro
    - In Catalog, browse to the data folder and expand the raster bands.
    - Drag Band_1 into the Table of Contents.
    - Layer Properties > Appearance > Symbology; set Primary to Unique Values.
    - If prompted to build an attribute table, click Yes.
    - Use the Import option (hamburger menu in the Symbology panel) to load LCMcolours.lyr; map redraws with correct classification.

- Additional notes for data governance and reuse:
  - The styling files (LCMcolours_QGIS.qml and LCMcolours.lyr) accompany the document to ensure consistent visualization across platforms.
  - For complete data description and context, refer to the product documentation.