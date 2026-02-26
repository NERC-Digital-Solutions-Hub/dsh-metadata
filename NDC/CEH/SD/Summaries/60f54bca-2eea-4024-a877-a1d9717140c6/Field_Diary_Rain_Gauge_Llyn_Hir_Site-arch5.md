# LLYN HIR RAIN GAUGE READ ME DOCUMENT

## Overview
- Documentation accompanying the Llyn Hir rain gauge dataset, detailing installation, operational notes, data quality issues, anomalies, and corrections applied to the data.

## Data and Equipment
- 28/09/07: Storage and tipping bucket rain gauges installed.
- 29/11/07, around 10:55: wind gust caused tipping bucket to tip once; base of storage gauge found full of water.
- 30/05/08: accidental tips of tipping bucket rain gauge occurred; advise to ignore these events.
- 03/11/08: time stamp issue suspected; assumes time stamp is wrong and adjusted to follow immediately after the last record from the previous download.
- 27/01/09: disparity between tipping bucket (TB) and storage gauge >13%; likely due to freezing conditions; ice present in TB bucket and subsequently removed.
- 06/04/09: time stamp issue possibly due to GMT to BST change; this adjustment is accounted for in the analysed data file.

## Data Quality and Processing
- Time stamp issues have required adjustments to ensure continuity with prior downloads.
- Discrepancies between TB and storage gauge readings have been attributed to weather-related effects (e.g., freezing) and corrected for in analysis.
- Some corrections and notes are incorporated into the analysed data file rather than raw records.

## Implications for Data Users
- Users should be aware of potential timing discrepancies, weather-induced anomalies, and occasional non-representative TB events.
- Data interpretation should reference the analysed data file where corrections and adjustments are documented.

## Recommendations for Data Stewards
- Maintain clear metadata on installation events, incidents, time stamp adjustments, and weather impacts.
- Document and link any data corrections to the analysed dataset to ensure reproducibility.
- Implement checks for DST transitions (GMT/BST), cross-gauge (TB vs storage) consistency, and missing or anomalous timestamps.
- Ensure updates to datasets include notes about corrections and the rationale behind them.