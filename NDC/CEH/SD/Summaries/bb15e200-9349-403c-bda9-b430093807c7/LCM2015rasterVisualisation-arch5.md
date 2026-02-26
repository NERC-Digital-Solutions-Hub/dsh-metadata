# Visualising UKCEH Land Cover 2015 class using a GIS application

- Purpose: Short guide to visualise Land Cover Class data contained in band 1 of the 2015 25m raster using common GIS applications.
- Dataset structure: The 2015 raster has two bands; band 1 contains the classification, band 2 contains the mean per-polygon probability produced by the classification algorithm.
- Platforms covered: QGIS and ArcGIS Desktop.
- Key approach: Use band 1 with unique value or paletted symbology, applying standard colours from the product documentation to produce a correct visual classification.
- Additional reference: For full data description and colour recipes, refer to the product documentation.

## Visualising in QGIS

- Add the file to your project; the layer appears in the layers panel.
- Double-click the layer name to open layer properties.
- In Symbology, set Render type to Paletted/Unique Values.
- Select Band 1.
- Click Classify.
- Colours will be assigned to each land class; edit colours as needed using the colour recipe from the product documentation.
- Click OK to redraw the map with the correct classification.

## Visualising in ArcGIS Desktop

- In the Catalogue window, browse to the data folder.
- Expand the raster to display its bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer to open Layer Properties; go to the Symbology tab.
- Choose Unique Values as the symbology type (if prompted to recalculate values, click YES).
- Assign appropriate colours using the colour recipe from the product documentation.
- Click OK to redraw the map with the correct classification.

## Additional notes for data stewardship

- The guide is intended to enable consistent visualization across GIS platforms, supporting governance of how Land Cover classes are displayed.
- Ensure the color mappings and classification scheme are documented (refer to the product documentation) to maintain reproducibility.
- When sharing datasets, reference the same band usage (band 1 for classification) and provide the visualization workflow to facilitate reuse.