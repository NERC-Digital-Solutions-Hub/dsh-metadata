# LLYN HIR RAIN GAUGE READ ME DOCUMENT

- Purpose: Provides operational notes and data quality considerations for the Llyn Hir rain gauge setup, including installation events, anomalies, and timestamp handling to inform data processing and analysis.

## Data and equipment described
- Two measurement devices:
  - Storage gauge
  - Tipping bucket (TB) rain gauge
- Key operational notes:
  - 28/09/07: Storage and TB gauges installed
  - 29/11/07: Wind caused a single TB tip
  - 30/05/08: Accidental TB tips; to be ignored
  - 03/11/08: Time stamp overlap with previous download; time adjusted to follow on from last record
  - 27/01/09: Disparity TB vs storage gauge >13%; ice in TB bucket suspected
  - 06/04/09: Time stamp issue likely due to GMT/BST change; accounted for in analysed data file
- Physical issue notes:
  - Base of storage gauge was full of water
  - Ice present in TB bucket during freezing conditions; ice removed

## Data quality issues and anomalies
- Time stamp problems:
  - Overlaps between downloads
  - GMT to BST transitions affecting time interpretation
- Measurement discrepancies:
  - TB vs storage gauge disparity (>13%), potentially due to freezing conditions and ice
- Data points to ignore or flag:
  - Accidental TB tips (to be ignored)
- Physical/maintenance notes impacting data:
  - Water in storage gauge base
  - Ice blockage in TB bucket during cold periods

## Data handling and adjustments
- Timestamp corrections:
  - Time stamps adjusted to align with the end of the previous download
  - DST (GMT/BST) changes accounted for in the analysed data file
- Anomaly handling:
  - Disparities and ice-related issues flagged as potential data quality concerns
  - Ice removal performed; impact to be considered in data interpretation
- Documentation intent:
  - Preserve provenance of adjustments and anomalies for transparent data analysis

## Practical takeaways for data support and product development
- Include clear provenance and anomaly flags in data products (time adjustments, DST changes, ice presence, accidental tips)
- Provide guidance on reconciling TB and storage gauge readings when building dashboards or reports
- Ensure data pipelines capture and expose maintenance events (water in gauge, ice removal) as metadata
- Create self-serve tools or reports that users can filter by anomaly type (time stamps, gauge disparities, tips ignored)

## Timeline highlights (key notes)
- 28/09/07: Installation complete
- 29/11/07: Wind-induced TB tip
- 30/05/08: Ignore accidental TB tips
- 03/11/08: Time stamp overlap; adjustment applied
- 27/01/09: TB vs storage disparity noted; ice suspected
- 06/04/09: GMT/BST DST shift; adjustments documented in analysis