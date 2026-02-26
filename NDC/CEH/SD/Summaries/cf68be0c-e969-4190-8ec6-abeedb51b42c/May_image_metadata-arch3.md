# May Image Metadata

## Overview
- Imagery collected for mapping nectar-rich floral resources for pollinators on a farm in Northamptonshire, UK.
- Data collected in mid-May 2019 at two spatial resolutions (3 cm and 7 cm) and across multiple spectral bands.

## Data capture details
- Location: farm in Northamptonshire, UK.
- Dates: 14th/15th May 2019.
- Platform and sensor: Hasselblad A6D-100c (50 mm) cameras on a Sky Arrow 650 manned aircraft.
- Spatial resolutions: 3 cm and 7 cm.
- Coordinate reference system: OSGB 1936 / British National Grid (EPSG: 27700).
- Data format: imagery stored as 16-bit orthomosaics.

## Data content and bands
- May_3cm: clipped 4-band 3 cm resolution image for classifications (bands blue, green, red, infrared; B0, B1, B2, B3).
- 14_05_2019_6_Band_3: 7-band data at 3 cm for May (6-band data details referenced in Table_band_data).
- May_7cm: original 7 cm data for May (6-band image; 4-band clipped version used for classifications: blue, green, red, infrared).
- 14_05_2019_6_Band_7_BIL: clipped 4-band 7 cm resolution image used for classifications.
- Original 7 cm 6-band image for May; per-band data available in Table_band_data in the main folder.
- Data organization: Table_band_data located in the main "Mapping nectar-rich floral resources for pollinators" folder.

## Data organization and references
- Main folder: "Mapping nectar-rich floral resources for pollinators."
- Table_band_data provides individual band data details for the multispectral datasets.

## Relevance to monitoring frameworks
- Provides high-resolution, multi-band imagery suitable for identifying and mapping nectar-rich floral resources, supporting environmental health indicators and policy evaluations related to pollinator habitats.
- The presence of both 3 cm and 7 cm datasets allows cross-resolution analysis and validation of classifications.
- Metadata and file naming conventions (e.g., May_3cm, May_7cm, 14_05_2019_6_Band_3) support reproducibility and traceability in monitoring workflows.

## Data quality, governance and barriers
- Metadata availability is explicit, with references to Table_band_data for band-specific details.
- Potential barriers inferred from the broader archetype context (noted in general challenges) include: the need for robust metadata, data sharing requirements, and data governance to ensure datasets meet standards and remain up to date.
- Data transformation may be required when using 6-band versus 4-band representations, and ensuring consistent CRS and 16-bit depth is important for analysis reproducibility.