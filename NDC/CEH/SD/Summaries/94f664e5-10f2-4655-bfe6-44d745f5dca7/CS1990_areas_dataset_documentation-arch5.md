# Landscape area data 1990 [Countryside Survey], Great Britain

- Landscape area data from the Countryside Survey, Great Britain (1990 sampling), with a published version dated 15-1-2016; data owned by NERC - Centre for Ecology & Hydrology (CEH).

## Purpose and scope

- Documents 1990 Areas of Broad and Priority Habitats across 506 1km squares in Great Britain.
- Two related CSV files provide habitat areas and associated attributes for each 1km square.
- Data are prepared to support governance, discovery, and reuse of landscape habitat information.

## Data structure and content

- LANDSCAPE_AREA_FEATURE_HAB_1990.csv
  - Captures habitat areas within 1km square polygons.
  - Key fields: SQUARE, YEAR, ID, BROAD_HABITAT, BROAD_HABITAT_NAME, AREA (square metres), LC07 (ITE Land Class 2007) and LC07_NUM, COUNTRY, COUNTY, EZ_DESC_07.
  - ID is unique within a year; SQUARE codes identify sampling sites; YEAR denotes survey year.
  - Includes environmental zone description reference (EZ_DESC_07) with documentation link.

- LANDSCAPE_AREA_FEATURE_ATT_1990.csv
  - Provides additional attributes for the same 1km square areas.
  - Key fields: YEAR, SQUARE, ID, THEME, THEME_NAME, PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME, SPECIES, SPECIES_NAME, SPECIES_COVER, SPECIES_COVER_NAME, PRIMARY_QUALIFIER, PRIMARY_QUALIFIER_NAME, STRUCTURE_USE, STRUCTURE_USE_NAME, PHYSIOGRAPHY_COVER, PHYSIOGRAPHY_COVER_NAME, ROAD_VERGE_A, ROAD_VERGE_A_NAME, ROAD_VERGE_B, ROAD_VERGE_B_NAME, MODAL_DBH, MODAL_DBH_NAME, LC07, LC07_NUM, COUNTRY, COUNTY, EZ_DESC_07.
  - Includes biological and physical attributes (e.g., species presence and cover, structure use, physiography, road verge attributes, modal DBH).

## Rights, attribution, and provenance

- All use of Countryside Survey data must be acknowledged.
- Acknowledgement statement: “Countryside Survey data owned by NERC - Centre for Ecology and Hydrology.”
- Copyright: Countryside Survey © NERC-CEH. All rights reserved.
- Acknowledgement and copyright must appear on all copies, publications, reports, and presentations.

## Metadata, documentation, and references

- EZ_DESC_07 provides environmental zone descriptions; see linked documentation.
- Data rely on established classifications:
  - ITE Land Classification 2007 (LC07, LC07_NUM)
  - Biodiversity Broad Habitat classifications (as per Jackson 2000)
- References and documentation available via:
  - Countryside Survey Website (general overview and methodologies)
  - Publications by Bunce et al. (ITE Land Classification) and Jackson (habitat guidance)

## Access, governance, and maintenance considerations

- The data provide a historical snapshot (1990) with a documented version in 2016.
- Data stewardship considerations:
  - Maintain clear metadata for all classification schemes and field definitions.
  - Ensure consistent use of codes (LC07, THEME, SPECIES, etc.) and link to documentation.
  - Preserve the required acknowledgement in all downstream use.
  - Handle any environmental zone descriptions and their associated documentation consistently.
  - Provide guidance for reuse, including potential limitations around non-interoperability of some legacy classifications.

## Applications and implications for users

- Facilitates analysis of habitat extent and associated attributes across Great Britain for 1990.
- Enables cross-referencing with land classification and habitat guidance documentation.
- Supports historical baselining for landscape and habitat change studies, governance, and biodiversity assessments.

## References and sources

- Countryside Survey Website: general project overview and methodologies.
- Bunce, R.G.H., Barr, C.J., Clarke, R.T., Howard, D.C., Lane, A.M.J. (1996) ITE Merlewood Land Classification of Great Britain.
- Bunce, R.G.H., Barr, C.J., Whittaker, H.A. (1981) Land Classes in Great Britain: Preliminary Descriptions for Users of the Merlewood Method of Land Classification.
- Jackson D.L. (2000) Guidance on the interpretation of the Biodiversity Broad Habitat Classification; JNCC Report 307.
- Bunce, R.G.H., Barr, C.J., Clarke, R.T., Howard, D.C., Scott, W.A. (2007) ITE Land Classification of Great Britain 2007. NERC Environmental Information Data Centre.