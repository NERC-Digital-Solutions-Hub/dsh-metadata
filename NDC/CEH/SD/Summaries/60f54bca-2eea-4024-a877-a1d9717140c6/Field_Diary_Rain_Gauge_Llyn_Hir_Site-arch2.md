# LLYN HIR RAIN GAUGE READ ME DOCUMENT

## Overview
- A concise log of the Llyn Hir rainfall measurement setup and issues from installation through 2009, focusing on equipment behavior, timing, and data integrity.

## Chronology of Observations
- 28/09/07: Storage and tipping bucket rain gauges installed.
- 29/11/07: Wind gust caused the tipping bucket to tip once; base of storage gauge found to be full of water.
- 30/05/08: Accidental tips of the tipping bucket (TB) rain gauge occurred; these tips should be ignored.
- 03/11/08: Time stamp issue suspected with overlap from the previous download; current time stamp assumed wrong and adjusted to follow immediately after the last record from the previous download.
- 27/01/09: Disparity >13% between TB and storage gauge readings; likely due to freezing conditions; ice present in one TB bucket and removed.
- 06/04/09: Time stamp issue suspected due to GMT to BST change; issue accounted for in the analysed data file.

## Data Quality Issues
- Environmental and equipment events (wind, ice) can affect readings and cause anomalies between TB and storage gauge.
- Time stamps have inconsistencies across downloads, requiring adjustments to maintain temporal continuity.
- Temporary data artifacts (e.g., water in storage gauge base, accidental TB tips) may need exclusion or flagging.

## Anomalies, Discrepancies, and Corrections
- Accidental TB tips: flagged as non-representative and ignored in analysis.
- TB vs storage gauge disparity: over 13% difference attributed to ice; ice removal documented.
- Time stamp adjustments: corrections made to align with actual timing; GMT/BST transitions considered and reflected in the analysed data file.

## Data Handling Guidance for Analysts
- Be aware of installation and operational context when processing rainfall data.
- Apply time stamp corrections consistently across downloads to maintain a continuous time series.
- Exclude or flag non-representative readings (e.g., accidental TB tips) and document any environmental factors (ice, wind) that may bias readings.
- Ensure analysed datasets account for recorded GMT to BST changes and any resulting time alignment issues.