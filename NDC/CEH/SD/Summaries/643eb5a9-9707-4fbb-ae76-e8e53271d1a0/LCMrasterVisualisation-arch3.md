# Visualising UKCEH Land Cover Class using a GIS application

## Purpose and scope
- Short guide for visualising Land Cover Class data contained in band 1 of UKCEH land cover rasters (2017–2020).
- Data vary by resolution: 20m and 10m rasters have two bands (Band 1: class identifier; Band 2: classification confidence), 25m rasters have three bands (Band 1: dominant class; Bands 2–3: confidence indicators).
- Intended for use with common GIS applications to produce clear visual representations of land cover classifications.

## Data structure and meaning
- Band 1 in all rasters contains the UKCEH Land Cover Class identifier used for visualization.
- Bands 2 and 3 (where present) provide indicators of classification confidence.
- Full data description available in the product documentation.

## How to visualize (by software)

### QGIS
- Add the file to your project.
- Open layer properties and select Symbology.
- Set render type to Paletted/Unique Values and choose Band 1.
- Load the provided LCMcolours_QGIS.qml style file to display correct classification.

### ArcGIS Desktop
- In the Catalog, locate the data folder, then expand the raster and drag Band_1 into the Table of Contents.
- Open Layer Properties > Symbology > Unique Values (if prompted to calculate values, click YES).
- Import the provided LCMcolours.lyr and apply.
- Map will redraw with the correct classification.

### ArcGIS Pro
- In the Catalog, locate the data folder and reveal the raster bands.
- Drag Band_1 into the Table of Contents.
- Open Layer Properties > Appearance > Symbology; select Unique Values.
- Use the hamburger menu in the Symbology panel to Import LCMcolours.lyr.
- Map will redraw with the correct classification.

## Styling files and outputs
- Use the accompanying style files (LCMcolours_QGIS.qml for QGIS and LCMcolours.lyr for ArcGIS) to ensure consistent, official classification visuals across platforms.
- The resulting map reflects the standardized Land Cover Class visualisation.

## Relevance for monitoring framework authors
- Provides a standardized, reproducible method to visualize environmental health classifications, aiding scrutiny and policy evaluation.
- The inclusion of confidence indicators (Bands 2/3 where available) supports assessment of data quality and reliability in monitoring outputs.
- Predefined styling promotes consistent communication of findings to stakeholders, reducing misinterpretation.
- Encourages transparency and ease of data governance by enabling straightforward replication of visual outputs across tools.