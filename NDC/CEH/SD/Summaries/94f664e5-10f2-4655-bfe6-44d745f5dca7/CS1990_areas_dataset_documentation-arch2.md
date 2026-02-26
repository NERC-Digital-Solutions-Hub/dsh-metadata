# Landscape area data 1990 [Countryside Survey], Great Britain

## Overview
- Provides landscape-level habitat data from 506 1km squares across Great Britain, sampled in 1990.
- Part of the Countryside Survey dataset managed by NERC - Centre for Ecology & Hydrology.
- Aimed at monitoring environmental condition and enabling standardised outputs (e.g., habitat areas, classifications) for trend analysis and policy assessment.

## Data Files and Key Fields

### LANDSCAPE_AREA_FEATURE_HAB_1990.csv
- SQUARE: 1km square sampling site code
- YEAR: Survey year
- ID: Landscape area polygon identifier (unique within a year)
- BROAD_HABITAT: Broad Habitat code
- BROAD_HABITAT_NAME: Broad and Priority Habitat name (Jackson, 2000)
- AREA: Area of habitat within the 1km square (square metres)
- LC07: ITE Land Class 2007 code
- LC07_NUM: ITE Land Class 2007 numeric code
- COUNTRY: England (ENG), Scotland (SCO), Wales (WAL)
- COUNTY: County (Eng & Wal) or Council (Sco)
- EZ_DESC_07: Countryside Survey Environmental Zone description

### LANDSCAPE_AREA_FEATURE_ATT_1990.csv
- YEAR: Survey year
- SQUARE: 1km square sampling site code
- ID: Landscape area polygon identifier (unique within a year)
- THEME: Theme code
- THEME_NAME: Theme (land use)
- PRIMARY_ATTRIBUTE: Primary Attribute code
- PRIMARY_ATTRIBUTE_NAME: Primary Attribute description
- SPECIES: Species code
- SPECIES_NAME: Species name
- SPECIES_COVER: Species cover code
- SPECIES_COVER_NAME: Species cover description
- PRIMARY_QUALIFIER: Primary qualifier code
- PRIMARY_QUALIFIER_NAME: Primary qualifier description
- STRUCTURE_USE: Structure use code
- STRUCTURE_USE_NAME: Structure use description
- PHYSIOGRAPHY_COVER: Physiography cover code
- PHYSIOGRAPHY_COVER_NAME: Physiography cover description
- ROAD_VERGE_A: Road Verge A code
- ROAD_VERGE_A_NAME: Road verge A description
- ROAD_VERGE_B: Road verge B code
- ROAD_VERGE_B_NAME: Road verge B description
- MODAL_DBH: Modal DBH code
- MODAL_DBH_NAME: Modal DBH description
- LC07: ITE Land Class 2007 code
- LC07_NUM: ITE Land Class 2007 numeric code
- COUNTRY: England (ENG), Scotland (SCO), Wales (WAL)
- COUNTY: County (Eng & Wal) or Council (Sco)
- EZ_DESC_07: Countryside Survey Environmental Zone description

## Temporal and Geographic Scope
- Year of survey: 1990
- Coverage: 506 1km squares across Great Britain
- Geography coding: SQUARE, COUNTRY, COUNTY; LC07 and environmental zone descriptors provide standardized geographic-context information

## Data Standards and Classifications
- Broad Habitat classification: Broad Habitat codes with names (BAP-related context) per Jackson (2000)
- ITE Land Classification: LC07 and LC07_NUM referencing the 2007 ITE classification
- Environmental Zones: EZ_DESC_07 providing Countryside Survey environmental zone descriptions
- Data formats and fields are designed for cross-survey comparability and integration with related Countryside Survey outputs

## Usage Notes and Requirements
- All Countryside Survey data must be acknowledged in outputs
- Acknowledgement text (to be used on copies, publications, and presentations):
  - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
- Data sources and methodologies are linked to public references and the Countryside Survey website for context and methodological details

## Related Publications and References
- Countryside Survey website (general overview and methodologies): http://www.countrysidesurvey.org.uk/
- ITE Merlewood Land Classification of Great Britain (Bunce et al., 1996)
- ITE Land Classification of Great Britain 2007 (Bunce et al., 2007)
- Guidance on Biodiversity Broad Habitat Classification (Jackson, 2000)
- Additional supporting documents and DOIs linked via the CEH/NERC data records

## Practical Applications for Analysts Monitoring the Environment
- Track and compare habitat area distributions across 1990 GB landscapes
- Link habitat area data with land-use themes and species/cover attributes for integrated environmental health assessments
- Use standard classifications (LC07, Broad Habitat, EZ_07) to benchmark against other years or datasets
- Support data portal uploads and reproducible reporting with explicit acknowledgement of data origin
- Enable cross-dataset analyses by leveraging consistent geographic identifiers (SQUARE, COUNTRY, COUNTY) and standardized attribute codes