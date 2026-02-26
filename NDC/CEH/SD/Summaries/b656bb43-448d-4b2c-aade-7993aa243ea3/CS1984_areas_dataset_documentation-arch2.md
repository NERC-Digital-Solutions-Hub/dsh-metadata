# Landscape area data 1984 [Countryside Survey], Great Britain

- The Countryside Survey dataset provides 1984 measurements of landscape areas across Great Britain, focusing on Broad and Priority Habitats sampled in 379 1km squares.
- Acknowledgement and rights: Data are owned by NERC - Centre for Ecology & Hydrology; all use must acknowledge Countryside Survey data © CEH/NERC; all rights reserved.

## Overview and purpose for analysts

- Used to monitor environmental health by documenting habitat area and related landscape attributes in a consistent, time-stamped format.
- Supports categorising environmental health against standards and tracking policy performance over time.
- Data can be integrated with other datasets to enhance value and enable broader analyses.

## Datasets and structure

- LANDSCAPE_AREA_FEATURE_HAB_1984.csv
  - Content: Areas of Broad and Priority Habitats within 379 1km squares across Great Britain (1984).
  - Key columns:
    - SQUARE: 1km square sampling site code
    - YEAR: Year of survey
    - ID: Landscape area polygon identifier (unique within a year)
    - BROAD_HABITAT / BROAD_HABITAT_NAME: Broad habitat code and name (Jackson, 2000)
    - AREA: Area of habitat within the 1km polygon (square metres)
    - LC07 / LC07_NUM: ITE Land Class 2007 code and number
    - COUNTRY / COUNTY: Geographic location
    - EZ_DESC_07: Countryside Survey Environmental Zone description
- LANDSCAPE_AREA_FEATURE_ATT_1984.csv
  - Content: Additional attributes for areas within the same 379 squares (1984).
  - Key columns (representative subset):
    - YEAR, SQUARE, ID
    - THEME / THEME_NAME: Theme code and description (land use)
    - PRIMARY_ATTRIBUTE / PRIMARY_ATTRIBUTE_NAME
    - SPECIES / SPECIES_NAME
    - SPECIES_COVER / SPECIES_COVER_NAME
    - PRIMARY_QUALIFIER / PRIMARY_QUALIFIER_NAME
    - STRUCTURE_USE / STRUCTURE_USE_NAME
    - PHYSIOGRAPHY_COVER / PHYSIOGRAPHY_COVER_NAME
    - ROAD_VERGE_A / ROAD_VERGE_A_NAME
    - ROAD_VERGE_B / ROAD_VERGE_B_NAME
    - MODAL_DBH / MODAL_DBH_NAME
    - LC07 / LC07_NUM, COUNTRY, COUNTY, EZ_DESC_07
- The two files together provide habitat area and a broad suite of attributes (land use, species, structure, physiography, road verge, diameter at breast height, etc.) for each 1km square in 1984.

## Geographic, temporal and classification context

- Geography: Great Britain (England, Scotland, Wales) across 379 1km sampling squares.
- Timeframe: Survey year is 1984.
- Classifications referenced:
  - Broad Habitat codes and names (Jackson, 2000)
  - ITE Land Classification 2007 (LC07) for cross-walked land-use classification
  - Environmental Zone description (EZ_DESC_07)

## Data usage and outputs

- Outputs can include maps, charts, and tabular reports showing habitat areas and related attributes by square or region.
- Data are suitable for standardised monitoring outputs and for integration into broader environmental health assessments.

## Data rights, acknowledgements, and references

- Acknowledgement requirement: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and copyright notice apply to all copies, publications, and presentations.
- References and resources:
  - Countryside Survey website (general overview and methodologies)
  - ITE Merlewood Land Classification and ITE Land Classification of Great Britain 2007 documents
  - Jackson (2000) Guidance on Biodiversity Broad Habitat Classification
  - NERC Environmental Information Data Centre entries (for LC07 and related datasets)

## Analyst considerations and challenges

- Value enhancement: Combine CS 1984 habitat data with other datasets to enrich analyses and avoid single-use datasets.
- Data access and reuse: Ensure proper data acknowledgement; data should be stored and accessible via appropriate portals.
- Interpretation: Be mindful of crosswalks between 1984 data and 2007 LC07 classifications; environmental zone descriptions may require additional referencing for full context.

## Practical takeaways for monitoring work

- Use the HAB_1984 file to quantify habitat area by square, country, and habitat type; complement with EZ_DESC_07 for zone context.
- Use the ATT_1984 file to explore associations with land use themes, species presence/cover, structure, physiography, road verge characteristics, and DBH-related attributes.
- Leverage standardised codes (LC07, THEME, SPECIES, etc.) to enable comparisons over time and with other datasets.
- Always include the required Countryside Survey acknowledgement in outputs.