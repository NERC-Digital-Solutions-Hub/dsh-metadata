# Experimental Design/Sampling Regime/Collection Methods

- Study area: Nant Trawsnant experimental catchment (LI8) near Llyn Brianne reservoir, Powys, Wales, UK.
- Contributory catchment areas: 1.23 km² for streamflow gauging; 1.21 km² for upstream pH monitoring.
- Geology and soils: Lower Palaeozoic shales, mudstones, greywackes, and grits; Podzols and Histosols; ~88% forested with coniferous cover during data periods.
- Key data sources and period: Streamflow and pH data collected by Lancaster University from gauging and water quality stations; rainfall (monthly) and temperature (monthly) spanning 1982–2013; NAO index monthly values obtained from public sources.
- IP and data rights: All data released via the Environmental Information Data Centre (EIDC) and vetted for IP rights by NERC EIDC.

## Data Collection and Instrumentation

- Streamflow: Observations derived from stream gauging; 15-minute interval measurements in 2013 using a Campbell Scientific CR1000 data logger.
- pH: Observations from a Hach Lange pH sensor (sc Digital Differential pH sensor with SC200 controller) also logged by a Campbell Scientific CR1000.
- Field instrumentation: 
  - Flow: Forth River Purification Board trapezoidal flume; pressure transmitter (Sensortechnics CTWM82X5G4C3SUN) for water level.
  - pH: Digital pH sensor setup as above; installation by Lancaster University.
- Calibration: Salt dilution gauging for stage-discharge calibration; SC200 controller recalibrated every 2–3 months; pH sensor recalibrated with pH 4.0 and 7.0 buffers as needed.

## Calibration and Maintenance

- Regular recalibration of sensors (every 2–3 months for pH; calibration checks for the flume via salt dilution guidelines).
- Data quality checks conducted on CR1000 logger outputs to identify and address erroneous values, typically due to power/battery events.

## Variables and Data Units

- A comprehensive set of daily and monthly statistics includes rainfall, flow, and pH metrics, plus temperature and derived indicators. Examples:
  - Rainfall: mean, 10th percentile, total, maximum, coefficient of variation (period: 365 days before sampling).
  - Flow: mean, 10th/95th percentiles, moving-average extrema (10-day windows), total, maximum/minimum, range, coefficient of variation, high/low flow pulses, pulse durations, rise/fall rates.
  - pH: mean and 10th percentile (365-day estimation period).
  - Temperature: mean, 10th/95th percentiles, moving-average extrema, overall max/min, range, coefficient of variation, growing season indicators (30- or 5-degree C thresholds) and related pulse durations.
  - Growth and thresholds: growing season length (5 C threshold) and other period-based metrics.
- Units: rainfall (mm), flow (m3/s), pH (unitless scale), temperature (Celsius), with various derived statistics calculated over specified estimation periods.

## Analytical Methods and Modelling

- Approach: Monthly streamflow and pH statistics derived by modelling observed daily rainfall, then daily streamflow and daily pH, aggregated to daily intervals.
- Modelling toolchain:
  - RIVC algorithm (Refined Instrumental Variable Continuous-time Box-Jenkins Identification) from the CAPTAIN Toolbox for Matlab (for model identification and parameter estimation).
  - LSIM routine in Matlab R2013 to simulate daily streamflow and daily pH data.
- Modelling period:
  - Identification and validation using 2013 daily data (1 Jan–31 Dec 2013) and then extrapolation to 1 Apr 1982–1 Apr 2013 for monthly statistics.
- Matlab code: Includes functions for computing mean, median, percentiles, moving-window statistics, growth rates, pulse counts/durations, and other statistical measures; demonstrated data processing workflow and reproducibility details.

## Data Quality Control and Provenance

- Data QA: Raw data from CR1000 loggers checked for erroneous values (e.g., due to power/battery issues) and replaced with NaN; quality assurance procedures applied to time-series data.
- Data structure and documentation: One CSV spreadsheet with 159 statistical columns (2–5 intentionally blank) and 32 rows; first row contains headers; rows 2–32 correspond to statistics for the first day of each month from 1 Apr 1982 to 1 Apr 2013.
- Metadata and accessibility: Dataset details, units, estimation periods, and variable definitions provided in the “Nature and Units of Recorded Values” section; data released in a format suitable for reuse and transparency.
- Data governance: Data and associated methods described with emphasis on transparency and reproducibility; IPR considerations addressed via NERC EIDC vetting for online release.

## Data Structure and Accessibility

- Data file: A single .csv containing 159 columns and 32 rows; columns 2–5 blank by design.
- Content coverage: Statistics cover monthly results derived from 1982–2013 daily observations for rainfall, streamflow, pH, and temperature, plus derived indices such as flow pulses and growth-related metrics.
- Variable mapping: Detailed mapping provided in the “Nature and Units of Recorded Values” section, including estimation periods (mostly 365 days prior to sampling, with some metrics using shorter windows like 30 or 120 days).