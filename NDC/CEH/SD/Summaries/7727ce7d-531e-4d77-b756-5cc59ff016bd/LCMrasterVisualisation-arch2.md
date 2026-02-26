# Visualising UKCEH Land Cover Class using a GIS application

- This is a short guide for visualising the Land Cover Class data (band 1) from UKCEH land cover rasters using common GIS applications.
- Data structure note: 20 m and 10 m rasters are two-band (band 1 = Land Cover Class identifier; band 2 = classification confidence). 25 m rasters are three-band (band 1 = dominant Land Cover Class; bands 2–3 = classification confidence).
- For a full data description, refer to the product documentation.

## Data structure and purpose

- Band 1 always contains the Land Cover Class identifier used for visualization in this guide.
- Bands 2 and 3 (for 25 m) provide indicators of classification confidence.
- The document focuses on visualising the band 1 classifications consistently across GIS platforms.

## Visualization workflow by software

### Visualising the data using QGIS
- Add the file to your project; the layer appears in the layers panel.
- Open layer properties and select Symbology.
- Set render type to Paletted/Unique values and choose Band 1.
- Load the style from LCMcolours_QGIS.qml, thenOK to redraw the map with the correct classification.

### Visualising the data using ArcGIS Desktop
- In the Catalog window, locate the data folder and expand the raster to reveal bands.
- Drag band_1 into the Table of Contents.
- Open layer properties and go to the Symbology tab; select Unique Values (confirm if prompted to build an attribute table).
- Click Import and load LCMcolours.lyr; OK to redraw the map with the correct classification.

### Visualising the data using ArcGIS Pro
- In the Catalogs window, locate the data folder and expand the raster bands.
- Drag band_1 into the Table of Contents.
- Open layer properties, then Contents > Symbology.
- In Primary Symbology, choose Unique Values (Yes to build attribute table if prompted).
- Use the hamburger menu in the symbology panel to Import and load LCMcolours.lyr; the map will redraw with the correct classification.

## Additional guidance for analysts

- The guide emphasizes consistent, standardized visualization across GIS platforms to support monitoring and comparison over time.
- Use the provided style files (LCMcolours_QGIS.qml and LCMcolours.lyr) to ensure uniform color mappings.
- For comprehensive data description and any nuances, refer to the official product documentation.