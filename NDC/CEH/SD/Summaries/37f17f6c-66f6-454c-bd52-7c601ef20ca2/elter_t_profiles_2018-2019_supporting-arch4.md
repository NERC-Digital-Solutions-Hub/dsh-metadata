# Elter_T_profiles_2018-2019.txt

- Overview
  - Hourly average water temperature profiles for Elterwater Inner basin's deepest point.
  - Time period: 2018-01-01 00:00:00 to 2019-12-31 23:00:00.
  - Depths: measurements at 1m, 2m, 3m, 4m, 5m, and 6m below the surface.

- Location and sampling context
  - Site coordinates: Lat 54.4287°, Long -3.0350°.
  - Data collected using RBRsoloT temperature sensors.
  - Raw data originally at 4-minute intervals; hourly averages provided.

- Data contents and structure
  - Columns: DateTime (yyyy-mm-dd HH:MM:SS), T_1m (°C), T_2m (°C), T_3m (°C), T_4m (°C), T_5m (°C), T_6m (°C).

- Data quality and processing
  - Sensor accuracy: ± 0.002 °C.
  - Some small gaps interpolated using linear interpolation for gaps less than 2 hours.

- Data governance and usage notes
  - Metadata includes location, depths, time range, and processing (hourly averaging; interpolation rules).
  - Data are suitable for vertical temperature profile analyses and time-series studies at the site.
  - Consider implications of hourly aggregation and any remaining gaps when analyzing high-frequency variability or processes requiring 4-minute resolution.