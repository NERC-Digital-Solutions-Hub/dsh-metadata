# Hirrhos Uchaf tipping bucket and  storage rain gauge

## Data collection context
- T/B installed 07/11/06
- Storage gauge installed 0930 GMT 08/11/06

## Data quality issues and timestamps
- Feb/07: Data dodgy due to significant snow; wind-blown snow off rain gauge likely caused improper recording.
- 03/11/08: Time stamp issue with overlap from previous download; timestamps adjusted to follow on immediately after the last record from the previous download.
- 06/04/09: Time stamp issue possibly from GMT to BST change; accounted for in the analysed data file.
- May/09: Data only available from 26th to 27th; reason unknown.

## GIS implications
- Data reliability varies by period; consider flags or exclusions for unreliable intervals.
- Time alignment and DST adjustments require standardization (prefer UTC) for accurate temporal mapping.
- Notable data gaps (e.g., May/09) and gaps during Feb/07 snow events; affects hydrological analyses and trend detection.
- Installation dates help define the valid data window and context for map-based displays.

## Recommendations for GIS workflows
- Attach clear data quality metadata and provenance (including installation dates and timestamp notes).
- Standardize times to a common zone (UTC) and document DST handling.
- Flag periods with suspected issues; avoid using unreliable data for precise rainfall calculations without corrective steps.
- If needed, apply documented data-cleaning steps (timestamp corrections, gap masking) and note any interpolations or assumptions.