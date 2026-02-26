# Visualising UKCEH Land Cover Class using a GIS application

- Purpose: Short guide for visualising Land Cover Class data (band 1) from UKCEH Land Cover Map rasters using common GIS apps. For a full data description, refer to the product documentation.
- Data structure note: 
  - 20m and 10m rasters: two bands (Band 1 = Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant Land Cover Class; Bands 2–3 = classification confidence indicators).
- Visualisation focus: Use band 1 to display the Land Cover Class, with color mapping supplied by accompanying style files.

## Visualising with QGIS

- Add the file to your project; the layer appears in the layers panel.
- Open layer properties > Symbology.
- Render as Paletted/Unique values; Band = Band 1.
- Click style > Load style from file; load LCMcolours_QGIS.qml.
- OK to redraw the map with the correct classification.

## Visualising with ArcGIS Desktop

- In the Catalogue window, locate the data folder, expand the raster to show bands.
- Drag band_1 into the Table of contents.
- Double-click the layer name to open Layer Properties > Symbology.
- Choose Unique Values; if prompted to build an attribute table, click YES.
- Click the Import button and load LCMcolours.lyr; OK to redraw the map with correct classification.

## Visualising with ArcGIS Pro

- In the Project, open Catalogue and locate the data folder; expand to view raster bands.
- Drag band_1 into the Table of contents.
- Double-click the layer name to open Layer Properties; Symbology.
- In Appearance > Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel > Import; load LCMcolours.lyr; the map will redraw with the correct classification.

## Additional considerations for Data Leaders

- The guide concentrates on visualising band 1 to interpret Land Cover Class; bands indicating classification confidence are available in the same rasters but not used for the basic visualization per platform.
- The color/style mappings are provided via platform-specific files (LCMcolours_QGIS.qml, LCMcolours.lyr) to ensure consistent classification visuals across tools.
- For data governance and reuse, note the instruction to refer to the product documentation for full data details and metadata.