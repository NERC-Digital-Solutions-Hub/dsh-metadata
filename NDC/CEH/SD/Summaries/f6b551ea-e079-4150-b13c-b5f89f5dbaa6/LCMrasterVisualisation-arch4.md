# Visualising UKCEH Land Cover Class using a GIS application

## Overview
- Land cover map rasters for 2017–2020 are multiband rasters.
- 20m and 10m rasters: two bands (Band 1 = UKCEH Land Cover Class identifier; Band 2 = classification confidence).
- 25m rasters: three bands (Band 1 = dominant Land Cover Class identifier; Bands 2–3 = classification confidence indicators).
- This short guide explains how to visualise the Land Cover Class data using Band 1 in common GIS applications; refer to the product documentation for full data details.

## Visualising in common GIS tools

### QGIS
- Add the file to your project; layer appears in the layers panel.
- Double-click the layer name to open Layer Properties → Symbology.
- Render as Paletted/Unique Values; select Band 1.
- Click Style → Load style from the menu; browse to LCMcolours_QGIS.qml that accompanies this document, select and open.
- Click OK to redraw the map with the correct classification.

### ArcGIS Desktop
- In the Catalogue window, navigate to the data folder and expand the raster to show its bands.
- Drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties → Symbology.
- Choose Unique Values (accept prompts to build values if needed).
- Click Import and load the provided LCMcolours.lyr file.
- Click OK to redraw the map with the correct classification.

### ArcGIS Pro
- In the project, open Catalog and browse to the data folder.
- Expand the raster to display bands; drag band_1 into the Table of Contents.
- Double-click the layer name to open Layer Properties; in Contents, select the layer and open Appearance → Symbology.
- Set Primary Symbology to Unique Values (answer Yes if prompted to build an attribute table).
- Use the hamburger menu in the Symbology panel → Import; load LCMcolours.lyr to redraw the map with the correct classification.

## Data details and usage notes
- The guide focuses on visualising Band 1 across the supported GIS platforms.
- For full data descriptions and metadata, refer to the product documentation.
- The accompanying colour/style files (LCMcolours_QGIS.qml and LCMcolours.lyr) ensure consistent classification visuals across platforms.

## Implications for Data Leaders
- Standardised, cross-platform visualization supports consistent communication of land cover data to policy colleagues and partners.
- Clear band definitions and provided style files aid discoverability and reuse, aligning with governance of data assets and dissemination practices.
- Emphasises the importance of accompanying metadata and documentation to support effective data utilisation and stakeholder engagement.