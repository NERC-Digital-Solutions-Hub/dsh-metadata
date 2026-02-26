# Landscape point feature data 2007 [Countryside Survey], Great Britain

## Overview
- Landscape point features from 566 1km squares across Great Britain, sampled in 2007.
- Source: Countryside Survey data © NERC - Centre for Ecology & Hydrology; dataset version 1: 04-2-2016.
- File: LANDSCAPE_PT_FEATURES_2007.csv; intended for map-based GIS analyses and visualization.

## Data contents and schema
- File details: Contains landscape point features at 1km resolution from the 2007 Countryside Survey.
- Key columns and their meaning:
  - SQUARE (text): 1km square sampling site code
  - YEAR (number): Year of survey
  - ID (number): Landscape point identifier (unique within a year)
  - THEME (number) / THEME_NAME (text): Theme code and name
  - PRIMARY_ATTRIBUTE (number) / PRIMARY_ATTRIBUTE_NAME (text): Primary attribute code and description
  - SPECIES (number) / SPECIES_NAME (text): Species code and name
  - PROPORTION (number) / PROPORTION_RANGE (text): Species cover code and range
  - USE (number) / USE_NAME (text): Structures theme land use
  - BUFFER (text): Buffer around veteran tree or pond
  - TREE_DEAD (text) / MISSING_LIMBS (text) / DEAD_WOOD (text) / DEAD_MISSING_BARK (text) / LIGHTNING_STRIKES (text) / HOLLOW_TRUNK (text): Veteran tree condition and features
  - MODAL_DBH (number) / MODAL_DBH_RANGE (text): Modal diameter at breast height code and range
  - VETERAN_TREE_TYPE (number) / VETERAN_TREE_TYPE_NAME (text): Veteran tree type code and name
  - EPIPHYTE_COVER (number) / EPIPHYTE_COVER_NAME (text): Epiphytic species cover code and name
  - IVY_COVER (number) / IVY_COVER_RANGE (text): Ivy cover code and range
  - CANOPY_LIVE (number) / CANOPY_LIVE_RANGE (text): Percent canopy live code and range
  - LC07 (text) / LC07_NUM (number): ITE Land Class 2007 description and numeric code
  - COUNTRY (text): Country (England ENG, Scotland SCO, Wales WAL)
  - COUNTY07 (text): County or Council area
  - EZ_DESC_07 (text): Countryside Survey Environmental Zone description
- Metadata and references are included to facilitate interpretation and cross-walking to classifications and habitat schemes.

## Usage notes for GIS work
- Scale and scope: Spatial resolution is 1km squares; suitable for landscape-scale analyses and map-based visualization.
- Coding and interpretation: Many columns use codes with corresponding NAME fields; use the NAME fields for human-readable mapping.
- Data integration: Data may need to be joined with other datasets (e.g., land classification or habitat classifications) using the provided codes (e.g., THEME_NAME, LC07, CANOPY_LIVE, etc.).
- Attribution: All use of Countryside Survey data requires explicit acknowledgement as described below.

## Usage and acknowledgement
- All use of Countryside Survey data must be acknowledged.
- Required acknowledgement text:
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
- Acknowledgement applies to copies of the data, publications, reports, and presentations.

## References and additional resources
- Countryside Survey Website: general overview and methodologies
- Countryside Survey Website: http://www.countrysidesurvey.org.uk/
- ITE Merlewood Land Classification (various foundational references for land classifications)
  - Bunce et al. 1996; 1981 (Land Classification of Great Britain)
  - Jackson 2000 (Guidance on Biodiversity Broad Habitat Classification)
  - Bunce et al. 2007 (ITE Land Classification of Great Britain 2007) – data centre references and DOIs
- Data centre and publication links provide methodological detail and crosswalks for interpreting classifications.