# Visualising UKCEH Land Cover Class using a GIS application

- This is a short guide for visualising Land Cover Map rasters in common GIS applications, focusing on band 1 which contains the Land Cover Class identifier.
- For full dataset descriptions, refer to the product documentation.

## Data structure at a glance

- 20m and 10m rasters: 2 bands
  - Band 1: UKCEH Land Cover Class identifier
  - Band 2: classification confidence indicator
- 25m rasters: 3 bands
  - Band 1: dominant UKCEH Land Cover Class identifier
  - Bands 2 and 3: classification confidence indicators
- Visualization centers on band 1; other bands reflect confidence.

## Visualization workflow by GIS

- Visualising with QGIS
  - Add the raster to your project; open layer properties.
  - Set Symbology to Paletted/Unique Values and select Band 1.
  - Load the provided style: LCMcolours_QGIS.qml, then OK to redraw with correct classification.

- Visualising with ArcGIS Desktop
  - In Catalog, navigate to the data folder and expand the raster bands.
  - Drag band_1 into the Table of Contents; open its Layer Properties.
  - Symbology: choose Unique Values (confirm to build attribute table if prompted).
  - Use Import to load LCMcolours.lyr; OK to redraw with correct classification.

- Visualising with ArcGIS Pro
  - Open Catalog, locate the data folder, expand to view raster bands and drag band_1 into the map.
  - Open Layer Properties > Appearance > Symbology; choose Unique Values.
  - Use the hamburger menu in the Symbology panel to Import and load LCMcolours.lyr; the map will redraw with correct classification.

## Practical notes for data leaders

- The provided styling files (LCMcolours_QGIS.qml, LCMcolours.lyr) ensure consistent color mapping of classifications across GIS platforms.
- This guide focuses on the primary class identifier (band 1); refer to the full product documentation for deeper data details and metadata.
- The workflow supports reproducibility and facilitates cross-team collaboration by standardizing how Land Cover Class data is visualized.