# Visualising UKCEH Land Cover Class using a GIS application

- Purpose and scope
  - Short guide for visualising Land Cover Class data contained in band 1 of the UKCEH land cover rasters (2017–2020).
  - Focuses on how to use common GIS applications to visualise the data; refer to the product documentation for full data descriptions.

- Data structure overview
  - 2017–2020 land cover map rasters are multiband.
  - 20m and 10m rasters: two bands. Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
  - 25m rasters: three bands. Band 1 = dominant UKCEH Land Cover Class; Bands 2–3 = classification confidence indicators.
  - Visualization in this guide uses Band 1; a full data description is in the product documentation.

- Visualising with QGIS
  - Add the file to the project; the layer appears in the layers panel.
  - Open layer properties > Symbology > render type: Paletted/Unique Values; Band: Band 1.
  - Click the style button > Load style > select LCMcolours_QGIS.qml accompanying this document > OK.
  - The map redraws with the correct classification.

- Visualising with ArcGIS Desktop
  - In the Catalogue, navigate to the data folder and expand the raster to view its bands.
  - Drag Band_1 into the Table of Contents.
  - Layer properties > Symbology > Unique Values (if prompted to build values, click YES).
  - Import the provided LCMcolours.lyr file; map redraws with the correct classification.

- Visualising with ArcGIS Pro
  - In a project, open Catalogue and locate the data folder; expand to view raster bands.
  - Drag Band_1 into the Table of Contents.
  - Layer properties > Symbology; set Primary to Unique Values (Yes to build attribute table if prompted).
  - Use the hamburger menu in the Symbology panel to Import and load LCMcolours.lyr; map redraws with the correct classification.

- Governance and stewardship notes
  - Style/legend files (LCMcolours_QGIS.qml and LCMcolours.lyr) accompany the data to ensure consistent visualization across platforms.
  - Documentation emphasizes Band 1 as the visualization target; metadata should capture band definitions and confidence indicators.
  - Ensure provenance and versioning of visualization styles are maintained as part of data sharing.