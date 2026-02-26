# 10km occurrence data for terrestrial mammals in Great Britain and Northern Ireland, 1960-1992 & 2000-2016, as mapped in the 2020 Mammal Atlas.

## Overview
- Presents summarised 10km grid-square occurrence data for mammal species from the 1960-1992 and 2000-2016 atlas periods (cetaceans excluded from this dataset).
- For each species, lists 10km grid squares with recorded occurrences during the two atlas periods.
- Includes both the current atlas period (2000-2016) and the previous atlas period (1960-1992) as applicable.
- Available in CSV and GeoPackage formats, enabling GIS-based analysis.

## Background to the Atlas
- Atlas of the Mammals of Great Britain and Northern Ireland (Crawley et al. 2020) describes current distributions and changes since the 1993 atlas.
- Built on the Mammal Watch South East (MaWSE) project, which led to the Mammal Tracker app; now superseded by Mammal Mapper.
- Project expanded UK-wide with Sea Watch Foundation; cetaceans added but not included in this dataset.
- Related outputs include population status reviews and red lists; contributed to State of Nature 2019.

## Data collection and validation
- Data sources include the National Biodiversity Network gateway (NBN Atlas), local biological records centres, monitoring schemes, Natural England, Mammal Society, Biological Records Centre, Sea Watch Foundation, iRecord, and Mammal Tracker.
- Mix of opportunistic, citizen-science records and more structured surveys; verification varies by source.
- Mammal Society verifiers validate data from iRecord and Mammal Tracker; external sources are assumed credible unless stated otherwise; some datasets with potential misidentifications were treated with extra caution.
- To minimise dubious records for harder-to-identify species, only records for widespread species (e.g., mole, rabbit, badger, fox, hedgehog) from certain datasets were included.
- 10km square occurrence maps reviewed by species experts; records in flagged squares re-evaluated at the record level before final map production.

## Cetaceans
- Cetacean accounts and maps exist but are produced separately by Sea Watch; cetacean data are not integrated into this atlas dataset.
- For cetacean inquiries or recording, contact Sea Watch.

## Dataset Structure
- Provided as a CSV with per-species 10km grid squares where occurrences were recorded in 1960-1992 and/or 2000-2016.
- Includes:
  - SPECIES: scientific name
  - COMMON_NAME: common name
  - GRIDREF: 10km grid square reference (OGB for GB, OSI for NI, truncated MGRS for Channel Islands)
  - CATEGORY: time period category (1960-1992; 1960-1992 & 2000-2016; 2000-2016)
  - TP_1960_1992: presence in 1960-1992 (1 = observed)
  - TP_2000_2016: presence in 2000-2016 (1 = observed)
  - LATITUDE, LONGITUDE: center of the 10km grid square (WGS84)
  - ENG, SCO, WAL, N_IRE, CD: country/area inclusions (1 = within)
- Also provided as a Geopackage (.gpkg) with 10km square boundaries mapped as polygons for GIS analyses (OSGB 36 / EPSG: 27700).
  - Channel Islands and Northern Ireland squares re-projected to British Grid; each species has a separate layer.
  - Attribute fields match the CSV schema.

## Implications for GIS Work
- Ready-to-use data products for map-based analysis of mammal distributions across GB&I over two atlas periods.
- Two formats (CSV and GeoPackage) support flexible GIS workflows and spatial analyses.
- Coordinate and grid reference systems clearly documented, with cross-border assignments and coastal/marine squares included.
- Data quality is variably validated due to diverse data sources; users should consider source-level validation notes and the expert review process when assessing record-level reliability.
- Cetacean data are not included in this dataset; consult Sea Watch for cetacean-specific mapping.

## References
- Arnold, H. (1993). Atlas of mammals in Britain.
- Hayhow et al. (2019). The State of Nature 2019.
- Mathews et al. (2018). A Review of the Population and Conservation Status of British Mammals.
- Mathews & Harrower (2020). IUCN - compliant Red List for Britain's Terrestrial Mammals.