# PULA Groundwater data folder

- Timeframe and location: May 2017 – June 2018, Gaborone catchment, Botswana
- Collaborating institutions: Botswana Department of Water Affairs, Botswana International University of Science and Technology, University of Aberdeen
- Purpose: Understand long-term groundwater response to the 2016–2017 floods, assess spatial variability in water level and basic physico-chemical parameters, and evaluate wider impacts of extreme rainfall on groundwater and surface water quality (NERC PULA project)

Data content and structure

- Total files: 25
- Strategy 1 (near-monthly, spatial mapping): 22 files
  - Parameters: groundwater level depth (GWD), pH, temperature (T), electrical conductivity (EC), total dissolved solids (TDS)
  - Temporal resolution: monthly or less
  - Boreholes: 22 across the catchment
  - Data organization: PULA_GW_level_physicochem_***.csv
  - Columns: date, time, GWD (m), pH, T (°C), EC (µS/cm), TDS (ppm)
- Strategy 2 (high-resolution, 5-minute timeseries): 3 files
  - Parameters: GWD, T, EC (where available)
  - Temporal resolution: 5-minute intervals
  - Boreholes: 3 with automatic dataloggers
  - Data organization: PULA_GW_timeseries_***.csv
  - Columns: date, time (hh:mm:ss), GWD (m), T (°C), EC (µS/cm) when available
- Coverage goals: spread across 22 boreholes (Strategy 1) and three boreholes with continuous monitoring (Strategy 2)
- Data availability notes: near-monthly data may have gaps due to logistical constraints; Strategy 2 data available for three boreholes but with some missing parameters

Experimental design and sampling regime

- Strategy 1: spatial mapping with 22 boreholes; broad hydrological/physico-chemical parameters; low temporal resolution
- Strategy 2: high temporal resolution at 3 boreholes; focused parameter set (GWD, T, EC)
- Campaigns: Strategy 1 collected 149 measurement occasions on 41 days across 11 sampling campaigns; total Strategy 1 measurements: 456 (GWD 75, pH 95, T 96, EC 95, TDS 95)
- Strategy 2: 5-minute timeseries from 18/05/2017 to 09/06/2018; total Strategy 2 measurements: 861,816 (GWD 324,353; T 324,376; EC 213,087)

Collection, transformation, and field instrumentation

- Strategy 1 instruments: Hydrotechnik dipmeter (GWD); HI-98129 portable tester (pH, T, EC, TDS)
- Strategy 2 instruments: Solinst Leveloggers (GWD, T, EC for LTC loggers; some LT loggers for GWD and T)
- Barometric correction: Barologger at Otse-ramotswa landfill BH2 used to calibrate freshwater head; barometric pressure subtracted and converted to freshwater meters
- Depth correction: linear interpolation between Strategy 1 measurement dates, used to adjust Strategy 2 depths
- Calibration status: GWD calibrated against manual depth measurements; other parameters calibrated per instrument factory settings
- Download schedule: eight occasions aligned with Strategy 1 rounds (dates provided)

Calibration, units, and quality control

- GWD units: meters; pH (unitless); Temperature: °C; EC: µS/cm; TDS: ppm
- GWD accuracy/resolution: Strategy 1 0.01 m; Strategy 2 0.001 m
- Calibration approach: factory calibration for field instruments; manual dipmeter used for Strategy 2 GWD reference
- Quality control: data screened for obvious errors (manual transcription mistakes, anomalous datalogger readings) and erroneous records removed

Data structure and documentation

- File formats: CSV for all data
- Strategy 1 files: PULA_GW_level_physicochem_***.csv
  - 7 columns: date, time, GWD (m), pH, T (°C), EC (µS/cm), TDS (ppm)
- Strategy 2 files: PULA_GW_timeseries_***.csv
  - 5 columns: date, time (hh:mm:ss), GWD (m), T (°C), EC (µS/cm) when available
- Borehole metadata: detailed in Table 1 (names, coordinates, measurement periods, borehole characteristics; includes automated vs. manual logging boreholes)

Notes and caveats

- Data gaps: incomplete months and parameters in near-monthly datasets due to logistics and equipment failures
- Spatial and temporal coverage reflects a compromise between practical accessibility and research objectives
- Data intended to support analysis of groundwater response to floods, spatial variability across the catchment, and evaluation of water quality changes linked to extreme rainfall events

Potential data applications (in line with data-support capabilities)

- Cleaned, joined time-series analyses comparing GWD, temperature, EC, and TDS across boreholes
- Temporal alignment of Strategy 1 and Strategy 2 data to study short-term flood-driven changes
- Visual dashboards or pivot-table style explorations for end users to self-serve groundwater dynamics by borehole and time period
- Cross-referencing groundwater measurements with flood events to assess hydrological responses and water quality implications
- Documentation of data quality and calibration procedures to support reproducibility and reuse in related hydrogeological studies