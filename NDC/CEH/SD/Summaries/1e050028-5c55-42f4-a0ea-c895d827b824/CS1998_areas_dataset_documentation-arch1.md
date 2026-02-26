# Landscape area data 1998 [Countryside Survey], Great Britain

## Overview
- Dataset from the Countryside Survey (1998) covering Great Britain, sampled in 1 km squares.
- Focuses on areas of Broad and Priority Habitats within each 1 km square (569 squares in total).
- Two CSV files provided: one for habitat areas and one for additional attributes.
- Data quality and usability supported by standard classifications (ITE Land Classification 2007) and related habitat codes.
- Acknowledgement and copyright requirements apply to all uses.

## Data Files
- LANDSCAPE_AREA_FEATURE_HAB_1998.csv
  - Contains habitat-area measures within each 1 km square.
- LANDSCAPE_AREA_FEATURE_ATT_1998.csv
  - Contains additional attributes for each habitat polygon, including thematic codes, species data, structure/use attributes, physiography, road verge information, and mosaic area.

## Key Fields (highlights)
- Common keys across files: SQUARE (1 km square code), YEAR (survey year, 1998), ID (polygon identifier within a year).
- Habitat file: BROAD_HABITAT, BROAD_HABITAT_NAME, AREA (square metres), LC07, LC07_NUM, COUNTRY, COUNTY, EZ_DESC_07.
- Attributes file: THEME, THEME_NAME, PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME, SPECIES, SPECIES_NAME, SPECIES_COVER, SPECIES_COVER_NAME, STRUCTURE_USE, STRUCTURE_USE_NAME, PHYSIOGRAPHY_COVER, ROAD_VERGE_A/B, MODAL_DBH, MOSAIC_PRECENT_AREA, EZ_DESC_07, LC07, LC07_NUM, COUNTRY, COUNTY.
- Coding and naming conventions reference established classifications (ITE Land Classification 2007, Broad Habitat classifications, JNCC guidance).

## Spatio-Temporal Scope
- Temporal coverage: year 1998.
- Spatial coverage: 1 km grid across Great Britain (England, Scotland, Wales).
- Output: polygon-level habitat areas and a rich set of ancillary attributes per polygon.

## Usage and Attribution
- All use of Countryside Survey data must be acknowledged.
- Required acknowledgement text: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and “Countryside Survey ©” with appropriate rights.
- Data sources and methodology links referenced (ITE Land Classification, Broad Habitat guidance, Countryside Survey website).

## Related References and Context
- Countryside Survey methodology and documents.
- ITE Land Classification of Great Britain (1996, 2007) and related Merlewood descriptions.
- Jackson (2000) guidance on Biodiversity Broad Habitat Classification.
- Data centre entry and DOIs/links for the LC07 dataset and methodology.