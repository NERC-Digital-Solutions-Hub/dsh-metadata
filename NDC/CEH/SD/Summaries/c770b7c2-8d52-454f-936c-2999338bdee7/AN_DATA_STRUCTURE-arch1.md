# UK Environmental Change Network (http://www.ecn.ac.uk) Atmospheric Chemistry: Nitrogen Dioxide (AN)

- Purpose and scope
  - A dataset of NO2 measurements collected using passive diffusion tubes, deployed for two-week periods, across 12 ECN sites.
  - Data support understanding environmental change effects and are used for research and policy-relevant analyses.

- Data origin, ownership, and access
  - Dataset Originator: ECN Data Centre (Centre for Ecology and Hydrology).
  - Dataset Owners: ECN programme, sponsored by a consortium of UK government departments and agencies (multiple DEFRA-related bodies, Natural England, NERC, Scottish/Welsh counterparts, etc.).
  - Usage acknowledgement: Users should acknowledge ECN data and return one reprint of any citing publication.

- Sampling protocol and quality assurance
  - Measurement method: Passive diffusion tubes deployed for two weeks to measure NO2 concentrations.
  - Quality checks: Blank tubes are processed alongside experimental tubes to monitor contamination or loss.
  - Quality information: Use accompanying quality metadata when using the data; a dedicated quality text accompanies unusual events (code 999).

- Data structure and schema
  - Core storage: Oracle database with per-site tables.
  - Tables:
    - D1AN_xxx: Core metadata/structure for each site (xxx = site code).
    - D2AN_xxx: Sample collection and measurement data for each site.
  - Key fields (typical structure across tables):
    - SITECODE: Dataset identifier (integer).
    - SDATE: Sampling date (date).
    - TUBEID: Tube type (E = Experimental, B = Blank) (VARCHAR2(3)).
    - FIELDNAME: Measured field name (e.g., NO2, WEIGHTNO2, NO2PPB) (VARCHAR2(30)).
    - VALUE: Measured value (numeric, optional).
    - DEPDATE/DEPHOUR/SHOUR/SMINS: Deployment timing details for tubes (where applicable).
  - Measurements and units:
    - NO2: NO2 concentration (micrograms/m3).
    - NO2PPB: NO2 concentration (ppb).
    - WEIGHTNO2: Weight of NO2 on the mesh (micrograms).
    - TDIFF: Exposure time (minutes).
    - Q1–Q8: Quality codes (integers) describing data quality factors.
  - Metadata references: SITECODE references to M_DESC and M_REFFIELD for descriptions and field references.

- Site codes, locations, and date ranges
  - 12 ECN sites (T01–T12) with site names, geographic coordinates, and dataset date ranges:
    - T01 Drayton: 52°11'37.95"N 1°45'51.95"W; 20-JAN-1993 to 26-DEC-2012
    - T02 Glensaugh: 56°54'33.36"N 2°33'12.14"W; 12-MAY-1993 to 12-DEC-2012
    - T03 Hillsborough: 54°27'12.24"N 6°4'41.26"W; 02-FEB-1994 to 19-DEC-2012
    - T04 Moor House - Upper Teesdale: 54°41'42.15"N 2°23'16.26"W; 03-FEB-1993 to 24-DEC-2012
    - T05 North Wyke: 50°46'54.96"N 3°55'4.10"W; 21-JUL-1993 to 26-DEC-2012
    - T06 Rothamsted: 51°48'12.33"N 0°22'21.66"W; 03-FEB-1993 to 12-DEC-2012
    - T07 Sourhope: 55°29'23.47"N 2°12'43.32"W; 09-JUN-1993 to 26-DEC-2012
    - T08 Wytham: 51°46'52.86"N 1°20'9.81"W; 03-FEB-1993 to 19-DEC-2012
    - T09 Alice Holt: 51° 9'16.46"N 0°51'47.58"W; 11-MAY-1994 to 27-DEC-2012
    - T10 Porton Down: 51° 7'37.83"N 1°38'23.46"W; 06-JUL-1994 to 12-DEC-2012
    - T11 Y Wyddfa – Snowdon: 53° 4'28.38"N 4° 2'0.64"W; 26-MAR-1997 to 27-DEC-2012
    - T12 Cairngorms: 57° 6'58.84"N 3°49'46.98"W; 10-NOV-1999 to 12-DEC-2012

- Quality codes and interpretation
  - ECN quality codes (applied by site managers) indicate data quality factors or issues (codes 100–513, 999 for unusual events with text).
  - Examples include data loss (100), no sample/reading taken (101), partial loss (103), contamination or debris events (several 120s–170s), laboratory issues (501–513), and non-standard sampling (222–223).
  - A detailed quality text accompanies the dataset for codes flagged as 999.

- Practical considerations for analysts
  - Data integration may require joining per-site D1AN_xxx and D2AN_xxx tables and applying quality codes to filter or weight observations.
  - Standardized units and metadata facilitate cross-site comparisons, but attention to site-specific date ranges and deployment timing is essential.
  - The dataset emphasizes the importance of using accompanying quality metadata when interpreting NO2 measurements.

- Protocol reference and additional documentation
  - Protocol reference: http://www.ecn.ac.uk/measurements/terrestrial/an
  - Metadata and field definitions are linked to master reference tables (M_DESC, M_REFFIELD) within the Oracle schema.

- Data usage commitments
  - Acknowledgement of ECN data use and provision of a reprint of any publication citing ECN data.