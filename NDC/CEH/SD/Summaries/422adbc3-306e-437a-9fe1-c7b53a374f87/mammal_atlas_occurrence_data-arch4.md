# 10km occurrence data for terrestrial mammals in Great Britain and Northern Ireland, 1960-1992 & 2000-2016, as mapped in the 2020 Mammal Atlas

## Overview
- Provides summarised 10km grid-square occurrence data for terrestrial mammal species during 1960-1992 and/or 2000-2016, as mapped in the 2020 Mammal Atlas.
- Cetaceans are excluded from this dataset; cetacean data are handled separately by Sea Watch Foundation.
- Atlas developed by the Mammal Society with Sea Watch Foundation, UK Centre for Ecology and Hydrology, and other partners; rooted in the MaWSE project and Mammal Tracker (now Mammal Mapper).
- Supports publications, red lists, and national/regional conservation assessments; data collection has expanded UK-wide from regional origins.
- Data collection underpinning the atlas involved a mix of citizen science and structured surveys, with validation efforts at record and expert-review levels.

## Data collection and validation
- Sources include the National Biodiversity Network (NBN Atlas), local biological records centres, local/national monitoring schemes, Natural England, Mammal Society, Biological Records Centre, Sea Watch Foundation, iRecord, and Mammal Tracker.
- Most data are opportunistic volunteer records; some datasets are more structured (professional surveys or monitoring schemes).
- Validation:
  - iRecord and Mammal Tracker data verified by Mammal Society verifiers.
  - External datasets often pre-validated; detailed validation procedures not always documented.
  - Datasets from non-mammal-focused schemes may contain more dubious records; to mitigate, records for widely recognizable species from these datasets were included selectively.
  - 10km square occurrence maps reviewed by species experts; any squares flagged for review had records checked at the record level before inclusion.
- Cetacean data are not integrated into this dataset and were produced separately by Sea Watch.

## Dataset structure
- Each species is represented with 10km grid squares indicating occurrences during the current atlas period (2000-2016) and/or the previous atlas period (1960-1992).
- Fields in the CSV:
  - SPECIES, COMMON_NAME
  - GRIDREF (grid square reference; uses OGB for GB, OSI for NI, and truncated MGRS for Channel Islands)
  - CATEGORY (1960-1992, 1960-1992 & 2000-2016, 2000-2016)
  - TP_1960_1992 (1 if observed in 1960-1992; null otherwise)
  - TP_2000_2016 (1 if observed in 2000-2016; null otherwise)
  - LATITUDE, LONGITUDE (centre of 10km grid square, WGS84)
  - ENG, SCO, WAL, N_IRE (flags indicating country membership)
  - CD ( Crown Dependencies: Channel Islands or Isle of Man)
- Geopackage (gpkg) alternative:
  - 10km square boundaries as polygons for GIS analyses; CRS is OSGB 36 (EPSG: 27700); NI and Channel Islands squares re-projected to British Grid
  - Each species has a separate layer; attribute fields mirror the CSV
  - Coastal/marine squares assigned to the nearest country
- Data coverage:
  - Includes 10km squares across Great Britain and Northern Ireland; cetacean data excluded from this dataset

## Data formats and access
- Available as a CSV file detailing species, grid cells, and period-specific presence.
- Also available as a Geopackage (.gpkg) with polygon grid squares for GIS analyses.
- Grid references reflect three reference systems (OGB, OSI, truncated MGRS); Centre coordinates provided in latitude/longitude (WGS84).
- Data are structured to support reproducible mapping and spatial analyses of species distributions across the two atlas periods.

## Cetaceans
- Cetacean data are part of the overall Atlas but not included in this dataset.
- For cetacean data inquiries or recordings, contact Sea Watch Foundation.

## Limitations and quality considerations
- Data quality and validation vary by source due to the mix of citizen science and professional datasets.
- While many records are pre-validated, not all have uniform validation detail; some datasets may contain dubious records, particularly for less easily identified species.
- The expert review process mitigates some uncertainties by re-evaluating highlighted grid squares and records at the individual level.

## References
- Arnold, H. (1993). Atlas of mammals in Britain.
- Hayhow, D.B. et al. (2019). The State of Nature 2019.
- Mathews, F., Kubasiewicz, L. M., et al. (2018). A Review of the Population and Conservation Status of British Mammals.
- Mathews, F., & Harrower, C. (2020). IUCN - compliant Red List for Britain's Terrestrial Mammals.