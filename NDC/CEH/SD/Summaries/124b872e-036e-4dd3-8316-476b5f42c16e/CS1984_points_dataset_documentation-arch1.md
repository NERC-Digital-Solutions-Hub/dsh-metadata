# Landscape point feature data 1984 [Countryside Survey], Great Britain

## Overview
- Landscape point features from 322 1km squares across Great Britain, sampled in 1984.
- Dataset title and source: LANDSCAPE_PT_FEATURES_1984.csv, Countryside Survey data © NERC - Centre for Ecology & Hydrology.
- Version and date: Version 1: 04-2-2016.

## Data content and structure
- File: LANDSCAPE_PT_FEATURES_1984.csv
- Core attributes:
  - SQUARE: 1km square sampling site code (text)
  - YEAR: Year of survey (numeric)
  - ID: Landscape point identifier (unique within a year)
  - THEME, THEME_NAME: Theme code and descriptive name
  - PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME: Primary attribute code and name
  - SPECIES, SPECIES_NAME: Species code and scientific/common name
  - PROPORTION, PROPORTION_RANGE: Species cover code and range value
  - USE, USE_NAME: Use code and description
  - MODAL_DBH, MODAL_DBH_RANGE: Estimated age (DBH) information and range
  - LC07 (text), LC07_NUM: ITE Land Classification 2007 (text) and numeric code
  - COUNTRY: Country in which the 1km square is located (ENG, SCO, WAL)
  - COUNTY07: County (England & Wales) or Council (Scotland)
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- Notes:
  - The dataset references ITE Merlewood/Land Classification and related classifications (1996–2007) and links to methodological documents.

## Data usage and attribution
- All use of Countryside Survey data must be acknowledged.
- Required acknowledgement text:
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."

## References and related publications
- Countryside Survey website (general overview and methodologies): http://www.countrysidesurvey.org.uk/
- Bunce et al. (1996): ITE Merlewood Land Classification of Great Britain (Journal of Biogeography)
- Bunce et al. (1981): Land Classes in Great Britain: Preliminary Descriptions for Users of the Merlewood Method of Land Classification (Merlewood RD/Development)
- Jackson (2000): Guidance on interpretation of the Biodiversity Broad Habitat Classification (JNCC Report 307)
- Bunce et al. (2007): ITE Land Classification of Great Britain 2007 (NERC Environmental Information Data Centre)
- DOIs/links provided in the original documentation for each reference

## Practical considerations for analysts
- Scale and scope: Data are at 1km square resolution from 1984; useful for historical baseline analyses and cross-walking with later land classifications (e.g., LC07).
- Data integration: Contains multiple related classifications and attribute codes; may require crosswalks to harmonize schemes across years.
- Data quality and access: Metadata and related documentation are essential for correct interpretation of themes, attributes, and classifications.
- Analytical opportunities: Explore correlations between landscape themes, species cover, land-use codes, and land classifications; build historical baselines and predictive models where compatible with other datasets.
- Documentation and reproducibility: Maintain provenance by tracking data sources, versions, and the required acknowledgement statements in all outputs.