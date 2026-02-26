# Visualising UKCEH Land Cover Class using a GIS application

- The 2021 Land cover map rasters are multiband:
  - 10m rasters have two bands: Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence.
  - 25m rasters have three bands: Band 1 = dominant UKCEH Land Cover Class identifier; Bands 2 and 3 = classification confidence indicators.
- The guide focuses on visualising data using Band 1.
- For a full data description, refer to the product documentation.

## Visualising the data using QGIS

- Add the file to your project; the layer appears in the layers panel.
- Open layer properties and choose Symbology.
- In Render type, select Paletted/Unique Values; in Band, choose Band 1.
- Click the style button and choose Load style from the menu.
- Load the accompanying LCMcolours_QGIS.qml file and apply; the map redraws with the correct classification.

## Visualising the data using ArcGIS Desktop

- In the Catalogue, locate the data folder and expand the raster’s bands.
- Drag Band 1 into the Table of Contents.
- Open the layer properties and go to the Symbology tab; choose Unique Values.
- If prompted, click Yes to build an attribute table.
- Click Import and load the provided LCMcolours.lyr file; the map redraws with the correct classification.

## Visualising the data using ArcGIS Pro

- In the project Catalog, locate the data folder and expand the raster’s bands.
- Drag Band 1 into the Table of Contents.
- Open layer properties (Appearance > Symbology).
- In Primary Symbology, select Unique Values.
- Use the Import option from the menu to load LCMcolours.lyr; the map redraws with the correct classification.

## Data governance and reuse considerations for Data Leaders

- The visualization relies on a consistent classification scheme (Band 1) and standardized color styles (LCMcolours files) to ensure interoperability across GIS tools.
- The accompanying style files (QGIS and ArcGIS) support repeatable, shareable visual representations, aiding discoverability and governance of data products.
- The guide emphasizes practical steps to establish consistent visual outputs, aligning with data strategy objectives to verify data suitability, maintain metadata, and support user-centric data products.