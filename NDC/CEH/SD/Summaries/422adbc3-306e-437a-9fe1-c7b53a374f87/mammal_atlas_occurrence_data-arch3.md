# 10km occurrence data for terrestrial mammals in Great Britain and Northern Ireland, 1960-1992 & 2000-2016, as mapped in the 2020 Mammal Atlas

## Overview
- Describes current distribution of mammals and changes since the 1993 atlas.
- Provides summarized 10km-resolution occurrence data for all atlas species except cetaceans.
- Lists 10km grid squares with recorded occurrences during 2000-2016 and/or 1960-1992.

## Background to the Atlas
- Produced by the Mammal Society with assistance from Sea Watch Foundation, Biological Records Centre, UK Centre for Ecology and Hydrology, and Staffordshire Mammal Group.
- Originated from the Mammal Watch South East (MaWSE) project to engage the public and create an online atlas; culminated in the Mammal Mapper app (succeeded Mammal Tracker).
- Expanded data collection to the UK, Isle of Man, and Channel Islands; cetaceans included with Sea Watch but data not integrated into the atlas dataset.
- Contributions to related outputs: review of population/conservation status (2018) and national/regional red lists (2020), and involvement in State of Nature 2019.

## Data collection and validation
- Data drawn from diverse sources: National Biodiversity Network (NBN) gateway, local biological records centres, monitoring schemes, Natural England, Mammal Society, Biological Records Centre, Sea Watch Foundation, iRecord, and Mammal Tracker app.
- Source methods vary: mostly opportunistic volunteer records, plus structured surveys and professional research data.
- Validation:
  - iRecord and Mammal Tracker submissions validated by Mammal Society verifiers.
  - External datasets often pre-validated; detailed validation procedures not always documented; credibility assumed unless stated.
  - Some datasets contributed many dubious or erroneous records for less common species; to mitigate risk, only records for widespread species from these datasets were included.
  - Expert review of 10km squares by species experts; records in flagged squares subjected to record-level review before inclusion.
- Cetaceans are handled separately by Sea Watch (not included in the atlas dataset).

## Cetaceans
- Cetacean data exist but are not integrated into the atlas dataset; atlas maps for these species are produced by Sea Watch. For inquiries or recording cetaceans, contact Sea Watch.

## Dataset Structure
- Format: CSV with per-species records of 10km grid squares where occurrences were recorded in 1960-1992 and/or 2000-2016.
- Fields include:
  - SPECIES (scientific name), COMMON_NAME, GRIDREF, CATEGORY (time period coverage: 1960-1992; 1960-1992 & 2000-2016; 2000-2016), TP_1960_1992, TP_2000_2016, LATITUDE, LONGITUDE, ENG, SCO, WAL, N_IRE, CD.
- Grid references:
  - OGB for Scotland/England/Wales/IOM, OSI for Northern Ireland, truncated MGRS for Channel Islands.
  - Some Channel Islands grid references shown in truncated MGRS form.
- Geographic data:
  - Includes coastal/marine squares assigned to the nearest country.
- Geopackage alternative:
  - Provided as .gpkg with same attributes, OSGB 36 (EPSG:27700) CRS.
  - NI and Channel Islands squares re-projected to British Grid; separate layers per species.

## Governance, metadata, and data usability
- Emphasis on data provenance, quality assurance, and transparent validation steps.
- Metadata considerations include varying data collection methods and the need for expert review to ensure reliability.
- Data sharing and openness balanced with reliance on multiple sources and provisional validation status; provides a clear framework for using these occurrences in monitoring and policy evaluation.

## References
- Arnold, 1993; Hayhow et al., 2019; Mathews et al., 2018; Mathews & Harrower, 2020.