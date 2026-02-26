# Rainfall and Weather GENerator (RWGEN) Code and Data: Supporting Documentation

- The dataset provides stochastic Rainfall and Weather Generator (RWGEN) model code and observed historical UK climate input data. It can simulate one or more stochastic realizations of rainfall, temperature, and potential evapotranspiration at hourly or longer timesteps, for single sites or spatial simulations (historical/reference or future scenarios).

## Collection/Generation Methods
- Observational climate input data come from the UK Met Office MIDAS-Open dataset (1853–2020).
- Hourly rainfall data: 331 stations; Daily weather data: 1000 stations.
- Data can train RWGEN for UK locations or catchments, or be supplied by users as alternative training data.
- MIDAS-Open coverage is uneven, with lower data availability before the mid-20th century.
- Daily weather data may have incomplete variables for some stations; RWGEN includes handling for partial data.

## Details of Data Structure
- Observed historical climate inputs are stored in .csv files directly compatible with RWGEN.
  - Hourly rainfall files contain only rainfall values.
  - Daily weather files contain multiple weather variables.
  - Each file’s first column is a date/time series; subsequent columns are time series values.
- Data folders:
  - historical_daily-weather: 1000 .csv files for daily weather data (station variables).
  - historical_hourly-rainfall: 331 .csv files for hourly rainfall data.
- File naming: XXXXX_YYYYY.csv
  - XXXXX = MIDAS station number
  - YYYYY = MIDAS station name in lowercase (e.g., lerwick)
- station_metadata.csv: station metadata (see below)
- Code is in rwgen-0.0.5:
  - environment.yml, setup.py
  - rwgen/ (core model)
    - rainfall/ (analysis, fitting, model, nsproc, perturbation, plotting, properties, shuffling, simulation, utils)
    - weather/ (fa56, model, preprocessing, simulation)
- The dataset provides installation instructions and a demo Jupyter notebook.

## Nature and Units of Recorded Values
- Data come from the UKMO observing network; units follow MIDAS-Open conventions.
- Hourly rainfall files:
  - DateTime: YYYY-MM-DD HH:MM:SS
  - Rainfall: mm/hour
- Daily weather files:
  - datetime: YYYY-MM-DD
  - prcp: mm/day
  - temp_mean: °C (mean of hourly temps if available)
  - temp_min: °C
  - temp_max: °C
  - temp_avg: °C (average of min and max)
  - rel_hum: %
  - vap_press: kPa
  - sun_dur: hours
  - wind_speed: m/s
- NA values indicate missing/low-quality data per UKMO quality control.
- station_metadata.csv includes:
  - Point_ID: unique station ID
  - Station_Name: station name
  - File_Name: corresponding data file names
  - Latitude/Longitude: decimal degrees
  - Easting/Northing: OSGB36 coordinates (metres)

## Quality Control
- Inputs sourced from the quality-controlled MIDAS-Open qc1 dataset.
- Additional spot checks confirmed extraction/processing plausibility.
- Users are advised to perform further quality checks in applications.
- RWGEN has been tested against RainSim V3 and observations; limitations acknowledged; ensure fit-for-purpose.

## RWGEN Model
- The dataset is a snapshot of the RWGEN core from the GitHub repository rwgen1/rwgen.
- Rainfall component: Neyman-Scott Rectangular Pulse (NSRP) process (aligned with RainSim V3 literature).
- Weather and PET component: regression-based models per Kilsby et al. (2007), Jones et al. (2010), and FAO Paper 56 guidance.
- Documentation and installation available online; installation example:
  - Navigate to rwgen-0.0.5 and run: pip install -e .
- A demo Jupyter notebook provides a basic RWGEN tutorial without requiring full installation.

## How This Supports Data Use and Sharing
- Provides ready-to-use UK climate data inputs and a reproducible modeling framework for exploring rainfall and weather scenarios.
- Enables creation of data products (e.g., self-serve simulations, dashboards) for policy and planning contexts (e.g., local councils, private sector).
- Clear provenance (MIDAS-Open sources, QC, model references) supports data traceability and re-use.
- Offers templates and examples for applying RWGEN to new locations or alternative training data.