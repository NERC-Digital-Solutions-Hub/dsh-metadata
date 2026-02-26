# UK Environmental Change Network (http://www.ecn.ac.uk) Rabbits and Deer (BU)

- Overview
  - Dataset from the UK Environmental Change Network (ECN) focusing on counts of deer, rabbits, grouse, and other indicators via transect-based dropping counts as an index of relative abundance.
  - Used to understand environmental change impacts on fauna; data are managed and disseminated by ECN with site-specific monitoring across multiple UK locations.
  - Data are stored in an Oracle database and come with accompanying metadata and quality information.

- Data Origin, Ownership and Access
  - Dataset Originator: ECN Data Centre (Centre for Ecology and Hydrology).
  - Dataset Owners: ECN programme sponsored by a consortium of UK government departments and agencies (including DEFRA, Natural England, Environment Agency, etc.).
  - Acknowledgement and use: ECN requests acknowledgement of data usage and requests one reprint of any publication citing ECN data.
  - Protocol Reference: Full methodology and measurement protocol available via ECN website.

- Methodology and Protocol
  - Dropping counts are recorded twice yearly (late March and late September) along transects.
  - Direct population size cannot be measured; relative abundance is estimated via the dropping-count index.
  - Moor House method used for Grouse as a cross-check reference.
  - Data should be used with accompanying quality information; interpretation should consider potential data quality issues noted in the metadata.

- Data Structure and Metadata
  - Data are stored in three interrelated sets of tables for each site (nine sites total):
    - D1BU_xxx: Core survey data, including site, location, sampling date, transect identifiers, and count values.
    - D2BU_xxx: Survey metadata and transect details (e.g., cleardate, survey reference, transect specifics).
    - D3BU_xxx: Transect characteristics and habitat descriptions (e.g., transect length, habitat description).
  - Tables are organized by site code; core metadata and data structure documentation exist to support data interpretation and integration.
  - Metadata documentation should be consulted to understand field definitions, data types, required fields, and reference tables.

- Site Codes, Names, and Date Ranges
  - T01 – Drayton: Location 52°11'37.95"N 1°45'51.95"W; Date range in dataset 01-APR-1993 to 11-OCT-2006.
  - T03 – Hillsborough: Location 54°27'12.24"N 6° 4'41.26"W; Date range in dataset 07-JUN-1995 to 02-MAY-2012.
  - T04 – Moor House - Upper Teesdale: Location 54°41'42.15"N 2°23'16.26"W; Date range in dataset 14-MAY-1993 to 10-OCT-2012.
  - T05 – North Wyke: Location 50°46'54.96"N 3°55'4.10"W; Date range in dataset 23-MAR-1993 to 28-SEP-2012.
  - T06 – Rothamsted: Location 51°48'12.33"N 0°22'21.66"W; Date range in dataset 11-APR-1994 to 18-OCT-2010.
  - T07 – Sourhope: Location 55°29'23.47"N 2°12'43.32"W; Date range in dataset 12-MAY-1993 to 28-SEP-1993.
  - T08 – Wytham: Location 51°46'52.86"N 1°20'9.81"W; Date range in dataset 06-MAY-1993 to 01-OCT-2012.
  - T09 – Alice Holt: Location 51° 9'16.46"N 0°51'47.58"W; Date range in dataset 10-OCT-1994 to 10-NOV-2006.
  - T10 – Porton Down: Location 51° 7'37.83"N 1°38'23.46"W; Date range in dataset 22-APR-1994 to 17-APR-2012.
  - Site coding and geographic metadata are provided to support cross-site comparisons and longitudinal analysis.

- Field Names and Quality Metrics
  - Core measurement fields include counts by species:
    - D: deer droppings (count)
    - G: grouse droppings (count)
    - R: rabbit droppings (count)
    - S: sheep droppings (count)
  - Quality code fields (Q1–Q8) accompany counts to capture data quality codes; each Q field is followed by an integer value.
  - Quality Codes: ECN standard codes (e.g., 100–241) indicate data quality issues or conditions (e.g., no information, sample lost, equipment issues, presence of debris, non-standard sampling dates/times, etc.). A special code 999 denotes an unusual event with associated free-text quality notes.
  - The site managers assign applicable quality codes; detailed explanations for each code are provided in the attached quality metadata.

- Usage Guidance and Data Governance
  - The dataset is intended for monitoring framework applications—identifying environmental health measures, evaluating policy impact, and informing future decisions.
  - Consider data gaps, access constraints, and potential silos when integrating with broader monitoring frameworks.
  - Public sharing of underlying datasets is a factor to consider; ensure adherence to metadata and quality reporting requirements.
  - Data governance practices—data provenance, metadata completeness, and data quality indicators—are essential for robust use in policy scrutiny and decision-making.
  - Users should reference the ECN protocol and quality metadata when interpreting results and acknowledge data usage as requested.