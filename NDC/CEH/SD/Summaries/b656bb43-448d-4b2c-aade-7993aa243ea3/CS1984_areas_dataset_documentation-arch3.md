# Landscape area data 1984 [Countryside Survey], Great Britain Version: 1: 15-1-2016

- Two CSV data files from the Countryside Survey 1984 covering landscape areas across Great Britain
  - LANDSCAPE_AREA_FEATURE_HAB_1984.csv
  - LANDSCAPE_AREA_FEATURE_ATT_1984.csv
- Coverage and timing
  - 379 1km squares sampled across Great Britain
  - Year of survey: 1984
- Acknowledgement and rights
  - All use of Countryside Survey data must be acknowledged
  - Copyright: Countryside Survey © NERC - Centre for Ecology & Hydrology; all rights reserved

## Data Structure and Key Fields

- LANDSCAPE_AREA_FEATURE_HAB_1984.csv
  - SQUARE: 1km square sampling site code
  - YEAR: Year of survey
  - ID: Landscape area polygon identifier (unique within a year)
  - BROAD_HABITAT: Broad habitat code
  - BROAD_HABITAT_NAME: Broad and Priority Habitat name (Jackson, 2000)
  - AREA: Area of habitat within 1km polygon (square metres)
  - LC07: ITE Land Class 2007 code
  - LC07_NUM: ITE Land Class 2007 numeric code
  - COUNTRY: England (ENG), Scotland (SCO), Wales (WAL)
  - COUNTY: County (Eng & Wal) or Council (Sco)
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- LANDSCAPE_AREA_FEATURE_ATT_1984.csv
  - YEAR, SQUARE, ID: Identifiers as above
  - THEME, THEME_NAME: Theme and description (land use)
  - PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME: Primary attribute codes and descriptions
  - SPECIES, SPECIES_NAME: Species code/name
  - SPECIES_COVER, SPECIES_COVER_NAME: Species cover code/name
  - PRIMARY_QUALIFIER, PRIMARY_QUALIFIER_NAME: Qualifier codes and descriptions
  - STRUCTURE_USE, STRUCTURE_USE_NAME: Structural/use description
  - PHYSIOGRAPHY_COVER, PHYSIOGRAPHY_COVER_NAME: Inland physiography cover descriptions
  - ROAD_VERGE_A, ROAD_VERGE_A_NAME: Road verge width and description (Transport Theme)
  - ROAD_VERGE_B, ROAD_VERGE_B_NAME: Additional road verge attribute
  - MODAL_DBH, MODAL_DBH_NAME: Modal DBH (diameter at breast height) and description
  - LC07, LC07_NUM: ITE Land Class 2007 codes
  - COUNTRY, COUNTY: Geographic location indicators
  - EZ_DESC_07: Environmental Zone description (as above)

## Data Use and Governance

- Purpose and provenance
  - Designed as landscape-scale habitat and attribute data for 1984 baseline assessments
  - Related publications and methodologies outlined in References
- Data usage requirements
  - Acknowledge Countryside Survey data ownership and copyright in all copies, publications, and presentations
  - Data linked to ITE Land Classification and biodiversity habitat frameworks (see references)
- Data access considerations for monitoring frameworks
  - Baseline for habitat extent and land-use characteristics across GB
  - Enables examination of habitat area within 1km squares and associations with land-class, environmental zones, and other attributes
  - Potentially supports temporal monitoring when paired with data from other years (not specified in document)
- Data quality and metadata considerations
  - Comprehensive field definitions provided (codes, names, and descriptors)
  - Some interpretation requires cross-referencing ITE Land Classification (LC07) and habitat definitions (Jackson, 2000; JNCC guidance)
  - Metadata completeness and ease of data integration depend on accompanying methodologies and data dictionaries (referenced in publications)

## Relevance for Monitoring Frameworks

- Environmental health measures
  - Extent and distribution of Broad and Priority Habitats across GB
  - Variation in habitat area by 1km square, enabling spatial trend analysis
  - Alignment of habitat data with land-class classifications (ITE LC07) and environmental zones
- Indicator development possibilities
  - Habitat area per square metre by country/county
  - Relationship between habitat area and landscape attributes (theme, primary attribute, structure use)
  - Linkages between habitat extent and physiography, road verge characteristics, and DBH distributions
- Data governance and transparency
  - Clear attribution requirements support responsible data sharing in monitoring outputs
  - Complex attribute set supports multi-metric policy evaluation, provided metadata and definitions are applied consistently

## References and Related Resources

- Countryside Survey Website: general overview and methodologies
- Bunce et al. (1996, 1997): ITE Merlewood Land Classification guidance
- Jackson (2000): Guidance on Biodiversity Broad Habitat Classification and its relationship to other classifications
- Bunce et al. (2007): ITE Land Classification of Great Britain 2007 dataset
- Data Centre references: NERC Environmental Information Data Centre and related links