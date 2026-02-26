# LLYN HIR RAIN GAUGE READ ME DOCUMENT

## Purpose
- Log of installation status, events, and data quality notes for the Llyn Hir rain gauge system.

## Key events and components
- 1 storage gauge and 1 tipping bucket (TB) rain gauge installed.
- 29/11/07: wind blew tipping bucket once.
- 30/05/08: accidental tips of TB rain gauge; ignore these.
- 03/11/08: time stamp issue observed; timestamp adjusted to follow last record from previous download.
- 06/04/09: time stamp issue potentially due to GMT→BST change; accounted for in analysed data file.

## Data quality and timestamp issues
- Time stamps occasionally misaligned across downloads; adjustments are documented.
- DST/GMT transitions implicated in timestamp discrepancies; corrections implemented in analysis.

## Data discrepancies and causes
- 27/01/09: TB vs storage gauge disparity >13%, likely due to freezing conditions; ice present in TB bucket during that period and subsequently removed.

## Data cleaning and handling
- Accidental TB tips ignored.
- Time stamps adjusted and the corrected times reflected in the analysed data file.

## Metadata and data management implications for data leaders
- Must maintain consistent timestamp handling across downloads and DST changes.
- Document hardware-related issues (e.g., ice, wind) that affect readings.
- Clearly flag anomalies, corrections, and cleaning steps in metadata and analysed datasets.
- Be aware of potential data gaps or quality concerns arising from environmental factors and sensor calibration differences.