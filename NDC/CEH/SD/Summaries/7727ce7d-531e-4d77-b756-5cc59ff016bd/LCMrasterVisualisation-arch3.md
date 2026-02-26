# Visualising UKCEH Land Cover Class using a GIS application

- This is a short guide for visualising the Land Cover Class data contained in band 1 of UKCEH rasters, using common GIS applications.
- Data structure varies by spatial resolution:
  - 20m and 10m rasters: two bands (Band 1 = Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant Land Cover Class identifier; Bands 2–3 = indicators of classification confidence).
- A full description of the data is available in the product documentation.
- Style files accompany the document to standardise visuals:
  - QGIS: LCMcolours_QGIS.qml
  - ArcGIS: LCMcolours.lyr

## Visualization focus

- The guide provides instructions to visualise the Land Cover Class data in band 1 using three popular GIS tools.
- Visuals are designed to present a clear, consistent classification map suitable for monitoring outputs and reporting.

## Visualisation steps by software

### Visualising with QGIS
- Add the Land Cover data file to your project; the layer appears in the layers panel.
- Open the layer's properties and choose Symbology.
- Set render type to Paletted/unique values; select Band 1.
- Click the style button, choose Load style, and load LCMcolours_QGIS.qml.
- Click OK to redraw the map with the correct classification.

### Visualising with ArcGIS Desktop
- In the Catalog, navigate to the data folder and expand the raster to view its bands.
- Drag band_1 into the Table of Contents.
- Open the layer properties and go to the Symbology tab.
- Choose Unique Values; if prompted to build an attribute table, click YES.
- Click the Import button and load LCMcolours.lyr.
- Click OK to redraw the map with the correct classification.

### Visualising with ArcGIS Pro
- In the Catalog, navigate to the data folder and expand the raster’s bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open properties, then Appearance > Symbology.
- In Primary Symbology, choose Unique values (if prompted to build a table, click Yes).
- Use the hamburger menu in the Symbology panel and select Import; load LCMcolours.lyr.
- The map will redraw with the correct classification.

## Notes for practitioners

- The guide focuses on visualising Band 1; refer to the product documentation for full data details.
- The accompanying style files are essential for achieving consistent, publication-ready visuals across platforms and analyses.