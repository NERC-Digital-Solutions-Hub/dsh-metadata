# Elter_T_profiles_2018-2019.txt

- What it is: Hourly average water temperature at the deepest point of Elterwater Inner basin, recorded at depths of 1–6 meters, from 2018-01-01 00:00:00 to 2019-12-31 23:00:00.

- Location: Latitude 54.4287, Longitude -3.0350.

- Measurement details: 4-minute interval temperature measurements using RBRsoloT sensors, with an accuracy of ±0.002°C.

- Data processing: Raw 4-minute data are hourly averaged; small gaps (< 2 hours) are linearly interpolated.

- Data fields: DateTime (yyyy-mm-dd HH:MM:SS), T_1m (°C), T_2m (°C), T_3m (°C), T_4m (°C), T_5m (°C), T_6m (°C).

- Data quality considerations: High-resolution vertical temperature profiles are available, but there are gaps due to interpolation; ensure time alignment and check for any remaining missing values after processing.

- Potential uses: Analyze vertical temperature structure and its temporal evolution (diurnal/seasonal patterns), compare temperatures across depths, inform hydrological or ecological models of the basin.

- Data handling recommendations: Confirm time zone consistency, document interpolation details and any quality flags, maintain calibration metadata for the sensors, and consider creating depth-specific visualizations or dashboards for self-service exploration.