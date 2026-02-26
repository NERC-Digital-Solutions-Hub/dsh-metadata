# 10km occurrence data for terrestrial mammals in Great Britain and Northern Ireland, 1960-1992 & 2000-2016, as mapped in the 2020 Mammal Atlas

## Overview
- Provides summarized 10km grid square occurrences for terrestrial mammals in GB and NI, excluding cetaceans.
- Covers two atlas recording periods: 1960-1992 (previous atlas) and 2000-2016 (current atlas).

## Background
- Produced by the Mammal Society with Sea Watch Foundation, UK Centre for Ecology and Hydrology, and others.
- Originated from the Mammal Watch South East (MaWSE) project and the Mammal Tracker app; expanded to the UK, Isle of Man, and Channel Islands.
- Cetacean data are included in the atlas but not integrated into this dataset; related publications include population status reviews and red lists.

## Data collection and validation
- Data drawn from diverse sources: National Biodiversity Network (NBN) gateway, local biological records centers, monitoring schemes, Natural England, Mammal Society, Biological Records Centre, Sea Watch Foundation, iRecord, and the Mammal Tracker app.
- Quality varies by source; majority are opportunistic citizen science records, with some structured and professional surveys.
- Validation:
  - iRecord and Mammal Tracker data validated by Mammal Society verifiers.
  - External data often had prior validation; new record-level validation is limited unless highlighted as questionable.
  - To minimise misidentifications, only records for widespread species (mole, rabbit, badger, fox, hedgehog) from certain datasets were included in high-risk categories.
  - Expert review of 10km squares; records in highlighted squares validated at the record level before inclusion or exclusion from maps.

## Cetaceans
- Cetacean data are not included in this dataset; atlas accounts and maps for cetaceans were produced separately by Sea Watch Foundation. For cetacean queries, contact Sea Watch Foundation.

## Dataset structure
- Format: CSV file with per-species 10km grid squares and coordinates, plus a GeoPackage (GPkg) with polygon boundaries for GIS analyses.
- CSV fields (per row):
  - SPECIES, COMMON_NAME
  - GRIDREF
  - CATEGORY (1990s only, 2000s only, or both)
  - TP_1960_1992, TP_2000_2016 (logical indicators of observations in each period)
  - LATITUDE, LONGITUDE (centre of 10km grid square, WGS84)
  - ENG, SCO, WAL, N_IRE, CD (flags indicating country/region inclusion)
- CATEGORY values:
  - '1960-1992' (observed only in previous atlas)
  - '2000-2016' (observed only in current atlas)
  - '1960-1992 & 2000-2016' (observed in both periods)
- Geopackage:
  - Each species as a separate layer; coordinates in OSGB 36 (EPSG: 27700).
  - Channel Islands and NI data re-projected to British Grid for consistency.
  - Attributes mirror the CSV fields.

## Data coverage and notes
- Geographic scope includes terrestrial mammal 10km squares across Great Britain and Northern Ireland; coastal/marine squares included and assigned to the closest country.
- Cetacean data are not part of this dataset.
- Data suitable for GIS analyses and examination of temporal changes between the two atlas periods.

## References
- Arnold (1993); Hayhow et al. (2019); Mathews et al. (2018); Mathews & Harrower (2020).