# Experimental Design/Sampling Regime/Collection Methods

- Study location and scope
  - Data from the Nant Trawsnant experimental catchment (LI8) near Llyn Brianne reservoir, Powys, Wales, UK.
  - Contributory catchment areas: 1.23 km2 for streamflow gauge; 1.21 km2 for upstream pH station.
  - Geology: Lower Paleozoic shales, mudstones, greywackes, grits; soils dominated by Podzols and Histosols; ~88% forested by conifer during data periods.
  - References for catchment details: Jones and Chappell (2014); Jones, Chappell & Tych (2014).

- Data collection overview
  - Observations of streamflow and pH provided by Lancaster University from stream gauging and water quality stations.
  - Temporal resolution: 15-minute intervals for 2013 data; monthly statistics derived from daily rainfall, streamflow, and pH.
  - Data logging: Campbell Scientific CR1000 data loggers; streamflow via trapezoidal flume; pH via Hach Lange digital sensor.

- Rainfall, temperature, and auxiliary data
  - Monthly rainfall (1982–2013) derived in MATLAB; gaps filled by correlations with nearby raingauges (Llanerch YRFA, Swyddffynnon, Ystradffin).
  - Monthly temperature derived from Felindre weather station (Met Office MIDAS data).
  - NAO index (monthly) from public source (CRU data).
  - All Environmental Information Data Centre (EIDC) data vetted for Intellectual Property Rights (IPR) by NERC EIDC.

- Modelling and analysis methods
  - Daily rainfall, streamflow, and pH statistics derived by modelling daily rainfall and its impact on streamflow and pH.
  - Model identification: RIVC algorithm (Refined Instrumental Variable Continuous-time Box-Jenkins) via CAPTAIN Toolbox for Matlab (Taylor et al., 2007).
  - Model calibration/validation: daily models identified using 1 Jan–31 Mar 2013 data; validated 1 Apr–31 Dec 2013.
  - Application: identified models applied with LSIM in Matlab R2013 to simulate daily streamflow and pH for 1 Apr 1982–1 Apr 2013; monthly statistics derived from simulated data.

- Fieldwork and instrumentation details
  - Streamflow time series from water-level measurements in a custom flume; sensing with a Sensortechnics pressure transmitter; data logged by CR1000.
  - pH time series from a digital differential pH sensor (Hach Lange); controller and logging via CR1000.
  - Calibration: salt-dilution gauging for stage-discharge; SC200 controller recalibrated every 2–3 months; pH sensor recalibrated with pH 4.0 and 7.0 solutions as needed.

- Quality control and data integrity
  - QA procedures to identify erroneous values (e.g., due to short power failures) with replacement by NaN in concatenated time-series.
  - Data provenance and structure documented alongside IPR vetting.

- Data structure and accessibility
  - Data product: a single .csv spreadsheet with 159 columns and 32 rows.
  - Columns 2–5 intentionally blank; header in the first row; statistics for the first day of each month from 1 Apr 1982 to 1 Apr 2013.
  - Key variable categories (example of included metrics):
    - Rainfall metrics: mean, 10th percentile, total, maximum, coefficient of variation.
    - Flow metrics: mean, various percentiles, moving-average extremes, flow range, variability, pulse counts and durations (high/low thresholds based on est. percentiles), rise/fall rates, totals, maxima/minima.
    - pH metrics: mean, 10th percentile, and related statistics.
    - Temperature metrics: mean and percentile-based statistics; includes growth-season indicators and duration metrics.
  - Some later columns (e.g., 67, 142–159) capture additional statistics such as moving-average extremes, pH/rate metrics, temperature-related statistics, and growing-season indicators.
  - Data structure notes: time span covers 1982–2013 with monthly statistics; dataset intended for reproducibility and cross-month analyses.

- Provenance and references
  - Data release and governance via Environmental Information Data Centre (EIDC); IPR vetted by NERC EIDC.
  - Related methodological references: CAPTAIN Toolbox (Taylor et al., 2007); MATLAB implementations; Jones & Chappell (2014); Jones, Chappell & Tych (2014).