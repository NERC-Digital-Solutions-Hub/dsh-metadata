# Rainfall and Weather GENerator (RWGEN) Code and Data: Supporting Documentation

- Purpose and scope
  - Provides stochastic RWGEN model code and observed historical climate input data for UK applications.
  - Enables simulation of one or more stochastic realizations of rainfall, temperature, and potential evapotranspiration at hourly or longer timesteps.
  - Supports single-site or spatial simulations of historical/reference or perturbed/future climate.

- Collection/Generation methods
  - Observational climate input data: historical hourly rainfall and daily weather time series from selected UK Met Office MIDAS-Open stations.
  - Period covered: 1853 to 2020.
  - Data sources: MIDAS-Open; training data for RWGEN possible, with users allowed to supply alternative data.
  - Coverage: hourly rainfall data for 331 stations; daily weather data for 1000 stations.
  - Data quality: some periods have incomplete data; RWGEN includes internal handling for partial data.

- Data structure and contents
  - Observed data stored as CSV files directly compatible with RWGEN.
  - Time column: first column in each file.
  - Hourly rainfall files: single rainfall values per time step.
  - Daily weather files: multiple weather variables per time step.
  - Directories:
    - historical_daily-weather: 1000 CSV files (daily variables) named XXXXX_YYYYY.csv.
    - historical_hourly-rainfall: 331 CSV files (hourly rainfall) named XXXXX_YYYYY.csv.
  - Naming convention: XXXXX is MIDAS station number; YYYYY is MIDAS station name in lowercase (e.g., lerwick).
  - station_metadata.csv: metadata for stations (Point_ID, Station_Name, File_Name, Latitude, Longitude, Easting, Northing).

- RWGEN code and architecture
  - Code snapshot provided in rwgen-0.0.5, reflecting core components of the RWGEN GitHub repository.
  - Folder structure highlights:
    - environment.yml, setup.py
    - rwgen/
      - __init__.py, model.py
      - rainfall/ (analysis.py, fitting.py, model.py, nsproc.py, perturbation.py, plotting.py, properties.py, shuffling.py, simulation.py, utils.py)
      - weather/ (__init__.py, fa56.py, model.py, preprocessing.py, simulation.py)

- Nature and units of recorded values
  - Hourly rainfall (Precipitation): mm/hour
  - Daily weather (per day):
    - prcp: mm/day (rainfall)
    - temp_mean: °C
    - temp_min: °C
    - temp_max: °C
    - temp_avg: °C
    - rel_hum: %
    - vap_press: kPa
    - sun_dur: hours
    - wind_speed: m/s
  - Data quality: NA values indicate missing or low-quality data and are removed per UKMO quality control (QC) procedures.

- Quality control and validation
  - Data sourced from the quality-controlled UKMO MIDAS-Open qc1 dataset.
  - Additional spot checks performed during extraction/processing.
  - Users encouraged to perform further data quality checks for their applications.
  - RWGEN has been tested against RainSim V3 and observations; reasonable consistency observed; note limitations and assess fitness-for-purpose.

- RWGEN model details and references
  - Rainfall component uses Neyman-Scott Rectangular Pulse (NSRP) process (aligned with RainSim V3 approach).
  - Weather and potential evapotranspiration component uses regression-based approaches (Kilsby et al. 2007; Jones et al. 2010; FAO Paper 56 guidance).
  - Further documentation and examples available in the accompanying package documentation.

- Installation, usage, and training
  - Installation: navigate to the rwgen-0.0.5 directory and run: pip install -e .
  - After installation: access examples and a full package reference for templates and setup.
  - Demo: a Jupyter notebook is available (no prior Python knowledge or local RWGEN installation required) via a linked demo notebook.

- Applications for analysts
  - Train RWGEN on UK locations or catchments using historical data; alternative training data can be supplied.
  - Generate multiple stochastic realizations for any length to study historical, reference, or future/perturbed climate scenarios.
  - Useful for environmental monitoring and policy performance evaluations where standardized, repeatable climate realizations are needed.

- Practical notes for use
  - Data producers should store and upload resulting datasets to appropriate data portals.
  - Ensure alignment with monitoring standards and maintain audit trails for data provenance and model outputs.

- References
  - Met Office MIDAS Open: UK Land Surface Stations Data (1853-current)
  - RWGEN GitHub repository and package documentation
  - Foundational works: RainSim (Burton et al. 2008), Kilsby et al. 2007, Jones et al. 2010, FAO Paper 56
  - RWGEN demonstration notebook and related online resources