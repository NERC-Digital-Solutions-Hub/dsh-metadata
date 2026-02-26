# LLYN HIR RAIN GAUGE READ ME DOCUMENT

## Overview
- Readme log for Llyn Hir rain gauge data documenting instrument installation, events, and data quality issues.
- Covers two instrument types: storage gauge and tipping bucket (TB) rain gauge.
- Timeframe referenced: 2007–2009, with notes on timestamp adjustments and DST changes.

## Key events and notes
- 28/09/07: Storage and tipping bucket rain gauges installed.
- 29/11/07 (around 10:55): Wind gust caused tipping bucket to tip once; base of storage gauge found full of water.
- 30/05/08: Accidental TB tips occurred; these should be ignored (14:35 GMT).
- 03/11/08: Time stamp issue detected; assumed mismatch with previous download; adjusted to follow immediately after the last record of the prior download.
- 27/01/09: Disparity >13% between TB and storage gauge readings; likely due to frozen conditions; ice observed in TB bucket and removed.
- 06/04/09: Time stamp issue possibly from GMT to BST DST change; adjustments accounted for in the analysed data file.

## Data quality and quality control notes
- Timestamp inconsistencies across downloads require alignment and adjustments during analysis.
- Discrepancies between TB and storage gauge readings may arise from freezing conditions and icing of the TB bucket.
- Accidental TB tips must be ignored to avoid bias in rainfall totals.
- DST transitions (GMT/BST) can affect time stamps and require explicit handling in data processing.

## Implications for GIS data preparation
- When integrating TB and storage gauge data, ensure synchronized timestamps and well-documented DST corrections.
- Implement flags or metadata to mark anomalous readings (e.g., tips due to wind, iced buckets) and exclude or adjust as appropriate.
- Maintain a clear audit trail of all timestamp adjustments and anomaly handling for reproducibility.

## Recommendations for analysts
- Verify time zone and DST context for each data segment; adjust timestamps accordingly.
- Flag and review periods with >10–13% TB vs storage discrepancies; investigate weather effects or instrument issues.
- Document all data cleaning steps (ignored tips, timestamp fixes, DST adjustments) within metadata.
- Consider data gaps and potential biases introduced by freezing conditions when analyzing rainfall patterns.