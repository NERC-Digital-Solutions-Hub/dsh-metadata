# UK Environmental Change Network (http://www.ecn.ac.uk) Rabbits and Deer (BU)

## Overview
- Long-running ECN dataset on relative abundance of rabbits and deer, based on transect droppings counts collected twice yearly (late March and late September).
- Uses an index method (not direct counts) due to practical measurement limitations; a similar approach is used for grouse at Moor House.
- Data are managed within an ECN framework and require acknowledgement of data use and reporting of publications citing the dataset.
- Protocol and metadata accompany the dataset, including quality indicators to inform data suitability and use.

## Data Structure and Content
- Data stored in Oracle: three sets of tables per site:
  - D1BU_xxx: survey data (counts and related fields)
  - D2BU_xxx: droppings data (relative abundance estimates by transect)
  - D3BU_xxx: transect data (transect details and measurements)
- Common table fields across sets include:
  - SITECODE, LCODE, SDATE, PLOTID, FIELDNAME, VALUE
  - VALUE is numeric where applicable; other fields provide site, location, date, and transect context
- Field codes for counts:
  - D = deer droppings, G = grouse droppings, R = rabbit droppings, S = sheep droppings
  - Q1–Q8: quality code pairs (each with a quality code and an integer value)
- Core metadata mentions the broader metadata documentation for core structures and reference lookups (M_DESC, M_REFFIELD).

## Site Coverage and Dates
- Site codes and basic metadata:
  - T01: Drayton (52°11'37.95"N 1°45'51.95"W), 01-APR-1993 to 11-OCT-2006
  - T03: Hillsborough (54°27'12.24"N 6°4'41.26"W), 07-JUN-1995 to 02-MAY-2012
  - T04: Moor House - Upper Teesdale (54°41'42.15"N 2°23'16.26"W), 14-MAY-1993 to 10-OCT-2012
  - T05: North Wyke (50°46'54.96"N 3°55'4.10"W), 23-MAR-1993 to 28-SEP-2012
  - T06: Rothamsted (51°48'12.33"N 0°22'21.66"W), 11-APR-1994 to 18-OCT-2010
  - T07: Sourhope (55°29'23.47"N 2°12'43.32"W), 12-MAY-1993 to 28-SEP-1993
  - T08: Wytham (51°46'52.86"N 1°20'9.81"W), 06-MAY-1993 to 01-OCT-2012
  - T09: Alice Holt (51° 9'16.46"N 0°51'47.58"W), 10-OCT-1994 to 10-NOV-2006
  - T10: Porton Down (51° 7'37.83"N 1°38'23.46"W), 22-APR-1994 to 17-APR-2012
- The dataset comprises data from multiple sites over varied date ranges, with a consistent structure for cross-site analysis.

## Metadata, Quality and Protocol
- Protocol reference available for terrestrial measurements (link provided in dataset notes).
- Data notes emphasize:
  - Dropping counts are taken twice per year to estimate relative abundance.
  - No direct population size measurements; index-based estimates are used.
  - Quality information accompanies the data and should be consulted to assess suitability.
- Quality codes:
  - Standard ECN quality codes (100–111, 113–145, 160–177, 181–191, 200–241, 501–508, 999, etc.) describe issues affecting data quality (e.g., no information, partial loss, debris in funnel, sampling disturbances, lab issues).
  - If an unusual event occurs not covered by codes, a text explanation is attached (code 999 with accompanying quality text).
- A dedicated quality information component accompanies the dataset to aid interpretation and filtering.

## Access, Citation, and Governance
- Dataset owners: The UK Environmental Change Network (ECN) program, sponsored by a consortium of UK government departments and agencies.
- Acknowledgement requested for data use; request a reprint of any publication citing the dataset.
- Data originator and contact: ECN Data Centre; data coordination and usage details provided in the documentation.
- Protocol and metadata are provided to support proper data reuse, reproducibility, and proper attribution.

## Practical Considerations for Data Leaders
- Discoverability and governance:
  - Data are distributed across multiple site-specific tables (D1BU_xxx, D2BU_xxx, D3BU_xxx) within an Oracle database, requiring clear data stewardship and cataloging for discoverability.
  - Core metadata guidance and site-level metadata facilitate understanding of context, location, and time range.
- Data quality management:
  - Use the ECN standard quality codes to assess data suitability; pay attention to notes about unusual events (code 999) and lab/field-related quality flags (501–508, etc.).
  - The accompanying quality information is essential for robust analysis and decision-making.
- Data strategy implications:
  - Emphasizes the importance of documenting data collection protocols, site metadata, and data quality to enable multi-site analyses.
  - Highlights challenges common to data-led governance: scattered data sources, data gaps, variable data quality, and the need for consistent metadata standards and discoverability.
  - Encourages explicit attribution and sharing of publications to demonstrate dataset value and usage.