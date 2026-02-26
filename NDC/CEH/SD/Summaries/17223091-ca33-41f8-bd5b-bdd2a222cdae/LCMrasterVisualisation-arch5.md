# Visualising UKCEH Land Cover Class using a GIS application

## Purpose and data context
- This is a short guide for visualising the Land Cover Class data contained in band 1 of UKCEH Land Cover Map rasters.
- Full data description is available in the product documentation.
- The rasters are multi-band: 20m and 10m have two bands (Band 1: Land Cover Class identifier; Band 2: classification confidence), while 25m rasters have three bands (Band 1: dominant class; Bands 2–3: confidence indicators).

## Data structure by resolution
- 20m and 10m rasters: Band 1 = Land Cover Class identifier; Band 2 = classification confidence.
- 25m rasters: Band 1 = dominant Land Cover Class; Bands 2 and 3 = classification confidence indicators.

## Visualization steps by GIS platform

### QGIS
- Add the file to the project; layer appears in the layers panel.
- Layer > double-click layer name to open Layer Properties.
- Symbology > Render type: Paletted/unique values; Band: Band 1.
- Style > Load style from the menu; select LCMcolours_QGIS.qml; open.
- OK to redraw the map with correct classification.

### ArcGIS Desktop
- In Catalog, locate the data folder; expand the raster to view bands.
- Drag Band 1 into the Table of Contents.
- Layer Properties > Symbology; set to Unique Values (Yes to build attribute table if prompted).
- Click Import and load LCMcolours.lyr; OK to redraw the map with correct classification.

### ArcGIS Pro
- Open Catalog in the Project; navigate to the data folder and expand the raster to see bands.
- Drag Band 1 into the Table of Contents.
- Layer properties > Symbology (Appearance > Symbology); set Primary/Unique Values.
- Use the hamburger menu in the Symbology panel > Import; load LCMcolours.lyr; map redraws with correct classification.

## Governance considerations for Data Stewards
- Ensure consistent styling files (LCMcolours_QGIS.qml, LCMcolours.lyr) are maintained and versioned for reproducibility.
- Document the visualization workflow to support data users in understanding band usage (Band 1) and the role of confidence bands (2–3).
- Align with data metadata standards to describe band definitions, resolution, and classification scheme.
- Plan for updates and ensure visualization steps remain valid when data are refreshed or reformatted.

## Additional notes
- The guide focuses on visualising band 1 across the most common GIS applications; for a full data description, refer to the product documentation.