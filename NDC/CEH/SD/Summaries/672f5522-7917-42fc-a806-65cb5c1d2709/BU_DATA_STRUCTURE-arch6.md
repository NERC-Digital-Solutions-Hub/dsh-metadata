# UK Environmental Change Network (http://www.ecn.ac.uk) Rabbits and Deer (BU) Dataset

- Overview
  - Dataset from the UK Environmental Change Network (ECN) focused on counts of deer, rabbits, grouse, and other indicators as an index of relative abundance based on dropping counts.
  - Data originator: ECN Data Centre; dataset owners and programme sponsors include a consortium of UK government departments and agencies.
  - Usage acknowledgement: please acknowledge use of ECN data and send one reprint of any publication that cites the data.
  - Protocol reference: provided at the ECN measurements documentation.

- Data contents and notes
  - Dropping counts are recorded biannually (late March and late September) as an index of relative abundance because direct population sizes are not measurable.
  - At Moor House, the same approach is used for Grouse.
  - Use accompanying quality information when analyzing the data.

- Data structure and storage
  - Data are stored in an Oracle database across 9 sites, with three data tables per site:
    - D1BU_xxx: survey-related data
    - D2BU_xxx: droppings (counts) data
    - D3BU_xxx: transect (survey routes) data
  - Table naming convention: D1BU_xxx, D2BU_xxx, D3BU_xxx, where xxx is the site code (e.g., T01, T03, etc.).
  - Each site has 9 tables per type? In total there are 27 site-type tables (9 sites × 3 data types).
  - Core fields across tables include SITECODE, LCODE (location code), SDATE (sampling date), PLOTID (transect/plot), and VALUE (where applicable). Some tables include additional fields (e.g., CLEARDATE, SURVEY, LENGTH, HABDESC).

- Site codes and dataset coverage
  - T01 Drayton (52°11'37.95"N 1°45'51.95"W), 01-APR-1993 to 11-OCT-2006
  - T03 Hillsborough (54°27'12.24"N 6° 4'41.26"W), 07-JUN-1995 to 02-MAY-2012
  - T04 Moor House - Upper Teesdale (54°41'42.15"N 2°23'16.26"W), 14-MAY-1993 to 10-OCT-2012
  - T05 North Wyke (50°46'54.96"N 3°55'4.10"W), 23-MAR-1993 to 28-SEP-2012
  - T06 Rothamsted (51°48'12.33"N 0°22'21.66"W), 11-APR-1994 to 18-OCT-2010
  - T07 Sourhope (55°29'23.47"N 2°12'43.32"W), 12-MAY-1993 to 28-SEP-1993
  - T08 Wytham (51°46'52.86"N 1°20'9.81"W), 06-MAY-1993 to 01-OCT-2012
  - T09 Alice Holt (51° 9'16.46"N 0°51'47.58"W), 10-OCT-1994 to 10-NOV-2006
  - T10 Porton Down (51° 7'37.83"N 1°38'23.46"W), 22-APR-1994 to 17-APR-2012

- Field names and data meanings
  - D, G, R, S: counts of deer, grouse, rabbit, and sheep droppings, respectively
  - Q1–Q8: quality codes associated with data points (each has a code and a corresponding value)
  - Quality Codes: site managers assign a standard set of ECN quality codes to indicate data quality issues (e.g., data lost, sample not taken, partial loss, debris in funnel, weather effects, etc.). A code 999 may be used with accompanying text for unusual events.

- Quality codes reference (highlights)
  - 100–111: No information; sample loss; partial loss; sample issues
  - 113–139, 145–177, 181–191, 200–239: various debris, weather, processing, or field-related notes
  - 501–508, 509–513, 999: laboratory or data handling issues; unusual events
  - 999: unusual event with explanatory text in the accompanying quality information

- Metadata and data validation
  - Metadata tables (M_DESC, M_REFFIELD, etc.) provide description and reference for fields.
  - Users should utilize the accompanying quality information to assess data reliability and filtering.
  - Data are designed to be self-serve but may require integration of D1–D3 datasets to enable full analysis of trends across sites and time.

- How this supports data work
  - Provides a structured, multi-site dataset suitable for cross-site comparisons of relative abundance indices.
  - Facilitates data stitching across survey records (dates, transects, locations) to create time-series dashboards or summary reports.
  - Encourages data quality-aware analysis by leveraging the quality code fields to filter or annotate analyses.

- Access and collaboration
  - Dataset originator and data center contact: ECN Data Centre; data sharing and usage should acknowledge ECN and provide reprint copies where possible.
  - Protocol and measurement methods are documented in the ECN measurements references.