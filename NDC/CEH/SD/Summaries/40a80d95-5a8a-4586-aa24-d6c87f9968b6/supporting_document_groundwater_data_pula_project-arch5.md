# A brief description/overview of the data being described

- Scope
  - PULA Groundwater data folder containing 25 CSV files with in situ groundwater measurements from the Gaborone catchment, Botswana, collected May 2017–June 2018.
  - Purpose: understand long-term groundwater response to the 2016–2017 floods and assess spatial variability in water level and basic physicochemical parameters.
  - Part of the NERC-funded PULA project assessing impacts of extreme rainfall and flooding on water quality across surface and groundwater bodies.

- Study area and collaborators
  - Groundwater measurements collected around the Gaborone Reservoir catchment (south-west Botswana).
  - Collaboration among the Botswana Department of Water Affairs, Botswana International University of Science and Technology, and the University of Aberdeen.

- Measurement regimes (two strategies)
  - Strategy 1 (near-monthly, 22 boreholes)
    - Parameters: groundwater level depth (GWD), pH, temperature (T), electrical conductivity (EC), total dissolved solids (TDS).
    - Temporal cadence: near-monthly campaigns; 149 measurement occasions across 41 days (11 campaigns), yielding 456 total measurements per parameter set (e.g., 75 GWD, 95 pH, 96 T, 95 EC, 95 TDS).
  - Strategy 2 (high temporal resolution, 3 boreholes)
    - Parameters: GWD, temperature, (and EC where available).
    - Temporal cadence: 5-minute time steps from 18/05/2017 to 09/06/2018; 861,816 measurements in total (324,353 GWD, 324,376 T, 213,087 EC).

- Instruments, calibration, and data processing
  - Strategy 1: manual in situ GWD with Hydrotechnik dipmeter; pH, T, EC, TDS with HANNA HI-98129 (portable tester) from pumped samples.
  - Strategy 2: automatic logging with Solinst Levelogger (GWD with Model 3001 LTC or LT; T; EC where available).
  - Barometric compensation applied to automatic data using a Barologger; depth corrections performed via linear interpolation using Strategy 1 measurements; 8 download events matched between strategies.
  - Calibration and units
    - GWD: Strategy 1 (m, 0.01 m resolution, factory calibration); Strategy 2 (m, 0.001 m, manual dipmeter calibration).
    - pH: factory calibration; resolution 0.01 pH units.
    - Temperature: Strategy 1 (°C, 0.1° resolution, factory); Strategy 2 (°C, 0.001°).
    - EC: Strategy 1 (µS/cm, 1 point automatic); Strategy 2 (µS/cm, 0.1 resolution, factory).
    - TDS: Strategy 1 (ppm, 1 ppm resolution, factory).
  - Data structure and naming
    - Strategy 1 files: PULA_GW_level_physicochem_***.csv with 7 columns: measurement date, time, GWD (m), pH, T (°C), EC (µS/cm), TDS (ppm).
    - Strategy 2 files: PULA_GW_timeseries_***.csv with 5 columns: measurement date, time (hh:mm:ss), GWD (m), T (°C), EC (µS/cm) when available.

- Quality control and data integrity
  - Data screened for obvious errors (manual entry mistakes, anomalous datalogger records); erroneous records removed.
  - Data primarily provided in CSV format; documentation includes instrument types, units, resolutions, and calibration notes (Table 2 details).

- Data gaps and limitations
  - Near-monthly Strategy 1 datasets are incomplete with gaps for certain months and parameters due to logistical and budget constraints, equipment failures, and human error.
  - Strategy 2 provides continuous 5-minute data for three boreholes but depends on 5-minute logging and barometric corrections; some variables may be missing in certain timestamps.

- Relevance to data stewardship
  - Clear provenance: multiple institutions, defined measurement regimes, and documented calibration and processing steps.
  - Standardized file naming and column structures facilitate discoverability and reuse.
  - Detailed metadata on instrumentation, units, calibration, and processing supports data governance, interoperability, and appropriate disclosure of data limitations for users.