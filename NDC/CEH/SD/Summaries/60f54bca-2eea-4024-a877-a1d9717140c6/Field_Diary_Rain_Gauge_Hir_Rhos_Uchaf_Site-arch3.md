# Hirrhos Uchaf tipping bucket and storage rain gauge

- Installation and equipment
  - Tipping bucket and storage rain gauge
  - Tipping bucket installed 07/11/06; storage gauge installed 08/11/06 at 09:30 GMT

- Data quality issues observed
  - Feb/07: Data considered dodgy because significant snow occurred; wind blew snow off the gauge, so precipitation may not have been recorded properly
  - 03/11/08: Time stamp issue with overlap between downloads; assumed timestamp was wrong and adjusted to follow immediately after the last record from the previous download
  - 06/04/09: Time stamp issue suspected due to shift from GMT to BST; issue accounted for in the analysed data file
  - May/09: Data coverage only from 26th to 27th May; reason not clear

- Data handling and adjustments
  - Time stamps were corrected or adjusted based on comparisons with prior records
  - Adjustments and assumptions were documented and reflected in the analysed data file

- End status and unknowns
  - Partial data presence in May/09; overall completeness and underlying causes for gaps remain unclear

- Relevance to monitoring-framework authors (implications)
  - Demonstrates common data quality risks: weather-related measurement interference, timestamp misalignment, and data gaps
  - Highlights need for robust metadata:
    - Clear recording of installation dates, sensor types, and maintenance
    - Documentation of data quality issues, corrections, and rationale
    - Time zone handling, including DST (GMT/BST) considerations
  - Underscores importance of data provenance and transparency for data corrections
  - Points to potential data governance requirements to manage data availability, access, and traceability across downloads and analyses