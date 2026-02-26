# Visualising UKCEH Land Cover Class using a GIS application

## Purpose and scope
- Short guide for using common GIS applications to visualize Land Cover Class data contained in band 1.
- Data covered: land cover map rasters for 2017–2020, multi-band rasters with:
  - 20m and 10m datasets: two bands (Band 1 = Land Cover Class identifier; Band 2 = classification confidence)
  - 25m datasets: three bands (Band 1 = dominant Land Cover Class identifier; Bands 2–3 = classification confidence indicators)
- For a full data description, refer to the product documentation.

## Data structure
- Band 1 holds the primary land cover class identifier.
- Additional bands (2 and 3, where present) provide classification confidence indicators.
- Multiple resolutions (20m, 10m, 25m) with corresponding band configurations.

## Visualising in QGIS
- Add the file to your project; the layer appears in the layers panel.
- Open layer properties and select Symbology.
- Set render type to Paletted/Unique Values and choose Band 1.
- Load the accompanying style: LCMcolours_QGIS.qml to apply correct classification colors.
- The map will redraw with the correct classification.

## Visualising in ArcGIS Desktop
- In the Catalogue, locate the data folder and expand to view raster bands.
- Drag Band_1 into the Table of Contents.
- Open layer properties and go to Symbology; choose Unique Values.
- If prompted, allow value calculation to proceed.
- Use Import to load the provided style: LCMcolours.lyr, then OK to redraw with correct classification.

## Visualising in ArcGIS Pro
- Open the catalogue in your ArcGIS Pro project and navigate to the data folder.
- Expand the raster bands and drag Band_1 into the Table of Contents.
- Open layer properties and set Symbology to Unique Values (If prompted to build an attribute table, choose Yes).
- Use the hamburger menu in the Symbology panel and choose Import.
- Load the provided style: LCMcolours.lyr; the map updates to show the correct classification.

## Metadata, documentation and governance notes
- The guide emphasizes using standard, accompanying style files to ensure consistent visualization across tools.
- For data interpretation and full specifications, consult the product documentation.
- Providing standardized visualization styles supports transparency and comparability in monitoring outputs.