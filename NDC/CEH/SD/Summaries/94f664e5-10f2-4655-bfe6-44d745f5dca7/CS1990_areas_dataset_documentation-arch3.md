# Landscape area data 1990 [Countryside Survey], Great Britain

## Overview
- A Countryside Survey dataset describing landscape area and habitat information for Great Britain based on 506 1km squares surveyed in 1990.
- Contains two CSV files: one with habitat area by square and year, and another with additional attributes for landscape areas within those squares.
- Data are owned by NERC - Centre for Ecology & Hydrology (CEH) and require acknowledgment in all copies, publications, and presentations.
- Version: 1, dated 15-01-2016.

## Data content

- Landscape_area_feature_hab_1990.csv
  - Areas of Broad and Priority Habitats within each 1km square.
  - Key columns:
    - SQUARE: 1km square code
    - YEAR: survey year
    - ID: polygon identifier (unique within a year)
    - BROAD_HABITAT: Broad habitat code
    - BROAD_HABITAT_NAME: broad habitat name (e.g., as per Jackson 2000)
    - AREA: habitat area within the square (in square metres)
    - LC07: ITE Land Class 2007 code and LC07_NUM
    - COUNTRY: England (ENG), Scotland (SCO), or Wales (WAL)
    - COUNTY: county or council area
    - EZ_DESC_07: environmental zone description

- Landscape_area_feature_att_1990.csv
  - Additional attributes for the landscape areas within the 1km squares.
  - Key columns (sample):
    - YEAR, SQUARE, ID
    - THEME, THEME_NAME: thematic classification (land use)
    - PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME
    - SPECIES, SPECIES_NAME, SPECIES_COVER, SPECIES_COVER_NAME
    - PRIMARY_QUALIFIER, PRIMARY_QUALIFIER_NAME
    - STRUCTURE_USE, STRUCTURE_USE_NAME
    - PHYSIOGRAPHY_COVER, PHYSIOGRAPHY_COVER_NAME
    - ROAD_VERGE_A, ROAD_VERGE_A_NAME
    - ROAD_VERGE_B, ROAD_VERGE_B_NAME
    - MODAL_DBH, MODAL_DBH_NAME
    - LC07, LC07_NUM
    - COUNTRY, COUNTY
    - EZ_DESC_07

## Data schema and interpretation

- 506 1km squares across Great Britain are sampled.
- Habitat file provides spatially-resolved habitat extents within each square and links to land classification (ITE Land Class 2007) and environmental zone descriptors.
- Attributes file adds multi-dimensional landscape context including land use themes, species presence/cover, structural uses, physiography, road verge characteristics, and dbh information.
- Both files enable calculation of habitat extents, thematic landscape composition, and integration with other ecological classifications for monitoring frameworks.

## Usage, governance, and limitations

- Data use requires explicit acknowledgment:
  - Acknowledgement: Countryside Survey data owned by NERC - CEH
  - Copyright: Countryside Survey © NERC CEH. All rights reserved.
  - Use in publications, reports, and presentations must include the acknowledgment above.
- Metadata and accessibility considerations:
  - The dataset uses standardized codes (e.g., LC07, THEME) with descriptive names to aid interpretability and comparability.
  - Some metadata quality aspects may require verification (e.g., consistency of codes across years or datasets) to ensure suitability for monitoring indicators.
- Implications for monitoring frameworks:
  - Enables tracking of habitat area changes over time when combined with later Countryside Survey data or other years.
  - Facilitates construction of landscape-level indicators (habitat extent, land-class distributions, environmental zone coverage, and structure/use attributes).
  - Requires data governance and transparency in data sharing to maintain open, reproducible monitoring outputs.

## Relevant publications and references

- Countryside Survey Website: general overview and methodologies
- Bunce, R.G.H., Barr, C.J., Clarke, R.T., Howard, D.C. & Lane, A.M.J. (1996) ITE Merlewood Land Classification of Great Britain. Journal of Biogeography, 23, 625-634
- Bunce, R.G.H., Barr, C.J., Whittaker, H.A. (1981) Land Classes in Great Britain: Preliminary Descriptions for Users of the Merlewood Method of Land Classification
- Jackson, D.L. (2000) Guidance on the interpretation of the Biodiversity Broad Habitat Classification (terrestrial and freshwater types): Definitions and the relationship with other classifications, JNCC Report 307
- Bunce, R.G.H., Barr, C.J., Clarke, R.T., Howard, D.C., Scott, W.A. (2007) ITE Land Classification of Great Britain 2007. NERC Environmental Information Data Centre. doi:10.5285/5f0605e4-aa2a-48ab-b47c-bf5510823e8f
- Countryside Survey Website references and linked methodologies and documents