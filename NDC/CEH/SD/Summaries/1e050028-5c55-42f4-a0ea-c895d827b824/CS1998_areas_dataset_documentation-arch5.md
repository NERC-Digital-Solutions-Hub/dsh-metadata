# Landscape area data 1998 [Countryside Survey], Great Britain
Version: 1: 15-1-2016
Countryside Survey data © NERC - Centre for Ecology and Hydrology

## Overview
- Dataset comprising landscape area data from the 1998 Countryside Survey for Great Britain, covering 569 1km squares.
- Two CSV files provide habitat areas and detailed attributes for landscape areas within each 1km square.

## Data files and schema

### LANDSCAPE_AREA_FEATURE_HAB_1998.csv
- Purpose: Areas of Broad and Priority Habitats within each 1km square sampled in 1998.
- Key columns:
  - SQUARE: 1km square sampling site code
  - YEAR: Year of survey
  - ID: Landscape area polygon identifier (unique within a year)
  - BROAD_HABITAT: Broad Habitat code
  - BROAD_HABITAT_NAME: Broad and Priority Habitat name (Jackson, 2000)
  - AREA: Area of habitat within the 1km polygon (square metres)
  - LC07: ITE Land Class 2007 code
  - LC07_NUM: ITE Land Class 2007 numeric code
  - COUNTRY: Country (England ENG, Scotland SCO, Wales WAL)
  - COUNTY: County or Council
  - EZ_DESC_07: Environmental Zone description (see linked reference)

### LANDSCAPE_AREA_FEATURE_ATT_1998.csv
- Purpose: Additional attributes for areas within 569 1km squares sampled in 1998.
- Key columns (examples):
  - YEAR, SQUARE, ID: Identifiers aligning with HAB file
  - THEME, THEME_NAME: Land use theme codes and descriptions
  - PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME: Primary attribute code and description
  - SPECIES, SPECIES_NAME, SPECIES_COVER, SPECIES_COVER_NAME: Species-related data
  - PRIMARY_QUALIFIER, PRIMARY_QUALIFIER_NAME: Qualifier codes and descriptions
  - STRUCTURE_USE, STRUCTURE_USE_NAME: Structure use codes and descriptions
  - PHYSIOGRAPHY_COVER, PHYSIOGRAPHY_COVER_NAME: Inland Physiography cover descriptions
  - ROAD_VERGE_A, ROAD_VERGE_A_NAME: Road verge width codes and descriptions
  - ROAD_VERGE_B, ROAD_VERGE_B_NAME: Additional road verge descriptors
  - MODAL_DBH, MODAL_DBH_NAME: Modal Diameter at Breast Height descriptions
  - MOSAIC_PRECENT_AREA: Proportion of area assigned to Broad Habitat in a mosaic habitat
  - LC07, LC07_NUM: ITE Land Class 2007 codes
  - COUNTRY, COUNTY: Geographic identifiers
  - EZ_DESC_07: Environmental Zone description (see linked reference)

## Data governance, provenance, and licensing
- Data provenance: Sourced from Countryside Survey; uses established classifications (ITE Land Classification 1996/2007; Broad Habitat Classification per Jackson 2000).
- Usage acknowledgement required: All uses must acknowledge Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; include Countryside Survey © and copyright notice.
- References and methodology: Provides links to Countryside Survey website and key publications for methodologies and classification schemes (ITE Land Classification GB 1996/2007; Broad Habitat guidance; related JNCC references).

## Access, sharing, and metadata considerations
- Designed for broad discovery and reuse; typically shared via data portals/catalogues.
- When sharing or publishing results, apply the required acknowledgement text and citations.
- Metadata considerations for stewardship:
  - Ensure alignment between HAB and ATT files using SQUARE, YEAR, and ID.
  - Preserve geographic context (COUNTRY, COUNTY) and classification codes (LC07, EZ_DESC_07).
  - Maintain versioning and provenance to reflect the 1998 survey basis.

## Practical notes for Data Stewards
- Data quality and interoperability:
  - Recognize the use of historical classifications (ITE GB Land Classification 1996/2007) and Broad Habitat definitions; document any mapping decisions if harmonizing with newer schemas.
  - Be aware of potential format/spatial resolution differences if integrating with other datasets (1km square granularity; unique per-year IDs).
- Documentation and citations:
  - Include the required acknowledgement on all copies, publications, and presentations.
  - Reference the primary sources listed (Countryside Survey website, Bunce et al., Jackson 2000, ITE 2007) to support interpretation and reuse.