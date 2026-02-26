# Experimental Design/Sampling Regime/Collection Methods

- Overview
  - Data pertain to the Nant Trawsnant experimental catchment (LI8) near Llyn Brianne reservoir, Powys, Wales, UK.
  - Measurements include streamflow, pH, rainfall, temperature, and the NAO index; data cover 1982–2013 for rainfall/temperature and 2013 for streamflow/pH statistics, with the 15-minute observation interval for 2013 and derived daily/monthly statistics.
  - Data are drawn from multiple sources: Lancaster University for streamflow and pH; historic rainfall data from Welsh Water Authority, National Rivers Authority, Environment Agency Wales; Met Office MIDAS for temperature; NAO index from public source. IP rights have been vetted by NERC EIDC.

- Site, catchment, and hydrogeology
  - Contributory areas: 1.23 km2 (streamflow) and 1.21 km2 (pH).
  - Geology: shales, mudstones, greywackes, grits (Lower Palaeozoic); soils mainly Podzols and Histosols.
  - Land cover: around 88% conifer forest during the data periods.
  - Field sampling conducted at a gauged station with a specific flume setup for discharge measurements.

- Data collection and instrumentation
  - Streamflow: monitored at regular 15-minute intervals using a Campbell Scientific CR1000 data logger; stage/discharge measured with a Forth River Purification Board trapezoidal flume; sensors include a Sensortechnics pressure transmitter.
  - pH: measured with a Hach Lange pH sensor and SC200 controller; logged with the CR1000 data logger.
  - Calibration: salt-dilution gauging used for stage-discharge calibration; SC200 controller recalibrated every 2–3 months; pH sensor recalibrated with pH 4.0 and 7.0 solutions as needed.

- Data processing and modelling
  - Monthly streamflow and pH statistics were derived by modelling daily rainfall plus daily streamflow and pH (aggregated to daily intervals) for 2013.
  - Modelling method: RIVC algorithm within CAPTAIN Toolbox for Matlab; used to identify optimal model structures/parameters; daily models validated from 1 April to 31 December 2013.
  - Extrapolation: identified model structures/parameters applied to LSIM in Matlab to simulate daily streamflow and daily pH from 1 April 1982 to 1 April 2013; monthly statistics derived from these simulations.
  - Matlab-based statistics: several functions used to compute means, percentiles, moving window statistics, peaks, rates of rise/fall, growing-season metrics, and CVs.

- Data structure, metadata, and provenance
  - Data file: a single CSV with 159 columns (many blank placeholders) and 32 rows.
  - Each row corresponds to a statistic for the first day of each month from 1 April 1982 to 1 April 2013; header row describes variables.
  - Columns cover extensive statistics for rainfall, flow, pH, and temperature (means, percentiles, moving mins/maxes, totals, pulses—high/low, durations, rates of rise/fall, CVs, growing season indicators, and multiple estimation periods).
  - Estimation periods: the majority use a 365-day window prior to sampling; temperature-related metrics often use a 30-day window; some flow-related metrics reference shorter windows (e.g., 10-day moving averages) and select pulse/season thresholds (e.g., 75th/25th percentiles).
  - Units: provided alongside each variable (e.g., rainfall in mm, flow in m3/s, pH, temperature in °C).
  - Data quality control: CR1000 data checked for erroneous values (e.g., power-failure artefacts); erroneous entries replaced with NaN in QA processes.

- Intellectual property, access, and documentation
  - All data released via the Environmental Information Data Centre (EIDC) online catalogue and vetted for IP rights by NERC EIDC.
  - Documentation includes explicit variable definitions, estimation periods, and the Matlab code fragments used to calculate statistics, supporting reproducibility.

- Data stewardship considerations
  - Data integration across multiple sources and formats; standardization of metadata and units is essential for consistency.
  - Explanations of data gaps and infill methods (gaps in rainfall records filled using correlations with nearby raingauges) important for users to assess data completeness.
  - Reproducibility relies on the CAPTAIN/RIVC modelling workflow and provided Matlab code; appropriate versioning and access to toolboxes should be maintained.
  - Clear provenance and calibration/QA logs should be preserved alongside the dataset to support audits and reuse.