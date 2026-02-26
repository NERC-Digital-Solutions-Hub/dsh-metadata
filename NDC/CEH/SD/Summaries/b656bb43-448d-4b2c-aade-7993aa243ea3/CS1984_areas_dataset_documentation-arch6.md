# Landscape area data 1984 [Countryside Survey], Great Britain

## Overview
- Historical landscape data from the Countryside Survey (1984) covering Great Britain.
- Focuses on areas of Broad and Priority Habitats within 1 km square sampling units (379 squares).
- Two CSV files accompany the dataset, detailing habitat areas and associated attributes, with maps to the ITE Land Classification (2007) and other thematic codes.
- Data is owned by NERC - Centre for Ecology & Hydrology; usage requires formal acknowledgement.

## Datasets

- LANDSCAPE_AREA_FEATURE_HAB_1984.csv
  - Purpose: Areas of Broad and Priority Habitats within each 1 km square.
  - Key columns:
    - SQUARE: 1 km square sampling site code
    - YEAR: Survey year
    - ID: Landscape area polygon identifier (unique within a year)
    - BROAD_HABITAT / BROAD_HABITAT_NAME: Habitat code and name
    - AREA: Area of habitat within the square (square metres)
    - LC07 / LC07_NUM: ITE Land Class 2007 code and number
    - COUNTRY / COUNTY: Location identifiers
    - EZ_DESC_07: Environmental Zone description
    - Additional descriptive fields (BROAD_HABITAT_NAME, etc.)

- LANDSCAPE_AREA_FEATURE_ATT_1984.csv
  - Purpose: Additional attributes for the landscape areas within each 1 km square.
  - Key columns (selected): 
    - YEAR / SQUARE / ID: Keys identifying the area
    - THEME / THEME_NAME: Thematic grouping (land use)
    - PRIMARY_ATTRIBUTE / PRIMARY_ATTRIBUTE_NAME
    - SPECIES / SPECIES_NAME / SPECIES_COVER / SPECIES_COVER_NAME
    - PRIMARY_QUALIFIER / PRIMARY_QUALIFIER_NAME
    - STRUCTURE_USE / STRUCTURE_USE_NAME
    - PHYSIOGRAPHY_COVER / PHYSIOGRAPHY_COVER_NAME
    - ROAD_VERGE_A / ROAD_VERGE_A_NAME
    - ROAD_VERGE_B / ROAD_VERGE_B_NAME
    - MODAL_DBH / MODAL_DBH_NAME
    - LC07 / LC07_NUM
    - COUNTRY / COUNTY
    - EZ_DESC_07
  - Note: Contains rich attribute data linked to each habitat area, enabling multi-faceted analysis (e.g., habitat type, land use, species presence, structure and physiography, road verge context).

## Usage & Outputs

- Practical uses for data support purposes:
  - Combine HAB and ATT files to create integrated habitat profiles for each 1 km square (spatial granularity suitable for regional analyses).
  - Transform and curate data into end-user friendly formats (dashboards, pivot tables, charts) to enable self-serve exploration of habitat extent, land-use themes, and associated attributes.
  - Develop early prototypes of data products and gather feedback to refine outputs.
  - Promote outputs and advocate for better data creation and consistency across datasets.

## Data quality considerations

- Temporal scope: Snapshot for the year 1984; not a time-series dataset by itself.
- Spatial scope: Derived from 379 1 km squares across Great Britain; users should consider spatial representativeness and potential gaps when extrapolating beyond sampled units.
- Variable richness: Rich attribute fields in ATT_1984 enable detailed analyses but require careful handling of coding schemes (e.g., LC07 classifications, habitat codes, and environmental zone descriptors).

## Acknowledgement & rights

- All use of Countryside Survey data must be acknowledged.
- Required acknowledgment text:
  - Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Include acknowledgement on copies, publications, reports, and presentations.

## References & publications

- Countryside Survey website: general overview and methodologies
- ITE Merlewood Land Classification of Great Britain (Bunce et al., 1996)
- ITE Land Classification of Great Britain 2007 (Bunce et al., 2007)
- Guidance on biodiversity broad habitat classification (Jackson, 2000)
- NERC Environmental Information Data Centre references for the 2007 classification
- Direct doi/links and citations provided in the dataset documentation for reproducibility and context