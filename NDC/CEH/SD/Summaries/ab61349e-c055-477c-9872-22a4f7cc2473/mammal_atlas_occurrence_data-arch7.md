# 10km occurrence data for terrestrial mammals in Great Britain and Northern Ireland, 1960-1992 & 2000-2016, as mapped in the 2020 Mammal Atlas

## Overview
- Provides summarized 10km resolution mammal occurrence data from the Atlas of Mammals of Great Britain and Northern Ireland (Crawley et al. 2020), excluding cetaceans from this dataset.
- Shows 10km grid squares where species were recorded during the current atlas period (2000-2016) and/or the previous atlas period (1960-1992).
- Describes data used to map distribution changes since the 1993 atlas and supports GIS-based visualisation and analysis.

## Data content and scope
- Includes all terrestrial mammal species in the atlas, with the exception of cetaceans (cetacean maps are provided separately by Sea Watch).
- Temporal coverage includes:
  - Most species: 1960-1992 and 2000-2016.
  - Exceptions with shorter periods: Water vole (2005-2016), Red squirrel (2010-2016), Grey squirrel (2010-2016).
- Grid data are provided for the UK, Isle of Man, Channel Islands; coastal/marine 10km squares included and assigned to the closest country.

## Data collection and validation
- Sources include: National Biodiversity Network (NBN) gateway, local biological records centres, monitoring schemes, Natural England, Mammal Society, Biological Records Centre, Sea Watch Foundation, iRecord, and Mammal Tracker.
- Data provenance and quality assurance vary by source; most records are opportunistic volunteer observations (citizen science) with some structured surveys and professional data.
- Validation:
  - Mammal Society verifiers validate records from iRecord and Mammal Tracker datasets.
  - External datasets often pre-validated; further record-level validation was limited to a subset of datasets.
  - To minimize errors for less common species, only records for widespread species unlikely to be misidentified were included from some datasets.
  - For each 10km square and time period, expert review of maps; squares flagged for review had their records re-examined at the record level to decide retention or exclusion.
- Cetacean data are not integrated into this dataset; Atlas Cetacean data are managed separately by Sea Watch.

## Cetaceans
- Cetacean species are included in the Atlas but not in this summarized dataset.
- Atlas cetacean data are maintained by Sea Watch; for cetacean queries, contact Sea Watch.

## Dataset structure and fields
- Two main formats:
  - CSV: per-species records with fields describing species, grid squares, time-period category, and geographic location.
  - Geopackage (.gpkg): polygonal 10km grid squares per species with identical attributes; all grids reprojected for GIS use.
- Key fields (CSV/Geopackage):
  - SPECIES: scientific name; COMMON_NAME: common name.
  - GRIDREF: 10km grid square reference (with regional variations explained below).
  - CATEGORY: time-period category ('1960-1992', '1960-1992 & 2000-2016', '2000-2016'), noting exceptions for three species with shorter recent periods.
  - TP_1960_1992 / TP_2000_2016: indicators (1=yes, missing/null=no) for presence in each period.
  - LATITUDE / LONGITUDE: center of 10km square (WGS84).
  - ENG / SCO / WAL / N_IRE / CI / ROI: flags indicating whether the square is in England, Scotland, Wales, Northern Ireland, Crown Dependencies (Channel Islands or Isle of Man), or Republic of Ireland.
- Grid reference specifics:
  - OSGB 36 (OSGB36, EPSG: 27700) for GB in geopackage.
  - Northern Ireland and Channel Islands use their respective CRS in CSV and are re-projected to British Grid in the geopackage (note rotation considerations for NI/CI squares).
  - GRIDREF conventions:
    - Scotland/England/Wales/Isle of Man use Ordnance Survey Great Britain system (OGB).
    - Northern Ireland uses Ordnance Survey Ireland (OSI).
    - Channel Islands use a truncated form of Military Grid Reference System (MGRS).
  - For truncated MGRS values, the initial 30U region is omitted; e.g., 30UWV64 appears as WV64..
- Spatial coverage:
  - Each row corresponds to a 10km square where a record was observed.
  - Coastal/marine squares are included and mapped to the closest country.

## Formats and coordinate reference systems
- CSV: tabular records with grid references and country flags; includes presence indicators per time period.
- Geopackage: layer-per-species with 10km square polygons; uses OSGB 36; NI and CI grids reprojected to British Grid.

## Temporal coverage and special cases
- Primary periods: 1960-1992 (previous atlas) and 2000-2016 (current atlas) for most species.
- Special cases with shorter recent periods:
  - Water vole: 2005-2016
  - Red squirrel: 2010-2016
  - Grey squirrel: 2010-2016
- CATEGORY and TP fields indicate whether a species was observed in each respective period.

## Spatial attribution and data interpretation
- Grids may cross country boundaries; country flags indicate the part of the grid that is within each country.
- Some squares may be assigned to multiple countries if they span boundaries; the dataset notes country membership per square.
- The dataset represents summarized mapping data derived from atlas records and expert review, suitable for GIS analyses of historical and contemporary mammal distributions.

## Uses for GIS specialists
- Map-based visualization of historical and current mammal distributions at 10km resolution.
- Multi-period analysis to identify range changes between 1960-1992 and 2000-2016.
- Integration with other biodiversity layers in GIS via CSV or GeoPackage formats.
- Spatial querying by country, region, or time period using the provided flag fields.

## References
- Arnold, H. (1993). Atlas of mammals in Britain.
- The State of Nature 2019 and related Mammal Society publications (Mathews et al., 2018; Mathews & Harrower, 2020).