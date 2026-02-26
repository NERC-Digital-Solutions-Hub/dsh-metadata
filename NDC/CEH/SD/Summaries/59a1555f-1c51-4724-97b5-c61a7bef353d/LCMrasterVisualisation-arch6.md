# Visualising UKCEH Land Cover Class using a GIS application

- Purpose: A short, practical guide to visualise UKCEH Land Cover Class data (Band 1) from Land Cover Map rasters in common GIS tools. Notes that 20m/10m rasters have two bands (Band 1: class ID; Band 2: classification confidence) and 25m rasters have three bands (Band 1: dominant class; Bands 2–3: confidence). For full data description, refer to the product documentation.

- General approach across tools:
  - Load the raster into the GIS project; the layer will appear in the layers panel.
  - Open the layer’s properties and set Symbology to use unique values (paletted/unique values).
  - Use Band 1 as the source for classification.
  - Load the provided color style file to ensure correct class colors:
    - QGIS: LCMcolours_QGIS.qml
    - ArcGIS Desktop/Pro: LCMcolours.lyr
  - Apply the style to redraw the map with correct classification.

- Visualising in QGIS:
  - Add the file to the project; select the layer in the Layers panel.
  - Open Layer Properties > Symbology; set Render type to Paletted/Unique values and Band to Band 1.
  - Use Load style to load LCMcolours_QGIS.qml; map updates to show classifications.

- Visualising in ArcGIS Desktop:
  - In Catalog, locate the data and expand the raster bands; drag Band 1 into the Table of Contents.
  - Open Layer Properties > Symbology; choose Unique Values (confirm value calculation if prompted).
  - Use Import to load LCMcolours.lyr; apply to redraw the map with correct classification.

- Visualising in ArcGIS Pro:
  - Open Catalog; locate data, expand bands, drag Band 1 into the Table of Contents.
  - Open Layer Properties > Symbology; set to Unique Values (build attribute table if prompted).
  - Use the Import option from the symbology menu to load LCMcolours.lyr; map updates to show classifications.

- Additional guidance:
  - The color style files accompany the instructions; for a full data description, refer to the product documentation.
  - The guide emphasizes making the Land Cover Class visually distinct and accurately mapped for end-user interpretation.