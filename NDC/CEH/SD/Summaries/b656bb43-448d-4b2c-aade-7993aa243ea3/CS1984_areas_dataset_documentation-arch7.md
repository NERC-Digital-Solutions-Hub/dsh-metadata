# Landscape area data 1984 [Countryside Survey], Great Britain

- Overview
  - Two CSV datasets from the Countryside Survey 1984 covering landscape areas within 379 1km squares across Great Britain.
  - Data owned by NERC - Centre for Ecology & Hydrology; all use must be acknowledged with the provided acknowledgement text.
  - Designed for GIS use to map and analyse habitat areas, land classifications, and related attributes at the 1km-square scale.

- Datasets and key fields
  - LANDSCAPE_AREA_FEATURE_HAB_1984.csv
    - SQUARE: 1km square sampling site code
    - YEAR: survey year (1984)
    - ID: landscape area polygon identifier (unique within a year)
    - BROAD_HABITAT: broad habitat code
    - BROAD_HABITAT_NAME: broad and priority habitat description
    - AREA: habitat area within the 1km polygon (square metres)
    - LC07, LC07_NUM: ITE Land Class 2007 codes
    - COUNTRY: country (England ENG, Scotland SCO, Wales WAL)
    - COUNTY: county or council area
    - EZ_DESC_07: Countryside Survey Environmental Zone description
  - LANDSCAPE_AREA_FEATURE_ATT_1984.csv
    - YEAR, SQUARE, ID: keys
    - THEME, THEME_NAME: theme (land use) codes and names
    - PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME
    - SPECIES, SPECIES_NAME
    - SPECIES_COVER, SPECIES_COVER_NAME
    - PRIMARY_QUALIFIER, PRIMARY_QUALIFIER_NAME
    - STRUCTURE_USE, STRUCTURE_USE_NAME
    - PHYSIOGRAPHY_COVER, PHYSIOGRAPHY_COVER_NAME
    - ROAD_VERGE_A, ROAD_VERGE_A_NAME
    - ROAD_VERGE_B, ROAD_VERGE_B_NAME
    - MODAL_DBH, MODAL_DBH_NAME
    - LC07, LC07_NUM
    - COUNTRY, COUNTY
    - EZ_DESC_07
  - Notes
    - The second file provides additional attribute data for areas within the 1km squares, including habitat-related attributes, species information, and other environmental and structural descriptors.
    - All fields reflect data collected in 1984 as part of the Countryside Survey and linked to the 1km square framework.

- How to use in GIS
  - Join HAB_1984 and ATT_1984 on YEAR, SQUARE, and ID to create per-square habitat polygons with rich attribute detail.
  - Use AREA to quantify habitat extents within each 1km square; aggregate to larger extents if needed.
  - Visualise spatial patterns of LC07 land classifications, environmental zones (EZ_DESC_07), and broad habitats across Great Britain.
  - Employ ATTR fields (species, cover, DBH, road verge, physiography, etc.) for advanced analyses or themed layers (e.g., biodiversity indicators, habitat condition).
  - Leverage COUNTRY and COUNTY for regional analyses and mapping.

- Data quality, provenance and rights
  - Data originate from the 1984 Countryside Survey; linked to ITE Land Classification and biodiversity classifications.
  - Acknowledgement required in all copies, publications, reports, and presentations:
    - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
    - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
  - References and methodology are provided to support interpretation and integration with related datasets.

- References and publications
  - Countryside Survey website and methodological documents
  - ITE Merlewood Land Classification of Great Britain (Bunce et al., 1996)
  - ITE Land Classification of Great Britain 2007 (Bunce et al., 2007)
  - Jackson D.L. Guidance on Biodiversity Broad Habitat Classification (2000)