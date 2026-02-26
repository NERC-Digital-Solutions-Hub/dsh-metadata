# July Image Metadata

## Overview
- Imagery collected on 4 July 2019 in Northamptonshire, UK, at 3 cm and 7 cm spatial resolutions.
- Sensor: Hasselblad A6D-100c (50 mm) with Bayer filters, mounted on a Sky Arrow 650 aircraft.
- Data are 16-bit orthomosaics in OSGB 1936 / British National Grid (EPSG: 27700).

## Data Products and Formats
- July_3cm: TIFF, clipped 4-band 3 cm resolution, used for classifications; bands are blue, green, red, infrared (B0–B3). Band data described in Table_band_data within the Mapping nectar-rich floral resources for pollinators folder.
- 04_07_2019_6_Band_3: TIFF, original 3 cm data across 6 bands; detailed band data in Table_band_data.
- July_7cm: TIFF, clipped 4-band 7 cm resolution, used for classifications (B0–B3: blue, green, red, infrared).
- 04_07_2019_6_Band_7_BIL: TIFF, original 7 cm data across 6 bands; band data available in Table_band_data.

## Metadata and Documentation
- Data associated with the main folder: Mapping nectar-rich floral resources for pollinators.
- Per-band data and specifics are provided in Table_band_data; filenames indicate resolution and band configuration to aid discoverability and reuse.

## Coordinate Reference System and Spatial Details
- All products aligned to OSGB 1936 / British National Grid (EPSG: 27700).

## Data Governance and Stewardship Considerations
- Clear provenance: acquisition date, platform, sensor, and flight context are documented.
- Multiple resolutions and band configurations demand consistent metadata across products to ensure interoperability.
- Metadata completeness relies on Table_band_data; ensure linkage and versioning are maintained.
- Large data volumes (6-band originals and clipped 4-band classifications) require robust storage, cataloging, and access controls.

## Data Access, Licensing and Storage
- Data are delivered as TIFF (and BIL where applicable); references to classifications datasets imply downstream use for analysis and mapping.
- Ensure portal-level cataloging with proper naming conventions and folder structure for discoverability and reuse.

## Actions for Data Stewards
- Verify and capture all metadata fields: acquisition date, platform, sensor, spatial resolution, CRS, band mapping, file formats, and dataset relationships.
- Confirm presence and content of Table_band_data and ensure it aligns with the actual bands in each product.
- Catalogue datasets in the appropriate data portal with clear provenance and usage notes.
- Document data processing steps (e.g., clipping, orthomosaic creation) for transparency and reproducibility.
- Plan for storage and access management given the dataset sizes and multiple resolutions.