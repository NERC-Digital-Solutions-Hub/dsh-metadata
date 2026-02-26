# March Image Metadata

## Overview
- Imagery acquired at a farm in Northamptonshire, UK on 28 March 2019
- Captured at two spatial resolutions: 3 cm and 7 cm
- Collected with Hasselblad A6D-100c (50mm) cameras with Bayer filters
- Mounted on a Sky Arrow 650 manned aircraft
- Each image is a 16-bit orthomosaic
- Coordinate reference system: OSGB 1936 / British National Grid (EPSG: 27700)

## Data assets and file formats
- March_3cm.tif: clipped 4-band 3cm resolution image used for classifications (bands B0, B1, B2, B3 corresponding to blue, green, red, infrared)
- 28_03_2019_6_Band_3.tif: original 3cm data across 6 bands (band data described in Table_band_data)
- March_7cm.tif: clipped 4-band 7cm resolution image used for classifications (bands B0, B1, B2, B3)
- 28_03_2019_6_Band_7_BIL.tif: original 7cm data across 6 bands
- Band data details for all images are available in Table_band_data in the main folder "Mapping nectarrich floral resources for pollinators"

## Processing and usage notes
- Some images are clipped for classification tasks
- Original datasets include 6 spectral bands at each resolution
- Band naming uses B0–B3 for the 4-band classifications (blue, green, red, NIR)

## Provenance and metadata context
- Location: Northamptonshire farm
- Capture date: 28 March 2019
- References to accompanying Table_band_data for band-specific details

## Relevance for Data Leaders
- Demonstrates organized handling of multi-resolution, multi-band imagery
- Clear file naming and processing status (clipped vs original) supports discoverability and reproducibility
- CRS and 16-bit depth enable interoperability and downstream analysis
- Centralized table reference (Table_band_data) aids standardization across datasets and partners
- Provides a solid basis for data governance, lineage, and metadata completeness in spatial data projects