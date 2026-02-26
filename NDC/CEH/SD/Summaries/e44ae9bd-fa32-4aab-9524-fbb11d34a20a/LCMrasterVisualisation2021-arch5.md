# Visualising UKCEH Land Cover Class using a GIS application

## Purpose and data structure
- Short guide for visualising Land Cover Class data from UKCEH in common GIS applications.
- Data specifics:
  - 10 m raster: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
  - 25 m raster: three bands (Band 1 = dominant Land Cover Class identifier; Bands 2 and 3 = classification confidence).
- Focus is on visualising Band 1; refer to the full product documentation for a complete data description.

## Visualisation workflow by GIS platform

### QGIS
- Add the file to your project; layer appears in the layers panel.
- Open layer properties, select Symbology.
- Render as Paletted/Unique values, Band 1.
- Load styling: LCMcolours_QGIS.qml (provided with the document).
- Map updates to show correct classification.

### ArcGIS Desktop
- In Catalog, locate the data folder and expand the raster to reveal bands.
- Drag Band 1 into the Table of Contents.
- Layer properties → Symbology → Unique Values.
- Import: load LCMcolours.lyr (provided with the instructions).
- Map updates to show correct classification.

### ArcGIS Pro
- Open Catalog, locate data folder, expand to view raster bands.
- Drag Band 1 into the Table of Contents.
- Layer properties → Appearance → Symbology → Unique Values.
- If prompted, build an attribute table (Yes).
- Use the Import option in the symbology panel to load LCMcolours.lyr.
- Map updates to show correct classification.

## Additional notes for data governance and reuse
- The guide includes recommended style files (LCMcolours_QGIS.qml and LCMcolours.lyr) to ensure consistent visualization across platforms, supporting reproducibility and discoverability of the data.
- Although focused on visualization, using standard styles aids data users in correctly interpreting classifications, aligning with data stewardship goals for accurate, interim or published maps.

## References and provenance
- For a full description of the data, consult the product documentation.
- The accompanying style files are provided with these instructions to maintain consistent rendering across GIS tools.