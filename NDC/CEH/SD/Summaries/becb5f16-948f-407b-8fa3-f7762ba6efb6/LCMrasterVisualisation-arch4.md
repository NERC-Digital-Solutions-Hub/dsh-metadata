# Visualising UKCEH Land Cover Class using a GIS application

## Purpose and data structure
- Short guide for visualising Land Cover Class data in band 1 using common GIS applications.
- Data specifics:
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2–3 = classification confidence).
- For a full data description, refer to the product documentation.
  
## Visualization workflow by platform

### Visualising the data using QGIS
- Add the file to your project; the layer appears in the layers panel.
- Double-click the layer name to open Layer Properties.
- In Symbology, select Paletted/Unique Values.
- Choose Band 1.
- Click Style -> Load style from the menu.
- Browse to LCMcolours_QGIS.qml accompanying this document, select and open.
- Click OK to redraw the map with the correct classification.

### Visualising the data using ArcGIS Desktop
- In Catalog, locate the folder containing the data; expand the raster to reveal bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties.
- In Symbology, select Unique Values (if prompted to build an attribute table, click YES).
- Click Import and load the provided layer file (LCMcolours.lyr).
- Click OK to redraw the map with the correct classification.

### Visualising the data using ArcGIS Pro
- In the Catalog, locate the data folder and expand the raster bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties; go to Appearance > Symbology.
- In Primary Symbology, choose Unique Values (and build the attribute table when prompted).
- Open the hamburger menu in the Symbology panel and choose Import.
- Load the provided layer file (LCMcolours.lyr).
- The map will be redrawn with the correct classification.

## Considerations for data governance and reuse
- The workflow relies on accompanying style files (LCMcolours_QGIS.qml for QGIS and LCMcolours.lyr for ArcGIS) to ensure consistent classification visuals.
- These steps facilitate consistent visualization across platforms, aiding user understanding and decision-making.
- For comprehensive data description and metadata, follow the product documentation.