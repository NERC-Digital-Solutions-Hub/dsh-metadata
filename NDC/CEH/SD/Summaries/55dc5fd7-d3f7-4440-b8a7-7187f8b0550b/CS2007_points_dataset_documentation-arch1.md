# Landscape point feature data 2007 [Countryside Survey], Great Britain

## Overview
- Dataset of landscape point features from 566 1km squares across Great Britain, sampled in 2007 as part of the Countryside Survey.
- Data are owned by the NERC - Centre for Ecology & Hydrology (CEH); copyright applies.
- Acknowledgement and copyright notice required on all copies, publications, and presentations.

## Data content and structure
- Columns cover identification, attributes, and contextual classifications, including:
  - SQUARE (text): 1km square sampling site code
  - YEAR (number): Year of survey
  - ID (number): Landscape point identifier (unique within a year)
  - THEME (number) / THEME_NAME (text): Theme code and name
  - PRIMARY_ATTRIBUTE (number) / PRIMARY_ATTRIBUTE_NAME (text): Primary attribute code and name
  - SPECIES (number) / SPECIES_NAME (text): Species code and name
  - PROPORTION (number) / PROPORTION_RANGE (text): Species cover code and range
  - USE (number) / USE_NAME (text): Structures theme land use
  - BUFFER (text): Buffer around veteran tree or pond
  - VETERAN_TREE-related fields: TREE_DEAD, MISSING_LIMBS, DEAD_WOOD, DEAD_MISSING_BARK, LIGHTNING_STRIKES, HOLLOW_TRUNK
  - MODAL_DBH (number) / MODAL_DBH_RANGE (text): Modal diameter at breast height code and range
  - VETERAN_TREE_TYPE (number) / VETERAN_TREE_TYPE_NAME (text): Veteran tree type code and name
  - EPIPHYTE_COVER (number) / EPIPHYTE_COVER_NAME (text): Epiphytic species cover
  - IVY_COVER (number) / IVY_COVER_RANGE (text): Ivy cover code and range
  - CANOPY_LIVE (number) / CANOPY_LIVE_RANGE (text): Percent canopy live
  - LC07 (text) / LC07_NUM (number): ITE Land Class 2007 code and number
  - COUNTRY (text): Country (ENG, SCO, WAL)
  - COUNTY07 (text): County or council area
  - EZ_DESC_07 (text): Countryside Survey Environmental Zone description
- Data includes both coded values and human-readable names for many fields.

## Spatial and temporal scope
- Temporal coverage: Year 2007
- Spatial coverage: 566 1km squares across Great Britain (England, Scotland, Wales)

## Data use, integration and limitations
- Designed to support analysis of landscape features, land use, vegetation structure, and veteran tree attributes.
- Codes and names enable cross-walks with classification schemes (e.g., ITE Land Classification 2007).
- Some fields are categorical codes requiring lookup tables to interpret; data integration may require harmonising scales and units across datasets.
- Data scope is limited to 2007 snapshots; longitudinal analyses would require additional years.

## Access, acknowledgment, and references
- Acknowledgement required: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
- Usage rights: Countryside Survey ©/Database Right; all rights reserved; acknowledge in publications and presentations.
- References and context:
  - Countryside Survey Website for project overview and methodologies
  - Bunce et al. (1996, 2007) on ITE Land Classification of Great Britain
  - Jackson (2000) guidance on Biodiversity Broad Habitat Classification
  - DOI references for the ITE Land Classification GB 2007 dataset

## Practical considerations for analysts
- Data provenance and documentation are essential for correct interpretation of codes (THEME, PRIMARY_ATTRIBUTE, SPECIES, LC07, etc.).
- Cross-referencing with environmental classifications and land-use data enhances analytical potential.
- Ensure proper handling of veteran tree attributes and rare/qualitative fields (e.g., BUFFER, HOLLOW_TRUNK) during cleaning.
- Maintain the required acknowledgment in any data products and ensure proper citation of the referenced materials.