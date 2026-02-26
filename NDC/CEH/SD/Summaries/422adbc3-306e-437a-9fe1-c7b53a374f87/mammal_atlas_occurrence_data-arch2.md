# 10km occurrence data for terrestrial mammals in Great Britain and Northern Ireland, 1960-1992 & 2000-2016, as mapped in the 2020 Mammal Atlas

## Overview
- Provides summarised 10km resolution occurrence data for terrestrial mammals (excluding cetaceans) from the 2020 Mammal Atlas.
- Covers recording periods: 1960-1992 (previous atlas) and 2000-2016 (current atlas).
- Data are presented as grid squares where species were recorded, with geographic centroids and country assignments.
- The dataset supports monitoring environmental health and policy performance over time, with potential for integration with other data sources.

## Background to the Atlas
- Produced by the Mammal Society with assistance from Sea Watch Foundation, Biological Records Centre, UKCEH, and others.
- Originated with the Mammal Watch South East (MaWSE) project to boost public involvement and develop an online atlas; led to Mammal Tracker app (now Mammal Mapper).
- Expanded to the UK, Isle of Man, Channel Islands; cetacean data contributed by Sea Watch Foundation but not integrated into the atlas dataset.
- Contributed to related publications on population status and red lists, and to State of Nature 2019.

## Data collection and validation
- Data compiled from diverse sources: NBN Atlas, local biological records centres, monitoring schemes, Natural England, Mammal Society, Sea Watch Foundation, iRecord, and Mammal Tracker.
- Data are largely opportunistic volunteer records, with some structured surveys and professional surveys included.
- Validation/verification:
  - iRecord and Mammal Tracker data verified by Mammal Society verifiers.
  - External datasets assumed credible if prior validation details were not provided; some datasets with potential misidentifications were used cautiously.
  - Records in dubious squares or rare/difficult-to-identify species were limited or scrutinised.
  - 10km square maps reviewed by species experts; any flagged squares underwent record-level review before inclusion.
- Cetaceans are part of the atlas but not included in this dataset; separate enquiries should be directed to Sea Watch Foundation.

## Cetaceans
- Cetacean data are not included in this dataset; atlas accounts for cetaceans were produced separately by Sea Watch Foundation.

## Dataset structure
- Available as:
  - CSV file detailing 10km grid squares per species for the specified time periods.
  - Geopackage (.gpkg) with 10km grid boundaries as polygons for GIS analyses (OSGB 36 / EPSG: 27700).
- Grid squares assigned to closest country (England, Scotland, Wales, Northern Ireland) or Crown Dependencies (Channel Islands, Isle of Man) where applicable.

## Data fields (CSV)
- SPECIES: Scientific name.
- COMMON_NAME: Common name.
- GRIDREF: 10km grid square reference (OSGB for GB, OSI for NI, truncated MGRS for Channel Islands).
- CATEGORY: Time period category (1960-1992; 1960-1992 & 2000-2016; 2000-2016).
- TP_1960_1992: 1 if observed in 1960-1992 period; missing/null otherwise.
- TP_2000_2016: 1 if observed in 2000-2016 period; missing/null otherwise.
- LATITUDE: Centre latitude (WGS84) of the 10km square.
- LONGITUDE: Centre longitude (WGS84) of the 10km square.
- ENG: 1 if within England (otherwise null).
- SCO: 1 if within Scotland (otherwise null).
- WAL: 1 if within Wales (otherwise null).
- N_IRE: 1 if within Northern Ireland (otherwise null).
- CD: 1 if within Crown Dependencies (Channel Islands or Isle of Man) (otherwise null).

## Time periods covered
- 1960-1992: occurrences in the previous atlas period.
- 2000-2016: occurrences in the current atlas period.
- 1960-1992 & 2000-2016: occurrences in both periods.

## Geographic coverage
- Great Britain and Northern Ireland.
- Includes coastal/marine 10km squares assigned to the nearest country.
- Channel Islands and Isle of Man included in the dataset context; coordinates re-projected to GB grid for the Geopackage.

## Access and usage
- Formats suitable for analysis in GIS and data portals:
  - CSV with central coordinates and country indicators.
  - Geopackage with polygonal 10km grid cells per species.
- Each species is provided as a separate layer in the Geopackage.
- Coordinate systems:
  - CSV uses WGS84 latitude/longitude for square centers.
  - Geopackage uses OSGB 36 (EPSG: 27700) with re-projected NI and Channel Islands grids.

## Practical implications for analysts monitoring the environment
- Enables time-based comparisons of mammal distributions to assess environmental health and policy outcomes.
- Data quality and consistency checks across many sources support standardized outputs suitable for monitoring dashboards and reports.
- The dataset is designed to be extended and linked with other environmental datasets to increase value beyond single-use applications.
- Accessibility to underlying data is supported through the CSV and Geopackage formats, facilitating reproducible analysis.

## References
- Arnold, H. (1993). Atlas of mammals in Britain.
- Hayhow, D.B. et al. (2019). The State of Nature 2019.
- Mathews, F. et al. (2018). A Review of the Population and Conservation Status of British Mammals.
- Mathews, F., & Harrower, C. (2020). IUCN - compliant Red List for Britain's Terrestrial Mammals.