# 10km occurrence data for terrestrial mammals in Great Britain and Northern Ireland, 1960-1992 & 2000-2016, as mapped in the 2020 Mammal Atlas

## Overview and purpose
- Summarised 10km resolution occurrence data for terrestrial mammals across Great Britain and Northern Ireland, reflecting recording periods 1960-1992 and 2000-2016 as mapped in the 2020 Mammal Atlas.
- Excludes cetaceans; data support analysis of species distributions and changes since the 1993 atlas.
- Dataset provided to enable discovery, reuse, and high-level assessments of mammal distributions across the UK.

## Data provenance and governance
- Collected from diverse sources: National Biodiversity Network (NBN) gateway, local biological records centres, local and national monitoring schemes, Natural England, Mammal Society, Biological Records Centre, Sea Watch Foundation, and online tools (iRecord, Mammal Tracker).
- Primarily opportunistic volunteer (citizen science) records, with some structured surveys and professional data.
- Most external data had prior validation; record-level validation varied by source. Credibility assumed unless stated; some datasets flagged for potential issues (particularly less common or harder-to-identify species).
- Final 10km maps and records reviewed by species experts; records in highlighted squares re-examined to decide retention.

## Validation and quality assurance
- Mammal Society verifiers validated data from iRecord and Mammal Mapper submissions.
- Prior validation existed for many external datasets; additional record-level validation focused on flagged squares and records.
- To minimise errors, particularly for uncommon species, emphasis placed on widely distributed species from less reliable sources.

## Cetaceans
- Cetacean data were included in the Atlas but are not part of this downloadable dataset; cetacean maps and accounts are produced separately by Sea Watch Foundation. For cetacean inquiries, contact Sea Watch.

## Dataset structure and formats
- Provided as a CSV file detailing, for each species, the 10km grid squares with recorded occurrences during either atlas period (1960-1992, 2000-2016) or both.
- Fields include:
  - SPECIES (scientific name)
  - COMMON_NAME
  - GRIDREF (10km grid square reference; multiple reference systems used)
  - CATEGORY (temporal category: 1960-1992 only; 1960-1992 & 2000-2016; 2000-2016 only)
  - TP_1960_1992 (1 if observed in previous atlas period; null otherwise)
  - TP_2000_2016 (1 if observed in current atlas period; null otherwise)
  - LATITUDE, LONGITUDE (centre of 10km square, WGS84)
  - ENG, SCO, WAL, N_IRE, CD (country/territory flags)
- Grid reference systems:
  - OGB for Great Britain (Scotland, England, Wales, Isle of Man)
  - OSI for Northern Ireland
  - A truncated form of MGRS for Channel Islands
- Geopackage option:
  - Contains per-species layers, using OSGB 36 (EPSG: 27700) CRS
  - NI and Channel Islands squares re-projected to British Grid
  - Coastally assigned squares to nearest country
- Data interpretation:
  - CATEGORY values indicate presence in the respective time period(s); TP fields use 1 to indicate presence, null to indicate absence
  - Data include 10km squares with both land and coastal/marine areas

## Access, metadata, and reuse considerations
- Available as CSV and Geopackage (.gpkg) formats to support GIS analyses and integration with other datasets.
- Grid squares from diverse sources and coordinate systems are harmonised for downstream use, with notes on re-projection where applicable.
- Metadata reflects data provenance, validation status, and temporal coverage to inform data stewardship and reuse decisions.

## Limitations and caveats for governance
- Variation in validation levels across sources; potential for dubious records in less common species.
- Some datasets may have limited documentation of validation procedures, affecting traceability and confidence for certain records.
- Cetacean data are not included in this dataset; users seeking full atlas coverage should refer to Sea Watch outputs for cetaceans.
- Data primarily represent presence/absence at 10km resolution within atlas periods; may not capture finer-scale occupancy or detectability nuances.

## References
- Arnold, H. (1993). Atlas of mammals in Britain.
- Hayhow, D.B. et al. (2019). The State of Nature 2019.
- Mathews, F. et al. (2018, 2020). Mammal Society reports on British mammals and red lists.