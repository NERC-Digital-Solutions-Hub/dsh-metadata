# Landscape area data 1998 [Countryside Survey], Great Britain

## Overview
- Data from the Countryside Survey (1998) covering landscape area features across Great Britain.
- Scope: 569 1km squares sampled; focuses on areas of Broad and Priority Habitats.
- Data is provided by NERC - Centre for Ecology & Hydrology.
- Two CSV files available:
  - LANDSCAPE_AREA_FEATURE_HAB_1998.csv – habitat area per 1km square.
  - LANDSCAPE_AREA_FEATURE_ATT_1998.csv – additional attributes for areas within the 1km squares.

## Files and scope (data content)
- LANDSCAPE_AREA_FEATURE_HAB_1998.csv
  - SQUARE: 1km square sampling site code
  - YEAR: Survey year (1998)
  - ID: Landscape area polygon identifier (unique within a year)
  - BROAD_HABITAT: Broad habitat code
  - BROAD_HABITAT_NAME: Broad and Priority Habitat (as per Jackson 2000)
  - AREA: Habitat area within the 1km polygon (square metres)
  - LC07: ITE Land Class 2007 code
  - LC07_NUM: ITE Land Class 2007 numeric code
  - COUNTRY: England (ENG), Scotland (SCO), Wales (WAL)
  - COUNTY: County or Council region
  - EZ_DESC_07: Countryside Survey Environmental Zone description (see accompanying document)

- LANDSCAPE_AREA_FEATURE_ATT_1998.csv
  - YEAR: Year of survey
  - SQUARE: 1km square sampling site code
  - ID: Landscape area polygon identifier
  - THEME: Theme code
  - THEME_NAME: Theme description (land use)
  - PRIMARY_ATTRIBUTE: Primary attribute code
  - PRIMARY_ATTRIBUTE_NAME: Description of primary attribute
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
  - ROAD_VERGE_A_NAME: Road verge A width description
  - ROAD_VERGE_B: Road Verge B code
  - ROAD_VERGE_B_NAME: Road verge B width description
  - MODAL_DBH: Modal DBH (Diameter at Breast Height) code
  - MODAL_DBH_NAME: Modal DBH description
  - MOSAIC_PRECENT_AREA: Proportion of area assigned to Broad Habitat in a mosaic habitat
  - LC07: ITE Land Class 2007 code
  - LC07_NUM: ITE Land Class 2007 numeric code
  - COUNTRY: Country location (ENG/SCO/WAL)
  - COUNTY: County or Council
  - EZ_DESC_07: Environmental Zone description (see above)

## Data provenance, standards and licensing
- Acknowledgement and copyright: All Countryside Survey data must be acknowledged in copies, publications, and presentations.
  - Acknowledgement text: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- References and classifications used:
  - ITE Merlewood Land Classification of Great Britain (1996, 1981) and ITE Land Classification of Great Britain 2007 (Bunce et al.).
  - Biodiversity Broad Habitat Classification guidance (Jackson, 2000).
- Relevant publications and links are provided for methodology and classifications, including the Countryside Survey website and DOI links for the 2007 ITE classification dataset.

## Data governance and stewardship considerations for Data Leaders
- Data system scope: Baseline 1998 landscape habitat data across GB at 1km resolution, with both habitat area and rich attribute data.
- Metadata and discoverability: Rich attribute fields and standardized codes (e.g., LC07, COUNTRY, EZ_DESC_07) support interoperability but require clear metadata to interpret codes and names.
- Data quality and standards:
  - Uses established classifications (ITE GB 2007, Broad Habitat classifications).
  - Some fields are coded values with corresponding lookup descriptions; ensure maintained mappings for interpretability.
- Data access and attribution:
  - Explicit acknowledgement requirements accompany all uses; plan for governance to enforce attributions in products, dashboards, and publications.
- Collaboration and reuse:
  - Data is framed to support broader data system goals (co-ownership of data products, cross-network collaboration, and integration with wider datasets).
- Potential limitations to consider:
  - Snapshot from 1998; historical baseline data rather than current conditions.
  - Complex, multi-field schema requiring careful interpretation of codes and their mappings.
  - Some fields (e.g., MOSAIC_PRECENT_AREA) may require careful handling due to potential typographical inconsistencies in headers.

## References and further reading
- Countryside Survey Website – general overview and methodology
- ITE Merlewood Land Classification of Great Britain (1996)
- ITE Land Classification of Great Britain 2007 (Bunce et al.)
- Jackson, D.L. (2000) Guidance on Broad Habitat Classification
- Publications detailing datasets and data centre records (NERC Environmental Information Data Centre)