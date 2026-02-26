# Visualising UKCEH Land Cover Class using a GIS application

- Purpose and scope
  - Short guide for visualising Land Cover Class data contained in band 1 of the 2021 UKCEH land cover rasters.
  - Refers users to the full product documentation for detailed data descriptions.

- Data structure at a glance
  - 10m raster datasets: two bands
    - Band 1: UKCEH Land Cover Class identifier
    - Band 2: classification confidence indicator
  - 25m raster datasets: three bands
    - Band 1: dominant UKCEH Land Cover Class identifier
    - Bands 2 and 3: classification confidence indicators
  - Visualization focuses on Band 1 (class identifiers)

- Visualisation workflow by platform
  - QGIS
    - Add the raster to the project; layer appears in the layers panel.
    - Open Layer Properties > Symbology; set Render type to Paletted/Unique Values; select Band 1.
    - Use Load Style to import LCMcolours_QGIS.qml to apply correct classification colours.
    - Map refreshes to display the classified land cover.
  - ArcGIS Desktop
    - In Catalog, locate the dataset and expand to view the raster bands; drag band_1 into the Table of Contents.
    - Layer Properties > Symbology > Unique Values (confirm if prompted to calculate values).
    - Import the provided LCMcolours.lyr to apply the correct classification styling.
    - Map refreshes to display the classified land cover.
  - ArcGIS Pro
    - Open Catalog, locate the dataset and expand to view the raster bands; drag band_1 into the Table of Contents.
    - Layer Properties > Symbology; set to Unique Values (and yes to build attribute table if prompted).
    - Use the hamburger menu in the Symbology panel and choose Import; load LCMcolours.lyr to apply correct classification.
    - Map refreshes to display the classified land cover.

- Practical considerations for data governance and use
  - Ensures consistent classification visuals across platforms by using standardized style files (LCMcolours_QGIS.qml, LCMcolours.lyr).
  - Highlight that the approach facilitates discoverability and reuse of the classification scheme.
  - Note that full data description is provided in the accompanying product documentation, with this guide focusing on practical visualization steps.
  - Emphasizes reliance on Band 1 for core classification visualization, with Band 2/3 providing confidence indicators (for 25m data).