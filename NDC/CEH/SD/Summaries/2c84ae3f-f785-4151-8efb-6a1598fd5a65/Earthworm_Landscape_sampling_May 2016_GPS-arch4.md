# GPS accuracy = 4m

## Summary
- The document records field GPS data used to assess accuracy, with an explicit GPS accuracy target of 4 meters. It notes that some samples (H, M) were collected where it was easiest to do so.
- Multiple waypoint groups are listed (LL A1, LL A2, LL B1, LL B2, HWA1, HWB, OV 7, WHA, WHB), each providing an initial coordinate and a sequence of subsequent coordinates at increasing distances.
- Distances are labeled with qualitative markers (H, M) and quantitative steps (2, 4, 8, 16, 32, 64), representing progressive points along a surveyed path.
- Coordinates are presented in various formats and contain inconsistencies and occasional gaps, suggesting raw, in-field data capture.

## Data structure and formats
- For each label (e.g., LL A1, LL A2, etc.), an initial latitude/longitude is given, followed by additional coordinates at increasing distances.
- Distance markers include H, M, and numeric steps (2, 4, 8, 16, 32, 64).
- Coordinate formats vary:
  - DMS-like with explicit degrees/minutes/seconds (e.g., N 54 21.312) and symbol-based longitudes (W001 30.840).
  - Mixed decimal/different spacings (e.g., N 54.21.317, W001 30.810).
- Some entries contain missing data or placeholders (e.g., longitude = .).

## Data quality, metadata, and gaps
- Inconsistent coordinate formatting within and across groups.
- Missing values in places (e.g., OV 7 longitude is shown as a dot; some entries appear truncated).
- No explicit metadata for datum/CRS, measurement instruments, timestamps, or data provenance beyond the 4m accuracy note.
- Potential duplication across groups and variability in data precision.

## Implications for Data Leaders
- Highlights need for standardized data collection and formatting to ensure usability across teams and partners.
- Emphasizes importance of comprehensive metadata, including coordinate reference system, datum, instrument used, date/time, and methodology.
- Demonstrates common field-data challenges: incomplete records, formatting inconsistencies, and need for validation.

## Recommendations
- Standardize coordinate representation to a single format (preferably decimal degrees in a common CRS such as WGS84).
- Document metadata thoroughly: datum/CRS, measurement method, instrument, operator, date/time, and data collection protocol.
- Implement data validation rules to catch missing or inconsistent values during or after collection.
- Centralize data storage with clear lineage, and include quality flags or confidence metrics.
- Create a data dictionary and ensure cross-group consistency to reduce duplication and facilitate wider sharing.

## Observations and endnotes
- The document appears to be raw GPS field data intended to illustrate accuracy testing; it lacks a narrative or comprehensive data dictionary, focusing instead on coordinate sequences and distance markers.