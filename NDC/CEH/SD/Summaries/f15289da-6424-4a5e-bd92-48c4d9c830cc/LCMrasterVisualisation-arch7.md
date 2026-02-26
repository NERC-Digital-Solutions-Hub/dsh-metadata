# Visualising UKCEH Land Cover Class using a GIS application

- Data structure:
  - 2017–2020 land cover rasters
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence)
  - 25m rasters: three bands (Band 1 = dominant Land Cover Class; Bands 2–3 = classification confidence indicators)

- Purpose
  - Short guide for visualising the Land Cover Class data contained in Band 1 using common GIS applications
  - For a full data description, refer to the product documentation

- Styling files provided
  - QGIS: LCMcolours_QGIS.qml
  - ArcGIS (Desktop/Pro): LCMcolours.lyr

- Visualising in QGIS
  - Add the file to your project; layer appears in the Layers panel
  - Double-click the layer name to open Layer Properties
  - Symbology: render type to Paletted/Unique values; Band = Band 1
  - Click Style > Load style; select LCMcolours_QGIS.qml and Open
  - Click OK; map updates to display correct classification

- Visualising in ArcGIS Desktop
  - In Catalog, navigate to the data folder
  - Expand the raster and drag band_1 into the Table of Contents
  - Double-click the layer name to open Layer Properties
  - Symbology tab: set Unique Values (if prompted to build values, click YES)
  - Import button: load LCMcolours.lyr
  - Click OK; map updates to display correct classification

- Visualising in ArcGIS Pro
  - In the project, open Catalog and navigate to the data folder
  - Expand the file to show raster bands; drag band_1 into the Table of Contents
  - Double-click the layer name to open Layer Properties
  - Contents window: Appearance > Symbology
  - Primary symbology: Unique Values (if prompted to build an attribute table, click Yes)
  - Open the hamburger menu in the Symbology panel > Import; load LCMcolours.lyr
  - Map updates to display correct classification

- End note
  - This guide focuses on visualising Band 1; consult the product documentation for full data details.