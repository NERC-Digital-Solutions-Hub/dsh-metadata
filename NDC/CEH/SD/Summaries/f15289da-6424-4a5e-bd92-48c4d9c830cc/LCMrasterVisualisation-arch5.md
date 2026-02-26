# Visualising UKCEH Land Cover Class using a GIS application

## Purpose and scope
- Short guide to visualize UKCEH Land Cover Class data contained in band 1 of multiband rasters.
- Applies to common GIS applications; for full data description, consult the product documentation.

## Data structure and band information
- 20m and 10m raster datasets: two bands
  - Band 1: UKCEH Land Cover Class identifier
  - Band 2: classification confidence
- 25m raster datasets: three bands
  - Band 1: dominant UKCEH Land Cover Class identifier
  - Bands 2–3: indicators of classification confidence

## Visualising in GIS platforms (data governance and reproducibility)
- Consistency: use the provided style files to ensure consistent colour mapping of classes across platforms.
  - QGIS: LCMcolours_QGIS.qml
  - ArcGIS (Desktop and Pro): LCMcolours.lyr
- Data focus: apply visualisation to band 1 (land cover class identifiers) to display the classifications.

### Visualising with QGIS
- Add the file to your project; layer appears in the layers panel.
- Open layer properties and select Symbology.
- Set render type to Paletted/Unique Values.
- Choose Band 1.
- Use Load style and select LCMcolours_QGIS.qml.
- Apply to redraw the map with correct classification.

### Visualising with ArcGIS Desktop
- In Catalogue, navigate to the data folder and expand the raster to reveal bands.
- Drag Band 1 into the Table of Contents.
- Open Layer Properties > Symbology.
- Select Unique Values (and YES to build attribute table if prompted).
- Import and load LCMcolours.lyr.
- Apply to redraw the map with correct classification.

### Visualising with ArcGIS Pro
- Open Catalogue in ArcGIS Pro and locate the data folder.
- Expand to reveal raster bands and drag Band 1 into the Table of Contents.
- Open Layer Properties > Symbology (Appearance > Symbology).
- Choose Unique Values (Yes to build attribute table if prompted).
- Use the Import option to load LCMcolours.lyr.
- Map will display the correct classification.

## Data governance considerations for Data Stewards
- Ensure metadata is complete and up to date; reference the product documentation for full data description.
- Maintain and supply the accompanying style files (LCMcolours_QGIS.qml, LCMcolours.lyr) to support consistent visual interpretation across platforms.
- Document the mapping between Band 1 classifications and the persistent colour scheme to support interoperability and reproducibility.
- Be aware of platform-specific steps to ensure consistent outcomes across QGIS, ArcGIS Desktop, and ArcGIS Pro.

## Additional notes
- This guide focuses on visualising the Land Cover Class data in Band 1; for the detailed data model and more on confidence bands, refer to the full product documentation.