# 10km occurrence data for terrestrial mammals in Great Britain and Northern Ireland, 1960-1992 & 2000-2016, as mapped in the 2020 Mammal Atlas

## Overview
- Provides summarized 10km grid square occurrence data for terrestrial mammals in Great Britain and Northern Ireland, covering recording periods 1960-1992 and 2000-2016, as mapped in the 2020 Mammal Atlas.
- Excludes cetaceans; cetacean data are produced separately by Sea Watch and not integrated into this dataset.
- Data are available as a CSV and as a Geopackage; both show the 10km squares where occurrences were recorded, with center coordinates and country membership.
- Intended for analysis and mapping of species distributions and changes between atlas periods.

## Background
- Atlas produced by the Mammal Society with assistance from Sea Watch, UK Centre for Ecology and Hydrology, Biological Records Centre, and others.
- Origin linked to the Mammal Watch South East (MaWSE) project and the Mammal Tracker app, later superseded by Mammal Mapper.
- Data collection expanded from South East England to the entire UK, Isle of Man, and Channel Islands; contributed to related publications and red lists.

## Data collection and validation
- Data sources include the National Biodiversity Network (NBN) gateway, local biological records centres, local and national monitoring schemes, Natural England, Mammal Society, Biological Records Centre, Sea Watch Foundation, and online tools (iRecord, Mammal Tracker).
- Mix of opportunistic (often citizen science) records and more structured surveys; some datasets are professional surveys.
- Validation:
  - Mammal Society verifiers validated data from iRecord and Mammal Tracker.
  - External datasets often had prior validation; details are not always provided, so validation level varies.
  - To minimize errors for less common species, some datasets with higher misidentification risk were filtered (e.g., only widely identifiable species included from certain datasets).
  - Expert review of 10km squares; any flagged squares were reviewed at the record level before inclusion in the final maps.
- Note: Cetacean data are not included in this dataset; mapping for cetaceans is managed separately by Sea Watch.

## Cetaceans
- Cetacean data are not integrated into this dataset and are handled directly by Sea Watch. For cetacean inquiries or recording, contact Sea Watch.

## Dataset structure and formats
- CSV file:
  - For each mammal species, lists 10km grid squares with observations during the recording periods (1960-1992 and/or 2000-2016).
  - Fields include:
    - SPECIES: scientific name
    - COMMON_NAME: common name
    - GRIDREF: 10km grid square reference (OGB for GB, OSI for NI, truncated MGRS for Channel Islands)
    - CATEGORY: time period category with values: '1960-1992', '1960-1992 & 2000-2016', '2000-2016'
    - TP_1960_1992: 1 if observed in 1960-1992, null otherwise
    - TP_2000_2016: 1 if observed in 2000-2016, null otherwise
    - LATITUDE: center latitude (WGS84)
    - LONGITUDE: center longitude (WGS84)
    - ENG / SCO / WAL / N_IRE / CD: boolean indicators for country/region inclusion (England, Scotland, Wales, Northern Ireland, Crown Dependencies)
- Geopackage (GPkg) file:
  - Provides the same data as separate layers per species, using OSGB 36 (EPSG: 27700) coordinates.
  - Includes 10km square boundaries as polygons; NI and Channel Islands squares are re-projected to the British National Grid for consistency; layer attributes match the CSV fields.
- Coverage notes:
  - Grid references include coastal/marine squares assigned to the closest country.
  - For NI, an OSI-based grid reference system is used in CSV; in GPkg, all layers are in British Grid.
  - Each species is represented in its own layer within the Geopackage.

## References
- Arnold, H. (1993). Atlas of mammals in Britain. HMSO.
- Hayhow, D.B. et al. (2019). The State of Nature 2019.
- Mathews, F. et al. (2018). A Review of the Population and Conservation Status of British Mammals.
- Mathews, F., & Harrower, C. (2020). IUCN-compliant Red List for Britain's Terrestrial Mammals.