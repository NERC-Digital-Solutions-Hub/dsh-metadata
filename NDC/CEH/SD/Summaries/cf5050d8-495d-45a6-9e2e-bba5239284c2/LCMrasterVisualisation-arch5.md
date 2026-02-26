# Visualising UKCEH Land Cover Class using a GIS application

- Purpose: A short guide for visualising the Land Cover Class data (band 1) from UKCEH rasters (2017–2020) in common GIS applications.
- Data structure: 
  - 20 m and 10 m rasters have two bands: Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
  - 25 m rasters have three bands: Band 1 = dominant Land Cover Class identifier; Bands 2–3 = confidence indicators.
- Visualization focus: Uses band 1 to display classification; full data description available in product documentation.
- Standardisation: Uses provided colour/style files to ensure consistent classification presentation across tools.

## Visualising with QGIS

- Add the file to your project; layer appears in the layers panel.
- Layer properties > Symbology:
  - Render type: Paletted/unique values
  - Band: Band 1
- Click Style > Load style, browse to LCMcolours_QGIS.qml, open, then OK.
- Result: map redraws with correct classification.

## Visualising with ArcGIS Desktop

- In Catalog, locate the data folder, expand the raster to view its bands.
- Drag band_1 into the Table of Contents.
- Layer properties > Symbology:
  - Type: Unique Values
- If prompted to calculate values, click YES.
- Click Import and load LCMcolours.lyr (provided with this guide).
- Result: map redraws with correct classification.

## Visualising with ArcGIS Pro

- In Catalog, navigate to the data folder and expand the raster bands.
- Drag band_1 into the Contents pane.
- Layer properties > Symbology:
  - Primary: Unique values
- Use the hamburger menu in the Symbology panel > Import.
- Load LCMcolours.lyr (provided with these instructions).
- Result: map redraws with correct classification.

## Governance and reuse notes for Data Stewards

- The guide promotes interoperable visualization across platforms, aiding dataset discoverability and usability.
- Use of standard colour/style files (LCMcolours_QGIS.qml, LCMcolours.lyr) ensures consistent interpretation of classifications.
- For complete dataset details and usage notes, refer to the full product documentation.
- Ensure that any updates to the dataset maintain consistency with the provided styling files to preserve reproducibility.