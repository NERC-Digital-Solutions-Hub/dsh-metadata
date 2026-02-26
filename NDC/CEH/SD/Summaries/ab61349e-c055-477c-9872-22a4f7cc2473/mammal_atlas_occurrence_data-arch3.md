# 10km occurrence data for terrestrial mammals in Great Britain and Northern Ireland, 1960-1992 & 2000-2016, as mapped in the 2020 Mammal Atlas

## Overview
- Presents summarized 10km grid occurrence data for terrestrial mammals in Great Britain and Northern Ireland, covering recording periods 1960-1992 and 2000-2016 (with some species using shorter recent periods).
- Excludes cetaceans from the dataset (cetaceans are handled separately by Sea Watch Foundation).
- Aimed at documenting distribution and changes since the 1993 atlas to inform monitoring and policy decisions.

## What the dataset contains
- For each species and 10km grid square, records whether the species was observed in:
  - 1960-1992
  - 2000-2016
  - Both periods (where applicable)
- Includes derived fields such as grid square centre coordinates (latitude/longitude) and country attribution (England, Scotland, Wales, Northern Ireland, Crown Dependencies, Republic of Ireland).
- Provides grid references in multiple systems (OGB, OSI, truncated MGRS) and notes on country coverage for each square.
- Data are available as:
  - CSV file detailing species, grid squares, time-period category, TP flags, coordinates, and country flags.
  - Geopackage (.gpkg) with 10km squares as polygons and identical attribute fields.

## Data sources and collection
- Sourced from diverse streams:
  - National Biodiversity Network (NBN) gateway, local biological records centers, local and national monitoring schemes, Natural England, Mammal Society, Biological Records Centre, Sea Watch Foundation.
  - Online tools: iRecord and the Mammal Tracker app (replaced by Mammal Mapper for many users).
- Most data are opportunistic volunteer-collected records (citizen science), with some structured surveys and professional data.
- Cetacean data are not integrated into this dataset; atlas-level cetacean data were produced separately by Sea Watch.

## Data collection and validation
- External records often carry prior validation; explicit validation details are not always provided and may vary by source.
- Mammal Society verifiers validated records from iRecord and the Mammal Tracker app.
- Expert review of 10km squares identified for further investigation; problematic squares prompted record-level checks and decisions on inclusion in maps.
- To minimize errors, only records unlikely to be misidentified for less common species were included from some datasets; more common species had broader inclusion.

## Dataset structure and formats
- CSV fields include:
  - SPECIES, COMMON_NAME, GRIDREF, CATEGORY (time period coverage), TP_1960_1992, TP_2000_2016, LATITUDE, LONGITUDE, ENG/SCO/WAL/N_IRE, N_IRE/ROI flags, etc.
- Time-period category values:
  - "1960-1992" (previous atlas only)
  - "2000-2016" (current atlas only)
  - "1960-1992 & 2000-2016" (present in both periods)
  - Some species use shortened recent periods (e.g., Water vole 2005-2016; Red/Grey squirrels 2010-2016).
- Geopackage provides the same data as separate layers per species, with polygons for 10km squares using OSGB 36 (EPSG:27700); NI and CI squares re-projected to British Grid for consistency.
- Coastal/marine 10km squares are included and assigned to the closest country.

## Cetaceans
- Cetacean data appear in atlas species accounts but are not included in this dataset; interested parties should contact Sea Watch Foundation for cetacean data.

## Usage, access, and governance
- Dataset supports monitoring, trend analysis, and policy evaluation by providing standardized presence data across time periods and geographies.
- Linked to the Atlas of Mammals and related outputs (e.g., state of nature reports and national red lists).
- Data governance and openness: underlying data are shared with attention to data provenance; some data sources may have restricted metadata or validation details, reflecting the source heterogeneity.
- For further inquiries about cetacean data or specific datasets, contact the respective data custodian (e.g., Sea Watch Foundation).

## Limitations and caveats
- Varied data quality and validation procedures across sources; reliance on prior validations means some records may carry differing certainty levels.
- Predominantly opportunistic records; potential biases in spatial and temporal coverage due to citizen science and data availability.
- Some species have incomplete temporal coverage or use non-standard periods for the atlas.
- Validation intensity is higher for square-level mapping; individual record verification is selective.

## Provenance and references
- Atlas context: Crawley et al. 2020; builds on the 1993 atlas (Arnold 1993).
- Related publications: State of Nature 2019; reviews of British mammal populations and red lists (Mathews et al. 2018; Mathews & Harrower 2020).
- Data and project lineage trace back to MaWSE (Mammal Watch South East) and the development of public recording tools (Mammal Tracker; later Mammal Mapper).