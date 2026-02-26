# Dataset Originator E CN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

- Overview
  - The ECN (Environmental Change Network) dataset is produced by the ECN Data Centre and supported by a consortium of UK government departments and agencies.
  - Purpose: support understanding of environmental change through site monitoring and network coordination; data are intended for researchers, policymakers, and other stakeholders needing comparable, site-based environmental data.
  - Acknowledgement: ECN asks users to acknowledge data use and to send one reprint of any publication that cites ECN data.

- Protocol and quality
  - ECN operates standard operating procedures to ensure data comparability across sites; see accompanying WD.pdf for data collection explanations.
  - Quality and metadata: usage notes emphasize using accompanying quality information when applying the data; specific quality flags are provided for certain sites and measurements (notably Moor House).

- Data structure and access
  - Data are provided as 15-minute summaries derived from 10-second logger sampling.
  - Data fields for download: SITECODE (site code), SDATE (date), SHOUR (hour), SMINS (minute), FIELDNAME (variable), VALUE (measured value).
  - Supporting quality documentation: ECN_WD_qtext.csv stores site-specific quality notes (SITECODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION).

- Explanatory information: site codes
  - T02 Glensaugh — coordinates: 56° 54' 33.36" N, 2° 33' 12.14" W
  - T04 Moor House - Upper Teesdale — coordinates: 54° 41' 42.15" N, 2° 23' 16.26" W
  - T07 Sourhope — coordinates: 55° 29' 23.47" N, 2° 12' 43.32" W
  - T08 Wytham — coordinates: 51° 46' 52.86" N, 1° 20' 9.81" W
  - T11 Y Wyddfa - Snowdon — coordinates: 53° 4' 28.38" N, 4° 2' 0.64" W
  - Further site information is available at the ECN catalogue page: https://catalogue.ceh.ac.uk/id/813712d4-d162-4edeaff8-cf1c337bdc27

- Explanatory information: variables and quality codes
  - FIELDNAME options:
    - STAGE: Stage height (units: meters)
    - DISCHARGE: Discharge (units: cumecs)
  - HYCODE_ST / HYCODE_DI: Hydrologic quality codes for stage and discharge
    - 0 = no problems
    - 3 = data suspect
    - 4 = data unchecked
  - WICODE_ST / WICODE_DI: Wiski (data system) codes for stage and discharge
    - Examples include 1 = good, within rating; 2 = estimated, within rating
  - These codes provide a structured means to assess data reliability alongside the primary values.

- Data usage and citation
  - When using ECN data, please acknowledge ECN and consider sending a reprint of any publication citing the data.
  - The dataset includes notes on data collection formats (WISKI and historical Hydrolog formats) and accompanying quality codes to aid correct interpretation.