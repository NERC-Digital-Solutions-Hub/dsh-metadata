# Landscape area data 2007 [Countryside Survey], Great Britain

- The dataset captures areas of Broad and Priority Habitats from 591 sampled 1km squares across Great Britain in 2007, excluding refused access areas.
- Data are provided in two CSV files: one for habitat areas and one for additional attributes.

## Datasets Included

- LANDSCAPE_AREA_FEATURE_HAB_2007.csv
  - Contains habitat area information within each 1km square.
  - Key fields: SQUARE, YEAR, ID, BROAD_HABITAT, BROAD_HABITAT_NAME, AREA (square metres), LC07, LC07_NUM, COUNTRY, COUNTY, EZ_DESC_07, plus various identifiers describing the 1km square sampling site.

- LANDSCAPE_AREA_FEATURE_ATT_2007.csv
  - Contains additional attribute data corresponding to the same 1km square areas.
  - Key fields: YEAR, SQUARE, ID, THEME, THEME_NAME, PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME, SPECIES, SPECIES_NAME, SPECIES_COVER, SPECIES_COVER_NAME, PRIMARY_QUALIFIER, PRIMARY_QUALIFIER_NAME, STRUCTURE_USE, STRUCTURE_USE_NAME, PHYSIOGRAPHY_COVER, PHYSIOGRAPHY_COVER_NAME, ROAD_VERGE_A, ROAD_VERGE_A_NAME, ROAD_VERGE_B, ROAD_VERGE_B_NAME, MODAL_DBH, MODAL_DBH_NAME, MOSAIC_PRECENT_AREA, LC07, LC07_NUM, COUNTRY, COUNTY, EZ_DESC_07, among others.
  - Note: Includes a mix of land-use themes, biodiversity attributes, landscape structure, vegetation descriptors, and infrastructure-related variables.

## Key Variables (highlights)

- Habitat data (LANDSCAPE_AREA_FEATURE_HAB_2007.csv)
  - SQUARE, YEAR, ID: identifiers for the 1km sampling site and year.
  - BROAD_HABITAT, BROAD_HABITAT_NAME: Broad and Priority Habitat classifications (Jackson, 2000).
  - AREA: Habitat area within the 1km square (square metres).
  - LC07, LC07_NUM: ITE Land Classification 2007 codes.
  - COUNTRY, COUNTY: geographic location at country/county level.
  - EZ_DESC_07: Countryside Survey Environmental Zone description.

- Attribute data (LANDSCAPE_AREA_FEATURE_ATT_2007.csv)
  - THEME, THEME_NAME, PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME: thematic categorisations (e.g., land use themes).
  - SPECIES, SPECIES_NAME, SPECIES_COVER, SPECIES_COVER_NAME: species-related descriptors and cover values.
  - PRIMARY_QUALIFIER, PRIMARY_QUALIFIER_NAME: qualifiers for primary attributes.
  - STRUCTURE_USE, STRUCTURE_USE_NAME: structure/use descriptions.
  - PHYSIOGRAPHY_COVER, PHYSIOGRAPHY_COVER_NAME: physiography-related coverage descriptions.
  - ROAD_VERGE_A, ROAD_VERGE_A_NAME; ROAD_VERGE_B, ROAD_VERGE_B_NAME: road verge characteristics (width-related).
  - MODAL_DBH, MODAL_DBH_NAME: modal diameter at breast height (forestry-related).
  - MOSAIC_PRECENT_AREA: proportion of area in mosaic habitat (note the dataset uses MOSAIC_PRECENT_AREA as named here).
  - COUNTRY, COUNTY, LC07, LC07_NUM, EZ_DESC_07: geographic and classification fields aligned with the habitat data.

## Spatial and Temporal Scope

- Temporal coverage: Year 2007 (Countryside Survey).
- Spatial coverage: Great Britain (England, Scotland, Wales).
- Sampling scope: 591 1km squares; refused access areas excluded.

## Data Quality, Scope and Limitations

- Snapshot in time: 2007 data; may need updates or contemporary comparisons for trend analysis.
- Scale: 1km square resolution; results are aggregated to this spatial unit.
- Data integration: attributes span multiple themes and classifications and may require careful alignment with ITE Land Classification (LC07) and environmental zone descriptions.
- Access and usability: some data elements are descriptive and may require cross-referencing to related classifications and publications.

## Access, Acknowledgement and Use

- All use of Countryside Survey data must be acknowledged.
- Acknowledgement text to be used on copies and presentations:
  - “Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology”
  - “Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.”

## References and Related Publications

- Countryside Survey Website: general overview and methodologies.
- Bunce, R.G.H., Barr, C.J., Clarke, R.T., Howard, D.C. & Lane, A.M.J. (1996). ITE Merlewood Land Classification of Great Britain.
- Bunce, R.G.H. et al. (1996, 2007). ITE Land Classification of Great Britain (studies describing the classification system and its 2007 update).
- Jackson, D.L. (2000). Guidance on interpretation of the Biodiversity Broad Habitat Classification (JNCC Report 307).
- Bunce, R.G.H. et al. (2007). ITE Land Classification of Great Britain 2007 (NERC Environmental Information Data Centre).
- DOIs/links provided in the original documentation for the 2007 ITE Land Classification and related materials.