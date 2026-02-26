# Landscape area data 1990 [Countryside Survey], Great Britain

## Overview
- Data from the Countryside Survey (GB, 1990) documenting landscape areas and attributes across 506 1km squares.
- Two CSV files detailing habitat areas and additional attributes within each 1km square.
- Data products support analysis and mapping of Broad and Priority Habitats, land classification, and related landscape attributes.
- Acknowledgement and copyright requirements apply to all copies, publications, and presentations.

## Files included
- LANDSCAPE_AREA_FEATURE_HAB_1990.csv
  - Contains areas of Broad and Priority Habitats within each 1km square.
  - Key fields: SQUARE, YEAR, ID, BROAD_HABITAT, BROAD_HABITAT_NAME, AREA (m²), LC07, LC07_NUM, COUNTRY, COUNTY, EZ_DESC_07.
- LANDSCAPE_AREA_FEATURE_ATT_1990.csv
  - Contains additional attributes for areas within the 1km squares.
  - Key groupings: YEAR, SQUARE, ID, THEME, THEME_NAME, PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME, SPECIES, SPECIES_NAME, SPECIES_COVER, SPECIES_COVER_NAME, PRIMARY_QUALIFIER, PRIMARY_QUALIFIER_NAME, STRUCTURE_USE, STRUCTURE_USE_NAME, PHYSIOGRAPHY_COVER, PHYSIOGRAPHY_COVER_NAME, ROAD_VERGE_A, ROAD_VERGE_A_NAME, ROAD_VERGE_B, ROAD_VERGE_B_NAME, MODAL_DBH, MODAL_DBH_NAME, LC07, LC07_NUM, COUNTRY, COUNTY, EZ_DESC_07.

## Key fields and what they represent
- HAB file
  - SQUARE: 1km sampling site code.
  - YEAR: Survey year (1990).
  - ID: Landscape area polygon identifier (unique within a year).
  - BROAD_HABITAT / BROAD_HABITAT_NAME: Broad habitat code and description.
  - AREA: Habitat area within the 1km square (in square metres).
  - LC07 / LC07_NUM: ITE Land Classification 2007 codes.
  - COUNTRY / COUNTY: Location identifiers (England, Scotland, Wales; county or council).
  - EZ_DESC_07: Environmental Zone description.
- ATT file
  - A rich set of attributes linked to landscape areas, including THEME / THEME_NAME, PRIMARY_ATTRIBUTE / PRIMARY_ATTRIBUTE_NAME, SPECIES / SPECIES_NAME / SPECIES_COVER / SPECIES_COVER_NAME, QUALIFIERS, STRUCTURE_USE / STRUCTURE_USE_NAME, PHYSIOGRAPHY_COVER / PHYSIOGRAPHY_COVER_NAME, ROAD_VERGE_A/B, MODAL_DBH / MODAL_DBH_NAME, LC07 / LC07_NUM, LOCATION fields (COUNTRY, COUNTY), and EZ_DESC_07.

## Usage guidance
- Data represent 506 1km squares from the 1990 Countryside Survey, enabling spatial analysis of habitat extent and associated attributes.
- Useful for combining habitat areas with attribute-level data (species, land use, physiography, road verge context) and linking to ITE Land Classification (LC07) and environmental zone descriptions.
- Applicability includes landscape-level habitat mapping, trend analyses (in conjunction with other years), and informing policy or planning at regional scales.

## Acknowledgement and licensing
- All use of Countryside Survey data must include the following acknowledgement on copies, publications, presentations, etc.:
  - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."

## References and references to related materials
- Countryside Survey Website (general overview and methodology): http://www.countrysidesurvey.org.uk/
- Key publications and classifications related to the data:
  - ITE Merlewood Land Classification of Great Britain (1996)
  - Land Classes in Great Britain: Preliminary Descriptions (1981)
  - Jackson, D.L. (2000) Guidance on Biodiversity Broad Habitat Classification (JNCC Report 307)
  - ITE Land Classification of Great Britain 2007 (Bunce et al.)
- Data licensing and DOI/links are provided in the references for each corresponding dataset and methodology document.