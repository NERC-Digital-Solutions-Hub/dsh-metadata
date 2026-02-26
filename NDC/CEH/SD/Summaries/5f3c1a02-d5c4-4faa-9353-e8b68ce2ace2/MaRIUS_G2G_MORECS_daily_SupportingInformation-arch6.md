# Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain (1960 to 2015): observed driving data [MaRIUS-G2G-MORECS-daily]

- Overview
  - Provides Grid-to-Grid (G2G) model estimates of daily mean river flow for 260 NRFA gauging stations across Great Britain, covering 1960–2015.
  - Output variable: river flow (m3 s-1), daily mean from 09:00 to 09:00 the next day.
  - The dataset enables comparison between G2G estimates and observed gauged flows and supports drought/water scarcity research.

- Model and driving data
  - G2G is a national-scale, grid-based hydrological model operating on a 1 km x 1 km grid with 15-minute time steps.
  - Parameterised using land cover, soils, and other spatial data; accounts for urban/suburban land-cover effects on runoff.
  - Uses input time-series of precipitation and potential evapotranspiration (PE); no snow module used here (precipitation assumed as rain).
  - Outputs represent natural flows (i.e., limited by model structure, not calibrated per catchment); spin-up not included.

- Input data
  - Meteorological drivers:
    - Daily rainfall at 1 km resolution (CEH-GEAR).
    - Monthly PE data at 40 km resolution (MORECS).
  - PE values are distributed from 40 km to 1 km boxes and across the 15-minute model time-step.
  - Spatial data such as topography and soil configurations follow Bell et al. (2009) and related work.

- Data format and contents
  - Main file: G2G_MORECS_flow_1960_2015.csv
    - CSV with a single header line.
    - First column: date; subsequent columns: daily flows for each catchment (one per column).
    - Years available: 1960–2015.
    - Time reference: flows are mean values from 09:00 to 09:00 the following day.
  - Related station file: MaRIUS_NRFAStationInfo.csv
    - Details for the 260 NRFA gauging stations, including station ID, river name, location, G2G coordinates, catchment area, and any data issues.

- How to use and interpretation
  - The dataset provides natural-flow estimates suitable for benchmarking against observed NRFA gauges; best performance for catchments with natural flow regimes and accurate observed records.
  - G2G grid cell selection: the closest 1 km x 1 km cell to each NRFA gauge, with checks to ensure correct tributary attribution. Some small catchments may have catchment areas that differ from the NRFA record; all G2G catchment areas are within 8% of NRFA catchment areas.
  - Limitations to note:
    - Model focuses on natural flows; artificial abstractions/discharges are not represented.
    - Calibration is not performed at the catchment level; parameter values are nationally applicable.
    - Spin-up period is not included in the data.
    - Precipitation input uses rainfall-only assumption (no snow module); drought assessments may be affected by this simplification.

- Acknowledgements and references
  - Funded by the UK Natural Environment Research Council (MaRIUS project; NE/L010208/1) as part of the UK Drought and Water Scarcity programme.
  - Acknowledges contributions from researchers (e.g., Nuria Bachiller-Jareno, Matt Fry, Maliko Tanguy) and cites foundational related works (Bell et al., Hough & Jones, Keller et al., Monteith, Tanguy et al., Rudd et al.).