# May Image Metadata

## Overview
- Imagery acquired at a farm in Northamptonshire, UK on 14th/15th May 2019.
- Captured at two spatial resolutions: 3 cm and 7 cm.
- Sensor setup: Hasselblad A6D-100c (50mm) cameras with Bayer filters mounted on a Sky Arrow 650 manned aircraft.
- Each image is a 16-bit orthomosaic.
- Coordinate reference system: OSGB 1936 / British National Grid (EPSG: 27700).

## Dataset Components and File Descriptions
- May_3cm: TIFF with a clipped 4-band 3 cm resolution image used for classifications. Bands are blue (B0), green (B1), red (B2), and infrared (B3). See Table_band_data in the Mapping nectar-rich floral resources for pollinators folder for band specifics.
- 14_05_2019_6_Band_3: TIFF containing the 3 cm data for May across 6 bands.
- May_7cm: TIFF containing the original 7 cm data for May across 6 bands.
- 14_05_2019_6_Band_7_BIL: TIFF containing the original 7 cm 6-band image (BIL format).
- The original 7 cm 6-band image for May: additional detail referenced in Table_band_data.
- All band data references and specifics are documented in Table_band_data within the main project folder: Mapping nectar-rich floral resources for pollinators.

## Sensor, Resolution, and Band Details
- 3 cm data: 6-band data available; 4-band subset (May_3cm) used for classifications.
- 7 cm data: 6-band data available; 4-band subset (May_7cm) used for classifications.
- Bands identified:
  - 4-band subset: blue (B0), green (B1), red (B2), infrared (B3).
  - 6-band full sets available for both 3 cm and 7 cm resolutions.
- All images are tied to the same project context: Mapping nectar-rich floral resources for pollinators.

## Data Governance and Stewardship Considerations
- Provenance: images originate from a single field campaign in May 2019; linked to the Mapping nectar-rich floral resources for pollinators project.
- Metadata completeness: ensure Table_band_data provides per-band details (wavelengths, radiometric calibration, processing steps).
- File naming and organization: consistent naming conventions for 3 cm and 7 cm datasets; keep links to the exact band data entries in Table_band_data.
- Data formats: uses TIFF and BIL formats; verify interoperability with target GIS/remote sensing workflows.
- Classification readiness: May_3cm and May_7cm are clipped 4-band products intended for classification workflows; maintain traceability to source data and processing steps.
- Documentation: maintain references to the main folder and metadata about how the 3 cm and 7 cm datasets were generated (clipping, band selection).

## Quality, Access, and Update Considerations
- Data quality: provide explicit notes on clipping process, band alignment, and any radiometric corrections applied; verify alignment between 3 cm and 7 cm datasets.
- Access and sharing: ensure metadata (including CRS and band mappings) is accessible to data users; confirm licensing or usage terms within the project documentation.
- Updates: any future revisions should clearly indicate dataset versioning and link to corresponding entries in Table_band_data.