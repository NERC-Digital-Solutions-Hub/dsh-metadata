# July Image Metadata

- Overview
  - Imagery acquired on 4 July 2019 at a farm in Northamptonshire, UK.
  - Two spatial resolutions: 3 cm and 7 cm.
  - Equipment: Hasselblad A6D-100c (50 mm) cameras with Bayer filters on a Sky Arrow 650 aircraft.
  - Each image is a 16-bit orthomosaic using OSGB 1936 / British National Grid (EPSG: 27700).

- Data sets and formats
  - July_3cm: clipped 4-band 3 cm resolution image used for classifications. Bands are blue, green, red, infrared mapped to B0, B1, B2, B3.
  - 04_07_2019_6_Band_3: original 3 cm data across 6 bands (band data details in Table_band_data).
  - July_7cm: original 7 cm data for July across 6 bands; file named 04_07_2019_6_Band_7_BIL.
  - Clipped 4-band 7 cm image used for classifications (bands B0-B3).
  - The original 7 cm 6-band image for July.
  - For per-band details, see Table_band_data in the main Mapping nectar-rich floral resources for pollinators folder.

- Bands and mapping
  - 4-band classification-ready images use: blue (B0), green (B1), red (B2), infrared (B3).

- Documentation and data dictionary
  - Band-specific data described in Table_band_data within the Mapping nectar-rich floral resources for pollinators folder.

- Data usage notes for data support
  - Supports data discovery, integration, and preparation for analyses and dashboards related to pollinator floral resource mapping.
  - Enables end users to self-serve with classification-ready TIFFs and original multi-band datasets.
  - Useful for cross-resolution comparisons (3 cm vs 7 cm) and for quality assurance through metadata consistency.

- Considerations for data support
  - Ensure consistent interpretation of B0–B3 across datasets.
  - Maintain clear linkage between clipped classification-ready images and their original multi-band counterparts.
  - Verify documentation availability (Table_band_data) and keep naming conventions and folder structure clear for reuse.