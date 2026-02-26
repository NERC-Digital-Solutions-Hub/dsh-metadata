# March Image Metadata

## Overview
- Imagery acquired at a farm in Northamptonshire, UK on 28 March 2019 at 3 cm and 7 cm spatial resolutions.
- Captured with Hasselblad A6D-100c (50 mm) cameras using Bayer filters.
- Mounted on a Sky Arrow 650 manned aircraft.
- Each image is a 16-bit orthomosaic with coordinate reference system OSGB 1936 / British National Grid (EPSG: 27700).

## Datasets and formats
- March_3cm.tif: clipped 4-band 3 cm resolution image used for classifications (bands correspond to blue, green, red, infrared; B0–B3).
- 28_03_2019_6_Band_3.tif: original 3 cm data for March across 6 bands.
- March_7cm.tif: clipped 4-band 7 cm resolution image used for classifications (bands B0–B3: blue, green, red, infrared).
- 28_03_2019_6_Band_7_BIL.tif: original 7 cm data for March across 6 bands.
- Table_band_data: per-band data referenced from the main folder “Mapping nectarrich floral resources for pollinators.”

## Spatial, spectral, and projection details
- 16-bit imagery.
- Spatial resolutions: 3 cm and 7 cm.
- Coordinate reference system: EPSG: 27700 (OSGB 1936 / British National Grid).

## Band information
- 4-band clips (B0 blue, B1 green, B2 red, B3 infrared) used for classifications.
- 6-band originals cover additional bands, with band data documented in Table_band_data.

## Metadata references and data lineage
- Band details and data lineage documented in Table_band_data within the main dataset folder.
- Classification-ready products (3 cm and 7 cm) are provided as clipped 4-band TIFFs; originals maintained as 6-band TIFFs for provenance.

## Data governance and stewardship considerations
- Ensure consistent metadata across all files, including band mapping (B0–B3) and CRS.
- Maintain linkage between clipped classification products and their corresponding original 6-band datasets via Table_band_data.
- Preserve both original and clipped datasets to support traceability and reproducibility.
- Facilitate discoverability by cataloguing these datasets with their spatial resolution, bands, CRS, and provenance details (farm location, date, platform).
- Manage access and sharing in line with any data sharing limitations; document any transformations (e.g., clipping) performed prior to sharing.

## Provenance and storage notes
- Data originate from a single acquisition event (28 March 2019) at Northamptonshire, UK, using a consistent platform and camera setup.
- Files are organized to support both classification workflows (4-band clips) and full spectral analysis (6-band originals).