# Visualising UKCEH Land Cover Class using a GIS application

- The Land cover map rasters for 2017-2020 come in multiband rasters with different band configurations by resolution:
  - 20m and 10m rasters: two-band files (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25m rasters: three-band files (Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence indicators).
- This document is a short guide for visualising the Land Cover Class data contained in Band 1 using common GIS applications. Refer to the full product documentation for complete data descriptions.

## Data structure and purpose
- Band 1 contains the land cover class identifier to be visualised.
- Bands 2 and 3 (for 25m) or Band 2 (for 20m/10m) provide classification confidence indicators.
- The guide focuses on applying the correct visual classification (colors) to Band 1 to interpret land cover.

## Visualisation workflow (summary)
- Load data into your GIS project, then apply a predefined color scheme to Band 1 so that each Land Cover Class is distinctly represented.

## Software-specific instructions

- Visualising the data using QGIS
  - Add the file to your project; layer appears in the layers panel.
  - Open Layer Properties → Symbology.
  - Render as Paletted/Unique Values, Band 1.
  - Load the style file LCMcolours_QGIS.qml, then OK to redraw with correct classification.

- Visualising the data using ArcGIS Desktop
  - In Catalog, locate the data folder; expand the raster to reveal bands.
  - Drag band_1 into the Table of Contents.
  - Layer Properties → Symbology → Unique Values (if prompted to calculate values, click YES).
  - Click Import and load LCMcolours.lyr, then OK to redraw with correct classification.

- Visualising the data using ArcGIS Pro
  - In Catalog, locate the data folder; expand to view raster bands.
  - Drag band_1 into the Table of Contents.
  - Layer Properties → Symbology (Appearance → Symbology) → Primary: Unique Values.
  - Use the Import option (hamburger menu) to load LCMcolours.lyr, then the map will display the correct classification.

## Additional notes for monitoring framework authors
- The guide emphasizes using a consistent, predefined color scheme to ensure comparability across datasets and analyses.
- While focusing on visualisation, it implicitly supports governance and transparency by enabling clear, shareable representations of land-cover classifications.
- For comprehensive data details (definitions, metadata, and quality considerations), refer to the full product documentation.