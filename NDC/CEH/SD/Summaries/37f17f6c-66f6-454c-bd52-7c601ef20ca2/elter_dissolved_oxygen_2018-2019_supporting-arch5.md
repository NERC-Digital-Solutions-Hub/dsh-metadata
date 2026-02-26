# Elter_dissolved_oxygen_2018-2019.txt

## Overview
- Daily average dissolved oxygen concentration (DO_conc, μg L-1) measured at Elterwater Inner basin's deepest point.
- Time period: May 2018 to December 2019.
- Measurements at depths of 3 m and 5 m from the surface, every 15 minutes.
- Sensor type: PME miniDOT oxygen sensors (Precision Measurement Engineering, USA) using fluorescence method.
- Sensor characteristics: accuracy stated as 0.3 mg L-1; equipped with anti-fouling wipers to reduce biofilm growth on the sensor.

## Data collection details
- Location coordinates: Lat 54.4287°, Long -3.0350°.
- Data capture cadence: 15-minute intervals; optical (fluorescence) DO measurement.
- Data ultimately provided as daily averages from raw 15-minute readings.

## Data processing and quality assurance
- Raw 15-minute data are averaged daily to produce daily DO_conc values.
- Some small gaps in the raw QCed data were linearly interpolated (less than 3 hours).
- Data structure includes: Date (YYYY-MM-DD), Depth (m), DO_conc (μg L-1).

## Data structure and metadata
- Fields: Date, Depth (m), DO_conc (μg L-1).
- Metadata captured includes spatial context (lake location), sampling depths, measurement method, sensor type, and processing steps (averaging, interpolation).

## Data quality considerations
- Units: DO_conc reported in μg L-1; sensor accuracy stated in mg L-1 (potential unit inconsistency to resolve).
- Interpolation applied only to small QCed data gaps (<3 hours); longer gaps may require caution in interpretation.
- Anti-fouling measures implemented to improve sensor reliability over time.

## Provenance and stewardship notes
- Data produced from standardized, repeatable measurements suitable for integration with other datasets.
- Clear documentation of method (fluorescence DO via miniDOT), depths, and temporal coverage supports reproducibility.
- Original raw 15-minute data exist alongside daily averages for traceability and reprocessing if needed.

## Access, sharing, and recommendations for users
- Data are prepared for sharing with accompanying metadata; ensure consistent units and documentation when integrating with other datasets.
- Recommend maintaining both raw (15-minute) and processed (daily-average) data to support various analyses and quality checks.
- Record any data gaps and interpolation assumptions in data dictionaries or usage notes.
- Consider providing data license and access details to facilitate discoverability and reuse.

## End-user guidance
- Suitable for limnology, aquatic ecology, and water quality assessments requiring temporal DO trends at multiple depths.
- Use with awareness of potential unit discrepancy and interpolation limitations for gaps.