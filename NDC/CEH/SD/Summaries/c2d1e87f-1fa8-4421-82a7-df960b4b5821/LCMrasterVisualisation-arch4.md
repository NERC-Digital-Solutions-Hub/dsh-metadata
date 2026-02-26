# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Short guide for visualising Land Cover Class data contained in band 1 of UKCEH Land Cover Map rasters.
- Band structure by resolution:
  - 20m and 10m rasters: two bands (Band 1 = class identifier; Band 2 = classification confidence).
  - 25m rasters: three bands (Band 1 = dominant class identifier; Bands 2–3 = classification confidence).
- Intended for common GIS applications; full data description available in the product documentation.
- Uses companion style files to ensure consistent classification visuals across platforms.

## Data structure and purpose
- Band 1 always contains the Land Cover Class identifier.
- Band 2 (and Band 3 for 25m) provide indicators of classification confidence.
- Visualisation focuses on Band 1 for the classification display; confidence bands support interpretation.

## Visualising the data by application

- Visualising with QGIS
  - Add the file to your project; layer appears in the layers panel.
  - Open layer properties -> Symbology -> Paletted/Unique values -> Band 1.
  - Click the style button -> Load style from LCMcolours_QGIS.qml provided with the document.
  - OK to redraw the map with correct classification.

- Visualising with ArcGIS Desktop
  - In Catalog, locate data folder, expand raster bands, drag band_1 to the Table of Contents.
  - Layer properties -> Symbology -> Unique Values (if prompted, choose YES to build attribute table).
  - Import button -> load LCMcolours.lyr provided with the instructions.
  - OK to redraw the map with correct classification.

- Visualising with ArcGIS Pro
  - In Catalog, locate data folder, expand raster bands, drag band_1 to Table of Contents.
  - Layer properties -> Appearance -> Symbology -> Primary: Unique Values (Yes to build attribute table if prompted).
  - Use the hamburger menu in the Symbology panel -> Import -> load LCMcolours.lyr.
  - Map refreshes with correct classification.

## Style files and resources
- LCMcolours_QGIS.qml for QGIS visualization.
- LCMcolours.lyr for ArcGIS Desktop/Pro visualization.
- Both accompany the instructions document.

## Implementation notes
- Visualisation uses Band 1 to display Land Cover Class classifications; confidence bands (Bands 2/3) are available for interpretation.
- Full data description and specifics are available in the product documentation.

## Relevance for Data Leaders
- Facilitates consistent, cross-platform visualization of land cover classifications, aiding data governance and communication.
- Supports user-centric data products by enabling straightforward, repeatable visualization workflows.
- Enhances transparency and discoverability of classification results through standardized styles and metadata cues.
- Helps ensure reproducibility and alignment with data quality and presentation standards across teams and partners.