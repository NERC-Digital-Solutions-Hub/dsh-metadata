# May Image Metadata

## Overview
- Imagery acquired at a farm in Northamptonshire, UK, on 14–15 May 2019.
- Platforms and sensors: Hasselblad A6D-100c cameras (50mm) mounted on a Sky Arrow 650 aircraft.
- Data type: 16-bit orthomosaic images.
- Coordinate reference system: OSGB 1936 / British National Grid (EPSG: 27700).
- Resolutions: 3 cm and 7 cm spatial resolutions.
- Purpose: metadata and datasets intended for mapping nectar-rich floral resources for pollinators; used in GIS to classify and map floral resources.

## Datasets and File Descriptions
- May_3cm: Tiff file with clipped 4-band 3 cm resolution image used for classifications.
  - Bands: blue (B0), green (B1), red (B2), infrared (B3).
  - Reference: Table_band_data in the Mapping nectar-rich floral resources for pollinators folder.
- 14_05_2019_6_Band_3: Original 3 cm data for May across 6 bands.
  - Individual band data available in Table_band_data.
- May_7cm: Tiff file with clipped 4-band 7 cm resolution image used for classifications.
  - Bands: blue (B0), green (B1), red (B2), infrared (B3).
  - Reference: Table_band_data in the Mapping nectar-rich floral resources for pollinators folder.
- 14_05_2019_6_Band_7_BIL: Original 7 cm data for May across 6 bands.
  - Individual band data available in Table_band_data.
- The listing also notes the existence of the original 7 cm 6-band image for May in the same data folder.

## Image Specifications and Band Details
- Clipped classification images:
  - 3 cm: 4-band (B0–B3) TIFF, suitable for classifications.
  - 7 cm: 4-band (B0–B3) TIFF, suitable for classifications.
- Original imagery:
  - 3 cm: 6-band TIFF (B0–B5), full bit depth; per-band details in Table_band_data.
  - 7 cm: 6-band TIFF (B0–B5), full bit depth; per-band details in Table_band_data.
- All images are georeferenced to OSGB 1936 / British National Grid (EPSG: 27700).

## Data Organization and GIS Considerations
- Data is organized under the main project folder “Mapping nectar-rich floral resources for pollinators,” with a companion Table_band_data file outlining band data per image.
- For GIS workflows:
  - Ensure proper loading of both clipped (classification-ready) and original multispectral datasets.
  - Maintain consistent band order (B0–B3 for 4-band products; B0–B5 for 6-band originals) when performing analysis.
  - Reproject if needed only after verifying CRS (27700) to avoid misalignment with other datasets.
- These datasets enable spatial analysis and visualization of nectar-rich floral resources at high spatial resolutions (3 cm and 7 cm).