# Visualising UKCEH Land Cover Class using a GIS application

- Purpose: Short guide for visualising UKCEH Land Cover Class data contained in band 1 of land cover rasters (2017–2020) using common GIS applications.
- Data structure:
  - 20m and 10m rasters: two bands — Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence indicator.
  - 25m rasters: three bands — Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2–3 = classification confidence indicators.
- Main goal: Visualise the Land Cover Class data in band 1; for a full data description, refer to the product documentation.

## Visualising the data using QGIS

- Add the file to your project; the layer appears in the layers panel.
- Open layer properties and select Symbology.
- Set Render type to Paletted/Unique values and choose Band 1.
- Click the style (Load style) option, browse to LCMcolours_QGIS.qml that accompanies the document, select and open.
- Click OK; the map redraws with the correct classification.

## Visualising the data using ArcGIS Desktop

- In the Catalog window, browse to the folder containing the data.
- Expand the raster to display its bands; drag band_1 into the Table of Contents.
- Open the layer properties, go to the Symbology tab, and choose Unique Values (if prompted to build values, click YES).
- Click the Import button and load the provided layer file (LCMcolours.lyr).
- Click OK; the map redraws with the correct classification.

## Visualising the data using ArcGIS Pro

- In ArcGIS Pro, open the Catalog and browse to the data folder.
- Expand the file to view the raster bands and drag band_1 into the Table of Contents.
- Open the layer’s properties (Contents) and go to Appearance > Symbology.
- In Primary Symbology, choose Unique Values (if prompted to build an attribute table, click Yes).
- Use the hamburger menu in the Symbology panel and select Import; load LCMcolours.lyr provided with the instructions.
- The map will be redrawn with the correct classification.

- Note: LCMcolours files are provided to apply consistent classification styling; for a full description of the data, refer to the product documentation.