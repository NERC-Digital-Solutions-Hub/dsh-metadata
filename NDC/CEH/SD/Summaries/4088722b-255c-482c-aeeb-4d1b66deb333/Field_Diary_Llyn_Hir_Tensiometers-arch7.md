# Llyn Hir tensiometes

## Overview
- A sequential log of events, adjustments, and maintenance related to tensiometer data collection at Llyn Hir during 2008–2009.
- Highlights data corrections, equipment issues, and changes to data collection cadence affecting time-series visualization.

## Data Quality and Processing Notes
- 16/10/08: Data downloaded; logger time read 14/10/08 00:17; dataset may require adjustment due to time mismatch.
- 25/11/08: Offset changed from -4.8 to 0 on the logger.
- 28/11/08: Original offset noted as -4.8 cm H2O; correction needed to +4.8 cm; data adjusted to reflect this.
- 29/04/09: Degassed tensios after download.
- 02/09/09: Sampling interval changed from 10 to 15 minutes to reduce site visits (monthly visits).

## Equipment and Maintenance
- 31/07/09: Could not get response from logger; batteries replaced but no response.
- 12/08/09: Logger stopped logging; reset and restarted.

## Data Anomalies and Gaps
- 03/07/09: Irregular blips occur at irregular times, leading to partial data loss; suspected logger issue.
- Data stops short around 26/08/09 rather than 02/09/09, indicating premature cessation of data collection during this period.

## Implications for GIS and Data Use
- Metadata critical for map-based analyses: time offsets, degassing steps, and offset corrections must accompany datasets.
- Time-series visualization requires clear documentation of sampling interval changes and any logger-induced gaps.
- Data quality flags and provenance are essential when integrating with other spatial datasets or performing temporal analyses.

## Recommendations for GIS Deployment
- Attach detailed metadata for all adjustments (dates, rationale, and impact on values).
- Record and expose data quality indicators (e.g., gaps, blips, logger issues) in GIS attributes.
- Maintain a maintenance log as part of the data product to preserve traceability.
- When merging with other datasets, align time stamps and coordinate with offset corrections to ensure spatial-temporal consistency.
- Consider strategies for gap handling or imputation, and document any assumptions.