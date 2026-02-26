# Elter_dissolved_oxygen_2018-2019.txt

## Overview
- Daily average dissolved oxygen concentration (DO_conc, μg L^-1) measured at the deepest point of Elterwater Inner basin.
- Location: Lat 54.4287°, Long -3.0350°.
- Timeframe: May 2018 to December 2019.
- Depths: measurements at 3 m and 5 m from the surface.
- Instrumentation: PME miniDOT oxygen sensors using a fluorescence method.
- Sensor accuracy: 0.3 mg L^-1; equipped with anti-fouling wipers to reduce biofilm growth.

## Data content and structure
- Data columns: Date (yyyy-mm-dd), Depth (m), DO_conc (μg L^-1).

## Sampling and processing details
- Raw data frequency: 15-minute intervals.
- Aggregation: raw 15-minute data daily averaged.
- Gaps: small gaps in QCed data linearly interpolated if < 3 hours.

## Data quality and considerations
- Potential unit discrepancy: DO_conc reported in μg L^-1, while sensor accuracy is stated as 0.3 mg L^-1.
- Interpolation of gaps may affect short-term variability interpretation.
- Spatial scope: single measurement point; no additional spatial coverage beyond the deepest point.

## GIS applicability and usage notes
- Suitable for time-enabled point visualization and depth-related analyses at a single site.
- Can be integrated with other hydrological or ecological layers for spatial-temporal studies.
- Useful for trend detection and quality assessment of aquatic oxygen dynamics at the deepest basin point.

## Data context and metadata considerations
- Precise location coordinates provided; no CRS specified—will require standard GIS handling (e.g., WGS84) for mapping.
- Temporal coverage explicit; ensure time zone alignment if integrating with other time-stamped data.