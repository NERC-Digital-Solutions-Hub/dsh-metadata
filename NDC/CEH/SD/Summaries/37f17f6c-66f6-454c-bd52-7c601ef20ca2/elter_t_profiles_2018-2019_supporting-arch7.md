Elter_T_profiles_2018-2019.txt

- Overview
  - Hourly average water temperature (°C) at the deepest point of Elterwater Inner basin.
  - Depths measured: 1–6 m below the surface.
  - Time period: 2018-01-01 00:00:00 to 2019-12-31 23:00:00.
  - Data collected with RBRsoloT sensors; high accuracy (±0.002 °C).

- Spatial and Temporal Coverage
  - Location: Elterwater Inner basin deepest point.
  - Coordinates: Lat 54.4287, Lon -3.0350.
  - Temporal resolution: hourly average (originally 4-minutely).

- Data Schema
  - Columns: DateTime (yyyy-mm-dd HH:MM:SS), T_1m (°C), T_2m (°C), T_3m (°C), T_4m (°C), T_5m (°C), T_6m (°C).

- Data Quality and Processing
  - Raw data were 4-minutely; aggregated to hourly averages.
  - Small data gaps (< 2 hours) were linearly interpolated.
  - Sensors: RBRsoloT; accuracy ± 0.002 °C.

- GIS-Related Considerations
  - Suitable for time-enabled map visualisations and depth-resolved analyses at a single fixed site.
  - Can support 3D or multi-layer representations (depth vs. time) for thermal profiling.

- Practical Uses in GIS
  - Visualising vertical temperature structure across depths over time.
  - Integrating with hydrological or ecological models for the Elterwater basin.
  - Comparing temperature trends between depths or time periods.

- Limitations and caveats
  - Single spatial location; not a broad spatial coverage dataset.
  - Depth measurements limited to the deepest point; may not represent lateral variability.
  - Interpolated gaps introduce slight smoothing; consider data gaps during analysis.