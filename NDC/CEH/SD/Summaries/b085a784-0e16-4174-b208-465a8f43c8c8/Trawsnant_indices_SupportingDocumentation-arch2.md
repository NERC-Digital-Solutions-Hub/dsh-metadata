# Experimental Design/Sampling Regime/Collection Methods

- Location and catchment context
  - Nant Trawsnant experimental catchment (LI8), near Llyn Brianne reservoir, Powys, Wales, UK.
  - Contributory area: 1.23 km2 for streamflow; 1.21 km2 for upstream pH monitoring.
  - Geology: Lower Palaeozoic shales, mudstones, greywackes, grits; soils dominated by Podzols and Histosols.
  - Land cover: about 88% conifer forest during the data period.
  - Additional catchment details are available in Jones and Chappell (2014) and Jones, Chappell and Tych (2014).

- Data sources and monitoring period
  - Streamflow and pH data from Lancaster University; regular 15-minute interval observations at stream gauging and water quality stations.
  - Timeframe: 1 January–31 December 2013; data recorded on a Campbell Scientific CR1000 data logger.
  - Rainfall data: monthly measures derived from 1 April 1982–1 April 2013 records from Welsh Water Authority/National Rivers Authority/Environment Agency Wales; gaps filled via correlations with nearby raingauges.
  - Temperature data: monthly values from Felindre weather station (Talgarth area), using Met Office MIDAS dataset.
  - North Atlantic Oscillation (NAO) index: monthly values from public CRU data source.
  - All data released via the Environmental Information Data Centre (EIDC) after IP rights vetting.

- Field instrumentation and calibration
  - Flow: water-level measurements from a trapezoidal flume deployed by Lancaster University; pressure sensing with a Sensortechnics CTWM82X5G4C3SUN transmitter; data logged by CR1000.
  - pH: measured with a Hach Lange pHD sc sensor and SC200 controller; logged by CR1000.
  - Calibration: salt-dilution gauging used to verify stage-discharge calibration; SC200 recalibrated every 2–3 months; pH sensor recalibrated with pH 4.0 and 7.0 solutions as needed.

- Data processing and modelling approach
  - Daily rainfall, streamflow, and pH models developed by linking observed daily rainfall to daily streamflow and pH using the CAPTAIN Toolbox for Matlab.
  - RIVC algorithm (Refined Instrumental Variable Continuous-time Box-Jenkins Identification) used to identify optimal model structures and parameters.
  - Models calibrated on 1 January–31 March 2013 and validated 1 April–31 December 2013.
  - Identified daily models applied to LSIM (Matlab) to generate simulated daily streamflow and pH for 1 April 1982–1 April 2013; monthly statistics then derived from these simulations.

- Analytical methods and software
  - Matlab (R2013) used for all modelling and statistics.
  - Statistical functions defined within the document include mean, median, percentiles (10th, 25th, 75th, 95th), moving-window min/max, sums, peaks, range, coefficient of variation, grow-season length, pulse counts and durations, and rates of rise/fall.
  - Thresholds for high/low pulses based on percentile cutoffs (75th for high, 25th for low).

- Nature and units of recorded values (data structure overview)
  - Dataset comprises a single CSV with 159 columns and 32 rows; columns 2–5 intentionally blank; rows 2–32 correspond to statistics for the first day of each month from 1 April 1982 to 1 April 2013.
  - Recorded variables include: rainfall metrics (mean, min/max, total, CV), flow metrics (mean, percentiles, moving-average extremes, total, and range), flow pulses (counts and durations above/below thresholds), flow rise/fall rates, mean and percentile pH, pH percentile and moving-average metrics, and a comprehensive set of temperature statistics (mean, percentiles, moving-average extrema, growth-season indicators, and pulse metrics).
  - Estimation windows vary by variable (e.g., 365 days for rainfall and flow metrics, 30–120 days for temperature and pH-related metrics).
  - Several fields are tied to specific analytical windows (e.g., 30 days prior to sampling for temperature, 365 days prior for rainfall/flow).

- Quality control and data integrity
  - Raw data from CR1000 loggers checked for erroneous values (often caused by power/battery interruptions).
  - Erroneous values replaced with NaN (not-a-number) in QA processes prior to time-series derivation.

- Data management and accessibility
  - Data are curated with IPR vetting by NERC EIDC and released in an online catalogue.
  - The dataset is designed to support reproducibility, with explicit methodological details and documented modelling steps to enable reuse and integration with other environmental datasets.