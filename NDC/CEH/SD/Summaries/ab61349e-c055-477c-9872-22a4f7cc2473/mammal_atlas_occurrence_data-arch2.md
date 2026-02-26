# 10km occurrence data for terrestrial mammals in Great Britain and Northern Ireland, 1960-1992 & 2000-2016, as mapped in the 2020 Mammal Atlas

## Overview
- Provides summarised 10km grid square occurrences for terrestrial mammal species in Great Britain and Northern Ireland from the atlas period 2000-2016 and the previous atlas period 1960-1992 (cetaceans excluded from this dataset).
- Supports monitoring of environmental health and policy performance by documenting species distribution changes over time.

## Background
- Atlas of Mammals of Great Britain and Northern Ireland (Crawley et al. 2020) updates the 1993 atlas and draws on a wide network of partners.
- Origin from the Mammal Watch South East (MaWSE) project; led to online recording via Mammal Tracker (now Mammal Mapper).

## Data collection and validation
- Data sources include: National Biodiversity Network (NBN) gateway, local biological records centres, monitoring schemes, Natural England, Mammal Society, Sea Watch Foundation, and online tools (iRecord, Mammal Tracker).
- Predominantly opportunistic volunteer records (citizen science), plus structured surveys and professional data.
- Validation approach:
  - External data often pre-validated; treated as credible unless stated otherwise.
  - Mammal Society verifiers validate data from iRecord and Mammal Tracker.
  - A subset from non-mammal-focused schemes flagged for potential misidentifications; for some hard-to-identify species, only records for widespread species are included to minimize errors.
  - Expert review of 10km maps; records in highlighted squares re-checked at the record level before inclusion.

## Cetaceans
- Cetacean data are part of the full atlas but are not included in this dataset; atlas cetacean data are provided by Sea Watch Foundation. Contact Sea Watch for cetacean-related inquiries.

## Dataset structure and formats
- Provided as:
  - CSV file detailing, per species and 10km grid square, occurrence status across time periods.
  - Geopackage (.gpkg) with 10km squares as GIS polygons; OSGB 36 CRS (27700), with re-projection for NI and Channel Islands to fit British Grid.
- CSV fields include:
  - SPECIES, COMMON_NAME, GRIDREF, CATEGORY (time period coverage), TP_1960_1992, TP_2000_2016, LATITUDE, LONGITUDE, ENG/SCO/WAL/N_IRE, Crown Dependencies (Channel Islands/Isle of Man), ROI indicators, etc.
  - Grid references use GB, NI, and Channel Islands systems; abbreviated grid refs reported where appropriate (e.g., 30UWV64 -> WV64..).
- Each species is a separate layer in the Geopackage; attribute fields align with the CSV schema.

## Time periods and species-specific adjustments
- Most species: 1960-1992 (previous atlas) and 2000-2016 (current atlas).
- Three species use shorter recent periods due to rapid range changes:
  - Water vole (Arvicola amphibius): 2005-2016
  - Red squirrel (Sciurus vulgaris): 2010-2016
  - Grey squirrel (Sciurus carolinensis): 2010-2016

## Geographic scope and data organization
- Covers 10km grid squares across Great Britain and Northern Ireland, including some coastal/marine squares assigned to the closest country.
- Includes country flags (ENG, SCO, WAL, N_IRE) and Crown Dependencies/ROI indicators for each square.

## Usage and context for environmental monitoring
- Enables standardized, repeatable mapping of mammal occurrences over time for policy scrutiny and environmental health assessments.
- Facilitates data integration with other datasets to enhance monitoring value beyond single-use applications.
- Data quality and interpretation should account for variable source validation, potential observer bias, and species-specific identification challenges.

## References
- Arnold, H. (1993). Atlas of mammals in Britain. HMSO.
- Hayhow, D.B. et al. (2019). The State of Nature 2019.
- Mathews, F. et al. (2018). A Review of the Population and Conservation Status of British Mammals.
- Mathews, F., & Harrower, C. (2020). IUCN-compliant Red List for Britain's Terrestrial Mammals.