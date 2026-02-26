# 10km occurrence data for terrestrial mammals in Great Britain and Northern Ireland, 1960-1992 & 2000-2016, as mapped in the 2020 Mammal Atlas

## Overview
- Provides summarized 10km grid square occurrences for all terrestrial mammal species in the 2020 Mammal Atlas, excluding cetaceans.
- Covers two atlas recording periods: 1960-1992 and 2000-2016 (with minor exceptions for a few species using shorter recent periods).
- Data structure supports analysis of species distributions across Great Britain, Northern Ireland, Isle of Man, and Channel Islands.

## Background to the Atlas
- Produced by the Mammal Society with Sea Watch Foundation, Biological Records Centre, UK CEH, and others.
- Evolved from the Mammal Watch South East (MaWSE) project to expand to the entire UK region.
- MaWSE led to the Mammal Tracker app; later superseded by the Mammal Mapper app.
- Atlas contributed to related publications on population status and red lists; cetacean data are provided separately by Sea Watch.

## Data collection and validation
- Sourced from a wide array of providers: National Biodiversity Network gateway (NBN Atlas), local biological records centres, monitoring schemes, Natural England, Mammal Society, Biological Records Centre, Sea Watch Foundation, iRecord, and Mammal Tracker.
- Predominantly opportunistic volunteer-collected records (citizen science), with some structured surveys and professional data.
- Validation:
  - iRecord and Mammal Tracker data validated by Mammal Society verifiers.
  - External datasets often pre-validated; detailed validation procedures not always documented.
  - To mitigate misidentifications in less common species, records from certain non-mammal-focused schemes were screened; only widely identifiable species (e.g., mole, rabbit, badger, fox, hedgehog) were included from those datasets.
  - Expert review of 10km squares by species specialists; flagged squares undergo record-level verification to confirm retention or exclusion before final maps.
- Cetaceans are included in the atlas but not in this dataset; inquiries should be directed to Sea Watch.

## Cetaceans
- Cetacean data are not integrated into the dataset described here; atlas accounts and maps for cetaceans are produced directly by Sea Watch.
- For cetacean data, contact Sea Watch via their website.

## Dataset Structure
- Each species’ data includes:
  - Species (scientific name) and COMMON_NAME.
  - GRIDREF describing the 10km grid square; multiple grid reference systems used (OGB for GB, OSI for NI, truncated MGRS for Channel Islands).
  - CATEGORY indicating the time period coverage for the grid square:
    - 1960-1992
    - 1960-1992 & 2000-2016
    - 2000-2016
  - TP_1960_1992 and TP_2000_2016 flags indicating presence in previous/current atlas periods.
  - LATITUDE and LONGITUDE for the grid square center (WGS84).
  - ENG, SCO, WAL, N_IRE, CI, ROI booleans indicating country/region associations (England, Scotland, Wales, Northern Ireland, Crown Dependencies, Republic of Ireland).
- Dataset available as a CSV file with the above fields and as a Geopackage (.gpkg) with identical attributes, where each species is a separate layer and grid squares are represented as polygons in OSGB 36 (EPSG: 27700).

## Formats and access
- CSV: tabular representation with per-grid-square occurrence data per species.
- Geopackage: GIS-friendly format with polygonal 10km squares; standardized CRS; suitable for GIS analyses.
- Grid squares covering coastal/marine areas are assigned to the nearest country; NI and Channel Islands data re-projected to the British Grid for consistency.

## References
- Arnold, H. (1993). Atlas of mammals in Britain.
- Hayhow, D.B. et al. (2019). The State of Nature 2019.
- Mathews, F. et al. (2018). A Review of the Population and Conservation Status of British Mammals.
- Mathews, F., & Harrower, C. (2020). IUCN-compliant Red List for Britain's Terrestrial Mammals.