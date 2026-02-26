# Dataset Description - ECN NO2 Diffusion Tubes

- Overview
  - ECN NO2 diffusion tube dataset collected by the ECN Data Centre (Centre for Ecology and Hydrology).
  - Data are collected under a standardized protocol to enable comparability across sites and over time.
  - Data users are asked to acknowledge ECN and provide one reprint of publications citing ECN data.

- Data provenance and governance
  - Dataset Owners: UK Environmental Change Network (ECN) programme, funded by a consortium of UK government departments and agencies.
  - Sponsors include multiple organisations (e.g., DEFRA, Natural England, NERC, SEPA, etc.).
  - ECN protocols ensure comparability across sites; accompanying PDF explains data collection methods.

- Data collection protocol
  - Passive diffusion tubes measure NO2 concentration over a two-week deployment period.
  - QA procedure includes deploying blank tubes alongside experimental tubes; blanks are analyzed in the lab same day.
  - Quality information accompanies the data for proper interpretation.

- Data structure and download fields
  - Primary download schema includes:
    - SITECODE: Unique ECN site code
    - SDATE: Sampling date
    - TUBEID: Tube identifier (E for experimental, B for blank)
    - FIELDNAME: Variable measured
    - VALUE: Measured value
  - Supporting file ECN_AN2.csv contains deployment details:
    - SITECODE, TUBEID, DEPDATE, DEPHOUR, DEPMINS
    - SDATE, SHOUR, SMINS
  - Supporting quality text file ECN_AN_qtext.csv provides context when quality codes (Q1–Q8) are insufficient.

- Site codes and locations
  - 12 ECN sites (T01 to T12) with site names and geographic coordinates (e.g., Drayton, Glensaugh, Hillsborough, Moor House, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon, Cairngorms).
  - Additional site information available in the ECN catalogue.

- Variables and quality codes
  - Field names:
    - WEIGHTNO2: Weight of NO2 on mesh (µg)
    - NO2: NO2 concentration (µg/m3)
    - NO2PPB: NO2 concentration (ppb)
    - TDIFF: Exposure time (minutes)
    - Q1–Q8: Quality codes (integers) indicating data quality factors
  - Quality codes (examples):
    - 100: No information available - data lost
    - 101–199: Various sampling/collection issues (e.g., no sample, partial loss, contamination)
    - 200–239, 501–513, 999: Adverse conditions, laboratory issues, or unusual events; 999 indicates an unusual event documented in quality text
  - Quality text: If a specific quality condition is not covered by codes, site managers add explanatory text (viewable in ECN_AN_qtext.csv).

- Usage notes and data integrity
  - Use accompanying quality information when analyzing and interpreting data.
  - The protocol ensures data comparability, but users should consult deployment details and quality text for context on any anomalies.

- Access, reuse, and attribution
  - Data are stored and uploaded to appropriate portals; ECN requests acknowledgement of data use and one reprint of any citing publications.
  - Emphasis on increasing dataset value through integration with other data sources and enabling access to underlying data for broader reuse.

- Practical implications for analysts
  - Standardized outputs (reports, maps, charts) can be produced to assess environmental health and policy performance over time.
  - Quality codes and deployment metadata are essential for robust interpretation and cross-site comparisons.
  - Consider correlating NO2 measurements with site-specific quality flags and deployment details to ensure reliable analyses.