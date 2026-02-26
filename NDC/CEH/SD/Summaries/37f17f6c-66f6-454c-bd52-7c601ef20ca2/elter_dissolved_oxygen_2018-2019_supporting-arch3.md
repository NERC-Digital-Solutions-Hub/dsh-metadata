# Elter_dissolved_oxygen_2018-2019.txt

## Overview
- Daily average dissolved oxygen concentration (DO_conc, μg L -1) collected at Elterwater Inner basin's deepest point (Lat: 54.4287°, Long: -3.0350°).
- Time period: May 2018 to December 2019.
- Measurements taken at 3 m and 5 m depths from the surface, every 15 minutes.
- Sensor technology: PME miniDOT oxygen sensors (Precision Measurement Engineering, USA) using a fluorescence method.
- Sensor features: accuracy stated as 0.3 mg L -1 and anti-fouling wipers to reduce biofilm growth on the optical sensor.
- Data processing: raw 15-minute measurements were daily averaged; small gaps in raw QCed data were linearly interpolated (< 3 hours).

## Data Structure
- Columns: Date (YYYY-MM-DD), Depth (m), DO_conc (μg L -1)

## Location and Time Span
- Location: Elterwater Inner basin, deepest point.
- Coordinates: Lat 54.4287°, Long -3.0350°.
- Time span: May 2018 – December 2019.

## Data Quality and Processing
- Data described as QCed.
- Short gaps in raw data were filled by linear interpolation (< 3 hours).
- Depth-specific measurements enable analysis of vertical dissolved oxygen profiles over time.

## Considerations for Monitoring Frameworks
- High-frequency (15-minute) data supports detection of short-term DO fluctuations.
- Depth-resolution (3 m and 5 m) allows vertical profiling and stratification assessment.
- Clear documentation of measurement method, sensor specifics, and processing (daily averaging, gap interpolation) aids reproducibility and governance.
- Potential caveats for framework use:
  - DO_conc unit is μg L -1, while sensor accuracy is stated in mg L -1, which may require unit alignment or clarification.
  - The description notes QCed data and interpolation but does not detail QC flags or metadata extensiveness beyond the listed fields.