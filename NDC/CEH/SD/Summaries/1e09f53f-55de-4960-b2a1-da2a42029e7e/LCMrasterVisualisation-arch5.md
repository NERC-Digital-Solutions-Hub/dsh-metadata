# Visualising UKCEH Land Cover Class using a GIS application

- The Land Cover Map rasters are multi-band:
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant class identifier; Bands 2–3 = classification confidence).
- This guide covers visualising data contained in Band 1 using common GIS applications; refer to product documentation for full data description.

## Visualising the data using QGIS
- Add the file to your project; layer appears in the layers panel.
- Open layer properties and select Symbology.
- Set render type to Paletted/Unique Values and Band to Band 1.
- Click the style button, choose Load style, and select LCMcolours_QGIS.qml provided with this document.
- Click OK to redraw the map with correct classification.

## Visualising the data using ArcGIS Desktop
- In Catalog, locate the data folder and expand the raster to show its bands.
- Drag band_1 into the Table of Contents.
- Open layer properties and go to the Symbology tab.
- Choose Unique Values (accept prompt to build attribute table if asked).
- Click Import and load LCMcolours.lyr provided with these instructions.
- Click OK to redraw the map with correct classification.

## Visualising the data using ArcGIS Pro
- In ArcGIS Pro, open Catalog and navigate to the data folder.
- Expand the raster to display its bands and drag band_1 into the Table of Contents.
- Open layer properties (Contents) and go to Appearance > Symbology.
- Set primary symbology to Unique Values (then Yes to build attribute table if prompted).
- Use the Import option (hamburger menu) in the Symbology panel to load LCMcolours.lyr.
- The map will be redrawn with the correct classification.

## Notes for data governance and usability
- The provided style files (LCMcolours_QGIS.qml and LCMcolours.lyr) standardize visualization, supporting consistent interpretation across platforms.
- Full data description and attributes are available in the product documentation; use the band 1 classification for visualization and refer to additional bands if confidence metrics are needed.
- Ensures consistent presentation to enable discovery, comparison, and reuse of Land Cover Class data across systems and teams.