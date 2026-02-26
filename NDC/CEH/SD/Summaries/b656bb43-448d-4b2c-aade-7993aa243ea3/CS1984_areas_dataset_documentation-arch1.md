# Landscape area data 1984 [Countryside Survey], Great Britain Version: 1: 15-1-2016 Countryside Survey data © NERC - Centre for Ecology & Hydrology

## Overview
- Data from the Countryside Survey (1984) covering 379 1km squares across Great Britain.
- Captures areas of Broad and Priority Habitats within 1km sampling squares.
- Provides both habitat area measurements and a broad set of associated attributes and classifications (e.g., land use, environmental zones, biodiversity-related codes).
- Designed to support landscape-scale ecological analysis and compatibility with later classifications (e.g., ITE Land Classification 2007).

## Data files and key variables

### LANDSCAPE_AREA_FEATURE_HAB_1984.csv
- Purpose: Habitat area within each 1km square polygon.
- Key columns:
  - SQUARE: 1km square sampling site code
  - YEAR: Survey year (1984)
  - ID: Landscape area polygon identifier (unique within a year)
  - BROAD_HABITAT: Broad Habitat code
  - BROAD_HABITAT_NAME: Broad/priority habitat name (Jackson, 2000)
  - AREA: Habitat area within the 1km polygon (square metres)
  - LC07, LC07_NUM: ITE Land Classification 2007 codes/numbers
  - COUNTRY, COUNTY: Geographic location (England, Scotland, Wales)
  - EZ_DESC_07: Environmental Zone description (see referenced documentation)

### LANDSCAPE_AREA_FEATURE_ATT_1984.csv
- Purpose: Additional attributes for areas within the 1km squares.
- Key columns include:
  - YEAR, SQUARE, ID: Identifiers linking to HAB file
  - THEME, THEME_NAME: Theme code and description (land use)
  - PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME: Primary attribute description
  - SPECIES, SPECIES_NAME, SPECIES_COVER, SPECIES_COVER_NAME: Species and cover details
  - PRIMARY_QUALIFIER, PRIMARY_QUALIFIER_NAME: Qualifier details
  - STRUCTURE_USE, STRUCTURE_USE_NAME: Structure use codes and descriptions
  - PHYSIOGRAPHY_COVER, PHYSIOGRAPHY_COVER_NAME: Inland physiography cover descriptions
  - ROAD_VERGE_A, ROAD_VERGE_A_NAME; ROAD_VERGE_B, ROAD_VERGE_B_NAME: Road verge attributes (A and B)
  - MODAL_DBH, MODAL_DBH_NAME: Modal DBH (Diameter at Breast Height) values and descriptions
  - LC07, LC07_NUM, COUNTRY, COUNTY, EZ_DESC_07: Cross-reference to habitat classification, location, and environment zone

## Use considerations

- Data are linked by SQUARE and ID to assemble habitat areas and their attributes for each 1km square.
- Classifications referenced include Broad Habitats and ITE Land Classification 2007; compatibility with other ecological classifications (e.g., biodiversity, land use) is possible through the attached codes and names.
- The dataset reflects 1984 survey context; cross-walking to newer classifications may be required for longitudinal analyses.
- Suitable for analyses at a 1km scale across Great Britain, with country and county-level geographic detail.
- Documentation notes emphasize the need for proper acknowledgement when using CS data.

## Access, acknowledgement and licensing

- All Countryside Survey data must be acknowledged.
- Required attribution:
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © NERC - Centre for Ecology & Hydrology. All rights reserved."
- Data are accompanied by publications and references that provide methodology and classifications.

## References and provenance

- Countryside Survey website and methodology documents.
- Key publications and classifications:
  - Bunce et al. (1996, 2007): ITE Land Classification of Great Britain
  - Jackson (2000): Guidance on Biodiversity Broad Habitat Classification
  - Additional links and DOIs provided for ITE Land Classification 2007 and related datasets
- Data usage notes and links to the Countryside Survey project and related datasets.