# ECN Breeding Birds Survey Dataset Documentation

## Overview
- Dataset Originator: ECN Data Centre (http://data.ecn.ac.uk), Centre for Ecology and Hydrology (ecn@ceh.ac.uk)
- Dataset Owners: UK Environmental Change Network (ECN) programme; funded by a consortium of UK government departments and agencies
- Purpose: Provide standardized Breeding Bird Survey data to understand environmental change; acknowledge data use and share one reprint of any publication citing ECN data
- Data compatibility: Standard operating procedures to ensure data comparability across sites; data may be combined with other monitoring programs to mitigate limitations

## Data Collection Protocol
- Methodology: Based on the Breeding Birds Survey (BTO); site transects within 1 km square; distance from transect recorded
- Sampling: Transect walked twice per year (early and late visits)
- Scope: National-scale survey; site-based data have limited detail on precise population-environment relationships
- References: Earlier protocols (Common Bird Census, Moorland Bird Survey) superseded by Breeding Bird Survey at ECN sites
- Quality: Use accompanying quality information to assess data suitability

## Dataset Structure and Files
- Core data fields (ECN_BB dataset):
  - SITECODE: Unique ECN site code
  - LCODE: Location ID (unique with site)
  - VISIT: Visit type (E = early, L = late)
  - SDATE: Sampling date
  - TRANSECT: Transect identifier
  - FIELDNAME: Bird species code
  - VALUE: Number of birds observed
  - DISTANCE: Distance category (1 = within 25 m, 2 = 25–100 m, 3 = >100 m)
  - F: Bird in flight (any distance)
- Supporting Documentation:
  - ECN_BB2.csv: Survey timing and Weather/Conditions (FROM_HOUR, FROM_MINS, TO_HOUR, TO_MINS, CLOUD, RAIN, WIND, VISIBILITY)
  - ECN_BB3.csv: Habitat context for transects (FIRSTHL1–FIRSTHL4A/B, SECONDHL1–SECONDHL4B; multiple habitat level codes)
  - ECN_BB_qtext.csv: Qualitative notes attached by site managers (SITECODE, FIELDNAME, FROM_DATE, TO_DATE, DATATYPE, CONTINUING)
- Explanatory Information:
  - Site codes: List of sites (e.g., T01 Drayton, T02 Glensaugh, T03 Hillsborough, etc.) with coordinates
  - Bird species codes: Mapping of two-letter/species codes to common and scientific names
  - Habitat codes: BTO habitat coding system (Levels 1–4) with examples (A: WOODLAND; B: SCRUBLAND; C: Semi-natural Grassland/Marsh; D: Heathland/Bogs; E: Farmland; F: Human Sites; G: Water Bodies; H: Coastal; I: Inland Rock; J: Miscellaneous)

## Site, Species, and Habitat Metadata
- Site codes and locations: T01–T12 with site names and latitude/longitude
- Bird species codes and names: Comprehensive mapping for species observed in survey data
- Habitat codes:
  - Level 1 codes: A–J (main habitat types)
  - Level 2–4 codes: Detailed subcategories describing habitat structure and disturbance (e.g., woodland types, scrubland, grassland, farmland, water bodies, coastal, etc.)
  - Each level includes descriptive codes for vegetation structure, disturbance, boundary features, and management

## Usage, Citations and Acknowledgments
- Acknowledge ECN data usage in publications
- Provide ECN with one reprint of any publication citing ECN data
- Recommend combining ECN data with broader monitoring datasets (e.g., BTO) to mitigate limitations on linking population data to environmental change
- Use accompanying quality information (ECN_BB_qtext.csv) to understand data quality nuances
- Data are intended to enable self-serve exploration through standardized formats and by providing clear field definitions and codes

## Access and Support
- Primary access: ECN Data Centre (URL provided above)
- Contact: ecn@ceh.ac.uk
- Additional documentation: Included ECN_BB2.csv, ECN_BB3.csv, ECN_BB_qtext.csv and site/species/habitat explanatory information

## Data Quality and Limitations
- Site-level data may not capture precise population-environment relationships; integration with broader datasets is advised
- Data quality is documented in accompanying quality text files; consult these for timing, weather, and site-specific caveats
- Standardized protocols promote comparability across sites, but patchy data across a wide range of sites and formats can pose challenges