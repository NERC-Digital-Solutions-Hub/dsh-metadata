# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land Cover Map rasters are multiband:
  - 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence)
  - 25m rasters: three bands (Band 1 = dominant class; Bands 2–3 = classification confidence)
- This guide focuses on visualising the Land Cover Class data contained in Band 1.
- For full data description, refer to the product documentation.

## Data structure and visualization focus
- Band 1 is used to display the classification.
- To apply consistent visuals, use the provided color styles:
  - QGIS: LCMcolours_QGIS.qml
  - ArcGIS Desktop/ArcGIS Pro: LCMcolours.lyr

## Visualising in QGIS
- Add the file to your project; the layer appears in the Layers panel.
- Steps:
  - Double-click the layer name in the layers panel.
  - Layer properties -> Symbology (left menu) -> Render type: Paletted/unique values -> Band: Band 1
  - Click style -> Load style from the menu
  - Browse to LCMcolours_QGIS.qml -> Open
  - Click OK -> map redraws with correct classification

## Visualising in ArcGIS Desktop
- In the Catalog window, browse to the data folder, expand the raster bands.
- Steps:
  - Drag band_1 into the Table of Contents
  - Double-click the layer name in the Table of Contents -> Layer properties
  - Symbology tab -> Unique Values (if prompted to build the attribute table, click YES)
  - Import -> load LCMcolours.lyr (provided with these instructions)
  - OK -> map redraws with correct classification

## Visualising in ArcGIS Pro
- In ArcGIS Pro project, open the Catalog, browse to the data folder, expand the raster bands.
- Steps:
  - Drag band_1 into the Table of Contents
  - Double-click the layer name -> Layer properties
  - Select the layer in Contents, open Symbology (Appearance > Symbology)
  - Primary symbology: Unique values
  - Hamburger menu in theSymbology panel -> Import -> load LCMcolours.lyr
  - Map redraws with correct classification

## Additional notes
- If prompted to build an attribute table or calculate values, select Yes.
- The accompanying style files ensure consistent classification colors across GIS applications.
- This guide is a short, practical how-to for common GIS tools; refer to product documentation for full data details.