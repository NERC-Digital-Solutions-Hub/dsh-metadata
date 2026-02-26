# Landscape area data 2007 [Countryside Survey], Great Britain

## Overview
- Dataset describing areas of Broad and Priority Habitats across 591 1km squares in Great Britain, sampled in 2007; areas with refused access are excluded.

## Data files and structure
- LANDSCAPE_AREA_FEATURE_HAB_2007.csv
  - Contains habitat-area data per 1km square for the 2007 survey.
  - Key columns include: SQUARE, YEAR, ID (unique within a year), BROAD_HABITAT, BROAD_HABITAT_NAME, AREA (square metres), LC07, LC07_NUM, COUNTRY, COUNTY, EZ_DESC_07, plus auxiliary identifiers.
- LANDSCAPE_AREA_FEATURE_ATT_2007.csv
  - Contains additional attributes for the 591 1km squares.
  - Key columns include: YEAR, SQUARE, ID, THEME, THEME_NAME, PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME, SPECIES, SPECIES_NAME, SPECIES_COVER, SPECIES_COVER_NAME, PRIMARY_QUALIFIER, PRIMARY_QUALIFIER_NAME, STRUCTURE_USE, STRUCTURE_USE_NAME, PHYSIOGRAPHY_COVER, PHYSIOGRAPHY_COVER_NAME, ROAD_VERGE_A, ROAD_VERGE_A_NAME, ROAD_VERGE_B, ROAD_VERGE_B_NAME, MODAL_DBH, MODAL_DBH_NAME, MOSAIC_PRECENT_AREA, LC07, LC07_NUM, COUNTRY, COUNTY, EZ_DESC_07.
- All use of Countryside Survey data must be acknowledged (see below).

## Data content and classifications
- HAB file: provides habitat codes and names (Broad Habitat and related identifiers) and the area of each habitat within each 1km square.
- ATT file: provides detailed thematic attributes (land use themes, primary attributes, species, cover values, qualifiers, structure use, physiography, road verge details, modal forestry DBH, mosaic habitat proportions) and again location and classification codes.
- Classifications referenced include ITE Land Classification of Great Britain 2007 (LC07) and related habitat nomenclature (Broad Habitat, Ecology zones).

## Governance, quality and metadata considerations
- Data origin and stewardship: Countryside Survey data owned by NERC – Centre for Ecology & Hydrology.
- Documentation and citations: Links to Countryside Survey website and key references for classifications (ITE Land Classification, Broad Habitat guidance, etc.).
- Data integrity: Refused access areas excluded; standard field definitions provided to support interoperability and reuse.
- Metadata expectations for stewardship: clear mapping of codes to names (LC07, BROAD_HABITAT, THEME, etc.), year of survey, geographic scope, and environmental zone descriptions (EZ_DESC_07).

## Access, usage rights and acknowledgements
- Acknowledgement is required for all uses: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and “Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.”
- Appropriate citation of the Countryside Survey sources and related references is expected in publications and presentations.

## Relevance to data stewardship practice
- Demonstrates the need for comprehensive metadata, standard classifications, and clear data provenance to ensure discoverability and reuse across organizations with large datasets.
- Highlights common stewardship tasks: ensuring data standards (habitat codes, land-use attributes), maintaining update pathways, and communicating usage rights and citations to data users.
- Exemplifies handling of multi-file datasets with related keys (SQUARE, ID, YEAR) to enable linking habitat areas with detailed attributes.

## Practical notes for data users
- Data are provided in two linked CSV files (habitat areas and their attributes) for 2007 across Great Britain; refer to the 2007 Countryside Survey methodology for context.
- Ensure proper acknowledgement in any derived products and publications using the specified wording.
- Consult the referenced publications and Countryside Survey website for methodological background and classification definitions.

## References and provenance
- Countryside Survey Website and project overview.
- ITE Merlewood Land Classification of Great Britain (1996).
- Guidance on Biodiversity Broad Habitat Classification (Jackson, 2000).
- ITE Land Classification of Great Britain 2007 (Bunce et al., 2007).
- DOI/links provided in the dataset documentation for detailed methodology and data centre records.