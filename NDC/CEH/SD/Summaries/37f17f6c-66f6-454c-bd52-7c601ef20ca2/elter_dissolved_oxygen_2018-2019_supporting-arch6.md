# Elter_dissolved_oxygen_2018-2019.txt

## Overview
- Daily average dissolved oxygen concentration (DO_conc, μg/L) measured at Elterwater Inner basin's deepest point.
- Location: Lat 54.4287°, Long -3.0350°.
- Time period: May 2018 to December 2019.
- Depths: 3 m and 5 m from the surface.
- Sampling frequency: every 15 minutes.

## Measurement method and sensors
- Sensor: PME miniDOT oxygen sensors (Precision Measurement Engineering, USA).
- Method: fluorescence-based oxygen measurement.
- Sensor accuracy: 0.3 mg/L.
- Hardware: anti-fouling wipers to reduce biofilm on the sensor.

Note: Reported DO_conc units are μg/L, while the stated sensor accuracy is 0.3 mg/L.

## Data processing
- Raw data collected at 15-minute intervals; daily averages computed.
- Quality-controlled data with small gaps linearly interpolated (< 3 hours).

## Data structure
- Columns: Date (yyyy-mm-dd), Depth (m), DO_conc (μg/L).

## Usage and considerations
- Suitable for time-series analysis of dissolved oxygen by depth and over time.
- Enables exploration of temporal (diurnal/seasonal) and depth-related patterns.
- Interpolation for gaps may affect high-frequency analyses; consider the absence/presence of QC flags when interpreting results.

## Limitations and notes
- Only two depths (3 m and 5 m) are included.
- Interpolations are limited to gaps shorter than 3 hours.
- Additional calibration details beyond what is provided are not included.