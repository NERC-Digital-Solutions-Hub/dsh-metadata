# March Image Metadata

- Purpose and scope: Metadata describing March imagery used to map nectar-rich floral resources for pollinators, including both high-resolution (3 cm) and lower-resolution (7 cm) orthomosaic data.

- Acquisition details:
  - Date and location: 28 March 2019, Northamptonshire, UK.
  - Sensor and platform: Hasselblad A6D-100c (50 mm) cameras on a Sky Arrow 650 manned aircraft.
  - Image type: 16-bit orthomosaic with OSGB 1936 / British National Grid (EPSG: 27700).

- Data products and formats:
  - 3 cm resolution:
    - March_3cm.tif: clipped 4-band image (Blue, Green, Red, Infrared) for classifications.
    - 28_03_2019_6_Band_3.tif: original 3 cm data across 6 bands.
  - 7 cm resolution:
    - March_7cm.tif: clipped 4-band image (Blue, Green, Red, Infrared) for classifications.
    - 28_03_2019_6_Band_7_BIL.tif: original 7 cm data across 6 bands.
  - Band mapping: 4-band images correspond to B0 (Blue), B1 (Green), B2 (Red), B3 (Infrared); see Table_band_data in the main "Mapping nectarrich floral resources for pollinators" folder for per-band data.

- Coordinate reference system:
  - OSGB 1936 / British National Grid (EPSG: 27700).

- Data provenance and structure:
  - Files are TIFF format; high-resolution (3 cm) and lower-resolution (7 cm) datasets with both multi-band originals and clipped 4-band classification-ready versions.
  - Band data and detailed band-by-band information are maintained separately in a referenced table within a companion folder.

- Relevance for monitoring frameworks:
  - Provides multi-scale, spectrally rich imagery essential for monitoring floral resources.
  - Clear naming conventions and documented band mappings aid reproducibility and data governance.
  - Metadata indicates the need to maintain provenance, file-level metadata, and access to the accompanying band data table to ensure data usability and quality for monitoring decisions.