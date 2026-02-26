# Visualising UKCEH Land Cover Class using a GIS application

- Dataset structure
  - 20m and 10m rasters have two bands: Band 1 is the UKCEH Land Cover Class identifier; Band 2 is an indicator of classification confidence.
  - 25m datasets have three bands: Band 1 is the dominant UKCEH Land Cover Class identifier; Bands 2 and 3 are indicators of classification confidence.
  - The guide focuses on visualising the Land Cover Class data contained in Band 1.

- How to visualize in GIS (by tool)
  - QGIS
    - Add the file to your project; open the layer in the layers panel.
    - Layer properties → Symbology → Render type: Paletted/Unique Values → Band: Band 1.
    - Click the style button → Load style from the provided LCMcolours_QGIS.qml → OK → map redrawn with correct classification.
  - ArcGIS Desktop
    - In Catalog, locate the data and expand its bands.
    - Drag band_1 into the Table of Contents; layer properties → Symbology → Unique Values → Import → load LCMcolours.lyr → OK → map redrawn with correct classification.
  - ArcGIS Pro
    - In Catalog, locate the data and expand its bands.
    - Drag band_1 into the Table of Contents; layer → Properties → Appearance > Symbology → Unique Values.
    - Use the hamburger menu in the Symbology panel → Import → load LCMcolours.lyr → map redrawn with correct classification.

- Style files and documentation
  - QGIS style file: LCMcolours_QGIS.qml
  - ArcGIS style file: LCMcolours.lyr
  - For a full description of the data, refer to the product documentation.

- Relevance for monitoring frameworks
  - Standardized visualization using provided style files supports consistent interpretation and communication of land cover classifications across teams.
  - Encourages reproducibility and alignment with data governance by using centralized, shareable styles.