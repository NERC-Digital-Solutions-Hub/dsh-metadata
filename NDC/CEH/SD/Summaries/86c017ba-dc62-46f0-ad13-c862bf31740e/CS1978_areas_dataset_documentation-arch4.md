# Landscape area data 1978 [Countryside Survey], Great Britain

## Overview
- 1978 dataset of areas of Broad and Priority Habitats derived from 256 1km squares across Great Britain, as surveyed in 1978.
- Part of the Countryside Survey, data owned by NERC - Centre for Ecology & Hydrology; © Countryside Survey.
- Supports measurement of habitat change over time.

## Data structure and key fields
- File: LANDSCAPE_AREA_FEATURE_HAB_1978.csv
- Columns and meanings:
  - SQUARE: 1km square sampling site code (text)
  - YEAR: Year of survey (number)
  - ID: Landscape area polygon identifier (unique within a year)
  - BROAD_HABITAT: Broad habitat code (number)
  - BROAD_HABITAT_NAME: Broad/Priority habitat name (text)
  - AREA: Area of habitat within the 1km polygon (square metres)
  - LAND_CLASS90: ITE Land Class 1990 (number)
  - COUNTRY: Country (ENG, SCO, WAL)
  - COUNTY: County or Council (text)
  - EZ_DESC_07: Countryside Survey Environmental Zone description (text)
- Taxonomies referenced: Jackson 2000 (habitat names), ITE Land Classification (1990).

## Spatial/Temporal coverage
- Geography: Great Britain (England, Scotland, Wales)
- Time: Snapshot for the year 1978

## Usage rights and attribution
- All use of Countryside Survey data must be acknowledged.
- Required acknowledgement and copyright statement on all copies, publications, reports, and presentations.

## Data quality, standards and metadata considerations
- Uses established classifications (BROAD_HABITAT, LAND_CLASS90) and cross-references to external schemes (ITE Land Classification, JNCC Biodiversity Broad Habitat guidance).
- Metadata supports discoverability; users should verify content/format alignment when integrating with other datasets.

## Related references and access points
- Countryside Survey website and Final Reports (e.g., 30-year habitat change studies)
- Key publications and documents:
  - CS1978_final_report_PDF.pdf
  - CS_UK_2007_TR4.pdf
  - ITE Land Classification papers (1990, 1996)
  - Jackson D.L. (2000) Biodiversity Broad Habitat Guidance
- Links and DOIs available via Countryside Survey resources and CEH/NERC data centres.

## Practical considerations for data products
- Useful for cross-year habitat change analyses when paired with other Countryside Survey years; ensure consistency in habitat classifications (BROAD_HABITAT and LAND_CLASS90) and COUNTRY coding.
- Environmental Zone descriptions (EZ_DESC_07) support regional analyses and governance planning.
- Data products should preserve attribution and metadata to maintain provenance and allow interoperability with related habitat classification schemes.

## Acknowledgements and policy
- Include the specified acknowledgement text:
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology" 
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."