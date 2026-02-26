# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Short guide for visualising UKCEH Land Cover Class data in common GIS applications.
- Land cover rasters for 2017–2020 are multiband:
  - 20m and 10m rasters: two bands (Band 1 = Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant Land Cover Class identifier; Bands 2–3 = confidence indicators).
- Focus of the guide is on visualising data using Band 1; refer to product documentation for full data description.

## Dataset structure and implications for governance
- Data comprises land cover rasters at multiple resolutions (20m, 10m, 25m).
- Band 1 provides the classification that should be visualised; Bands 2–3 indicate confidence, which can inform data quality considerations.
- To ensure consistent interpretation across platforms and datasets, standardized style files are provided for visualization.

## Visualising the data by GIS platform

### Visualising with QGIS
- Add the file to the project; layer appears in the layers panel.
- Open layer properties, choose Symbology.
- In render type, select Paletted/Unique Values.
- Choose Band 1.
- Load style: select LCMcolours_QGIS.qml accompanying this document.
- Apply (OK); map redraws with correct classification.

### Visualising with ArcGIS Desktop
- In Catalog, locate the data folder and expand the raster to view bands.
- Drag band_1 into the Table of Contents.
- Open layer properties and go to the Symbology tab.
- Choose Unique Values; if prompted to build an attribute table, click Yes.
- Click Import and load LCMcolours.lyr accompanying this document.
- Apply (OK); map redraws with correct classification.

### Visualising with ArcGIS Pro
- In the project, open the Catalog, browse to the data folder.
- Expand the file to display the raster bands; drag band_1 into the Table of Contents.
- Open layer properties and go to Appearance > Symbology.
- In Primary Symbology, select Unique Values (if prompted to build an attribute table, click Yes).
- Open the hamburger menu in the Symbology panel and choose Import; load LCMcolours.lyr.
- Apply (OK); map redraws with correct classification.

## Notes for Data Stewards
- The visualization relies on a consistent color/classification mapping via provided style files (LCMcolours_QGIS.qml and LCMcolours.lyr), supporting uniform interpretation across platforms.
- For full data description and metadata, refer to the product documentation.
- Ensures that the Band 1 classification is used for visualization to facilitate discovery, comparison, and reuse across datasets and portals.