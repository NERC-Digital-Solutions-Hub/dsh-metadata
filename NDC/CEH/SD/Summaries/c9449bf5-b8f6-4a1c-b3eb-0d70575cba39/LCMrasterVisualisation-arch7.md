# Visualising UKCEH Land Cover Class using a GIS application

- Data structure
  - 20m and 10m rasters: two bands
    - Band 1 = UKCEH Land Cover Class identifier
    - Band 2 = classification confidence
  - 25m rasters: three bands
    - Band 1 = dominant UKCEH Land Cover Class identifier
    - Bands 2–3 = indicators of classification confidence
- Purpose
  - Short guide for visualising the Land Cover Class data contained in band 1 using commonly used GIS applications
  - Full data description available in the product documentation
- General approach
  - Visualise Band 1 values using thematic (unique values) rendering
  - Use accompanying style/configuration files to ensure consistent classification colours

## Visualising the data using QGIS

- Add the file to the project; the layer appears in the layers panel
- Open layer properties → Symbology
- Render type: Paletted/Unique values
- Band: Band 1
- Click Style → Load style from the menu
- Browse to LCMcolours_QGIS.qml that accompanies this document, select it, and open
- Click OK to redraw the map with the correct classification

## Visualising the data using ArcGIS Desktop

- In the Catalog window, browse to the folder containing the data
- Expand the file to display the raster bands
- Drag band_1 into the Table of Contents
- Double-click the layer name in the Table of Contents to open Layer Properties
- Symbology tab → Unique Values (if prompted to calculate values, click YES)
- Click Import → load the layer file (LCMcolours.lyr) provided with these instructions
- Click OK to redraw the map with the correct classification

## Visualising the data using ArcGIS Pro

- In the Catalog window, browse to the folder containing the data
- Expand the file to display the raster bands
- Drag band_1 into the Table of Contents
- Double-click the layer in the Table of Contents to open Layer Properties
- In Contents, open Appearance → Symbology
- Primary symbology: Unique Values (if prompted to build an attribute table, click Yes)
- Open the hamburger menu in the Symbology panel → Import
- Load the layer file (LCMcolours.lyr) provided with these instructions
- The map will be redrawn with the correct classification

## Additional notes

- The LCMcolours style/file accompanies these instructions and should be used to ensure consistent visualisation across applications
- For a full description of the data (including band definitions and resolutions), refer to the product documentation