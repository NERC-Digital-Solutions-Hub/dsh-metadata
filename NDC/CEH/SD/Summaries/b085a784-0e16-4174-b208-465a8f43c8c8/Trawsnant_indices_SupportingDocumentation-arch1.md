# Experimental Design/Sampling Regime/Collection Methods

- Location and catchment context
  - Nant Trawsnant experimental catchment (LI8) near Llyn Brianne reservoir, Powys, Wales, UK.
  - Contributory area to streamflow gauging station: 1.23 km2; upstream pH monitoring contributory area: 1.21 km2.
  - Geology: Lower Palaeozoic shales, mudstones, greywackes, grits; soils: Podzols and Histosols.
  - Land cover: ~88% of the basin was conifer forest during the data periods.
  - Additional catchment details referenced in Jones and Chappell (2014).

- Data collection and monitoring
  - Streamflow and pH data collected by Lancaster University from stream gauging and water quality stations on Nant Trawsnant.
  - Measurements taken at 15-minute intervals in 2013; recorded on a Campbell Scientific CR1000 data logger.
  - Field instrumentation
    - Streamflow: Forth River Purification Board trapezoidal flume; Sensortechnics pressure transmitter; Campbell CR1000 data logger.
    - pH: Hach Lange pHD sc digital pH sensor; SC200 controller; Campbell CR1000 data logger.

- Calibration, quality control, and data integrity
  - Salt dilution gauging used to validate stage-discharge calibration for the Nant Trawsnant flume.
  - SC200 controller recalibrated every 2–3 months during continuous monitoring.
  - pH sensor recalibrated with fresh pH 4.0 and 7.0 buffers as needed.
  - Quality control: erroneous values (e.g., due to power/battery events) replaced with NaN; QA processes used to derive time-series.

- Ancillary data and data provenance
  - Rainfall: monthly measures from 1982–2013, derived from Welsh Water Authority, National Rivers Authority, and Environment Agency Wales data; gaps filled using correlations with nearby gauges (Llanerch, YRFA, Swyddffynnon, Ystradffin).
  - Temperature: monthly values from Felindre weather station; data sourced from the Met Office MIDAS dataset (station code 1243).
  - North Atlantic Oscillation (NAO) index: monthly values from public source (CRU data).
  - Data availability and rights: all data released via the Environmental Information Data Centre (EIDC) and vetted for Intellectual Property Rights (IPR) by NERC EIDC.

- Analytical framework and modeling
  - Core approach: model daily rainfall-to-streamflow and rainfall-to-pH relationships to generate monthly statistics.
  - Methodology: Refined Instrumental Variable Continuous-time Box-Jenkins Identification (RIVC) algorithm from CAPTAIN Toolbox for Matlab to identify optimal model structures/parameters; model calibration using observations from Jan 1–Mar 31, 2013; validation from Apr 1–Dec 31, 2013.
  - Long-horizon simulation: identified models applied to LSIM (Matlab) to simulate daily streamflow and daily pH for Apr 1, 1982–Apr 1, 2013; monthly statistics derived from simulated data.
  - Tools and code
    - Matlab R2013; CAPTAIN Toolbox (RIVC algorithm) for model identification.
    - Provided example Matlab code for statistical calculations (mean, median, percentiles, moving-window statistics, rise/fall rates, pulses, etc.) to reproduce reported statistics.

- Data structure and content
  - Output format: a single .csv spreadsheet with 159 columns of statistical variables; columns 2–5 intentionally blank.
  - Rows: 32 rows total; first row is the header; rows 2–32 correspond to a statistic for the first day of each month from 1 April 1982 to 1 April 2013 (monthly statistics).
  - Variable details: the dataset documents extensive statistics including rainfall (mean, percentiles, totals, CV), flow metrics (mean/percentiles, moving-window min/max, totals, ranges, CV), pulse counts/durations for high/low flow, rate-of-change metrics, and pH and temperature statistics (means, percentiles, moving-window min/max, climate-related metrics like growing season temperature). Estimation periods are typically 365 days prior to sampling; for temperature and pH, 30 days prior are used.
  - Notable columns include:
    - Rainfall metrics (columns 6–11, 14–16, etc.)
    - Flow statistics (columns 11–27, 21–24, 26–27, etc.)
    - Pulse statistics (columns 21–24)
    - pH statistics (column 27–28 and related)
    - Temperature-related statistics (columns 142–159 and related)
    - Specific growth-season and pulse-duration metrics (e.g., growing-season temperature, high/low pulse durations)

- Scope and limitations
  - Spatial scale: small basin (roughly 1–1.2 km2 contributory areas).
  - Temporal scope: high-resolution 2013 observations for model development/validation; extended daily simulations back to 1982 for long-horizon statistics.
  - Data completeness: rainfall data gaps addressed via infill correlations; long-term analyses rely on modeled rainfall-to-flow/pH relationships.
  - Metadata richness and reproducibility: dataset includes detailed methodological notes, calibration steps, and Matlab code fragments to reproduce statistics; data and metadata are organized for discoverability via EIDC.

- Practical relevance for analysis tasks
  - Enables investigation of rainfall–streamflow–pH dynamics and their responses to wet/dry conditions and flow pulses.
  - Supports examination of long-term trends and seasonal patterns using model-based daily data extended across decades.
  - Provides a documented pipeline for data cleaning, model identification, validation, and statistical derivation, useful for reproducible data-driven decision-making in hydrology and water quality studies.