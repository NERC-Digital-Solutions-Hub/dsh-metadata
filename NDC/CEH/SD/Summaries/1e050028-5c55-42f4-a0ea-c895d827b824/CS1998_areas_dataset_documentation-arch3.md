# Landscape area data 1998 [Countryside Survey], Great Britain

## Overview
- Provides landscape area data from the Countryside Survey (GB) for 1998, sampled across 569 1km squares.
- Two main CSV files:
  - LANDSCAPE_AREA_FEATURE_HAB_1998.csv: habitat areas by 1km square, including Broad Habitat codes and area in square metres.
  - LANDSCAPE_AREA_FEATURE_ATT_1998.csv: additional attributes for the same areas, covering themes, species, structure, physiography, road verge data, DBH, mosaic area, and related classifications.
- Data drawn from established classifications and systems (e.g., ITE Land Classification 2007, Broad Habitat Classification).
- Geographic and administrative fields included: SQUARE, COUNTRY, COUNTY, plus environmental zone descriptions (EZ_DESC_07).

## Data Files and Key Fields
- LANDSCAPE_AREA_FEATURE_HAB_1998.csv
  - SQUARE: 1km square sampling site code
  - YEAR: survey year
  - ID: polygon identifier (unique within a year)
  - BROAD_HABITAT / BROAD_HABITAT_NAME: broad and priority habitat codes and names
  - AREA: habitat area within the 1km square (square metres)
  - LC07 / LC07_NUM: ITE Land Classification (2007)
  - COUNTRY / COUNTY: geographic location (England, Scotland, Wales)
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- LANDSCAPE_AREA_FEATURE_ATT_1998.csv
  - YEAR / SQUARE / ID: identifiers as above
  - THEME / THEME_NAME: theme codes and descriptions (land use)
  - PRIMARY_ATTRIBUTE / PRIMARY_ATTRIBUTE_NAME
  - SPECIES / SPECIES_NAME / SPECIES_COVER / SPECIES_COVER_NAME
  - PRIMARY_QUALIFIER / PRIMARY_QUALIFIER_NAME
  - STRUCTURE_USE / STRUCTURE_USE_NAME
  - PHYSIOGRAPHY_COVER / PHYSIOGRAPHY_COVER_NAME
  - ROAD_VERGE_A / ROAD_VERGE_A_NAME
  - ROAD_VERGE_B / ROAD_VERGE_B_NAME
  - MOSAIC_PRECENT_AREA
  - LC07 / LC07_NUM / COUNTRY / COUNTY / EZ_DESC_07 (as above)
- All use of Countryside Survey data requires proper acknowledgement and copyright notice.

## Data Provenance, Rights, and Standards
- Data owned by NERC – Centre for Ecology & Hydrology; Countryside Survey © and copyright held.
- Acknowledgement required on all copies, publications, and presentations:
  - Acknowledgement: Countryside Survey data owned by NERC - CEH
  - Countryside Survey © Database Right/Copyright CEH
- References and methodological context are provided (e.g., links to Countryside Survey website and publications detailing land classification systems and biodiversity broad habitats).

## Relevance for Monitoring Frameworks
- Delivers spatially explicit, time-stamped habitat area data across GB, suitable for evaluating environmental health policy and monitoring changes over time.
- Enables integration with other thematic attributes (land use, biodiversity indicators, physiography, road verges) for multi-criteria assessments.
- Supports standardization through recognized classifications (ITE Land Classification 2007, Broad Habitat classifications) and standardized geographic descriptors (country, county, environmental zones).
- Provides a structured data-goundation for dashboards, reports, and policy evaluations, with clear metadata fields and provenance.

## Data Governance and Accessibility Considerations
- Public sharing of datasets is required for use in outputs, which aligns with open-data practices but can pose barriers if metadata or access to origin datasets are incomplete.
- Metadata completeness and data provenance are essential to ensure datasets meet standards and can be validated for monitoring purposes.
- Data may require transformation to align with other datasets or monitoring frameworks, given the presence of multiple classification schemes and attribute fields.

## References and Further Reading
- Countryside Survey Website: general overview and methodology
- ITE Merlewood Land Classification of Great Britain (1996)
- ITE Land Classification of Great Britain 2007
- Guidance on Biodiversity Broad Habitat Classification (Jackson, 2000)
- Related R&D papers and datasets (DOIs/links provided in the reference section)