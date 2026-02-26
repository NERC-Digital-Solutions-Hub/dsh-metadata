# Rainfall and Weather GENerator (RWGEN) Code and Data: Supporting Documentation

## Overview
- Provides stochastic RWGEN model code and observed historical climate input data for UK applications.
- RWGEN can simulate one or more stochastic realizations of rainfall, temperature, and potential evapotranspiration at hourly or longer timesteps.
- Supports single-site or spatial simulations for historical/reference or perturbed/future climate.

## Data and Observations
- Historical input data come from UK Met Office MIDAS-Open, covering 1853–2020.
- Hourly rainfall data: 331 stations; daily weather data: 1000 stations.
- MIDAS-Open data coverage is uneven, with limited data prior to the mid-20th century.
- Historical data used for training RWGEN, with options to supply alternative training data.

## Data Structure and Access
- Stored as CSV files directly compatible with RWGEN.
- Data organized into two folders:
  - historical_daily-weather: 1000 CSV files with daily weather variables.
  - historical_hourly-rainfall: 331 CSV files with hourly rainfall values.
- File naming convention: XXXXX_YYYYY.csv where XXXXX is MIDAS station number and YYYYY is the lowercase station name (e.g., lerwick).
- station_metadata.csv contains metadata (Point_ID, Station_Name, File_Name, Latitude, Longitude, Easting, Northing).
- RWGEN code snapshot located in rwgen-0.0.5, with a structure mirroring the Github repository rwgen.

## Observed Variables and Units
- Hourly rainfall files:
  - Date/time: YYYY-MM-DD HH:MM:SS
  - Rainfall: mm/hour
- Daily weather files:
  - Date/time: YYYY-MM-DD
  - Rainfall (prcp): mm/day
  - Mean temperature (temp_mean): °C
  - Minimum temperature (temp_min): °C
  - Maximum temperature (temp_max): °C
  - Average temperature (temp_avg): °C
  - Relative humidity (rel_hum): %
  - Actual vapour pressure (vap_press): kPa
  - Sunshine duration (sun_dur): hours
  - Wind speed (wind_speed): m/s
- NA values indicate missing or low-quality data per UKMO quality control procedures.

## Quality Control and Data Processing
- Data derived from quality-controlled MIDAS-Open qc1 data.
- Additional spot checks performed on extraction, processing, and reformatting.
- Users advised to perform further quality checks for their applications.
- RWGEN validated against RainSim V3 and observations; limitations acknowledged; users should ensure fit-for-purpose.

## RWGEN Model Details
- Rainfall component based on Neyman-Scott Rectangular Pulse (NSRP) process; follows RainSim V3 approach.
- Weather and PET component based on regression models (Kilsby et al., Jones et al., FAO Paper 56).
- Capabilities:
  - Generate stochastic realizations for historical/reference or future scenarios.
  - Supports single-site or spatial simulations.
  - Can train on provided UK data or user-supplied data.
- Model version in this dataset is a snapshot of the core RWGEN GitHub repo; newer releases may exist.
- Full installation and usage guidance available online in package documentation.

## Installation and Usage
- Installation: navigate to the root rwgen-0.0.5 directory and run: pip install -e .
- After installation, examples and a full package reference are available for templates and use cases.
- Demo Jupyter notebook available (RWGEN tutorial) that does not require prior Python knowledge or local installation.

## References and Further Resources
- MIDAS Open data documentation (Met Office)
- RWGEN GitHub repository
- RWGEN package documentation
- Foundational papers on RainSim (Burton et al.)
- Kilsby et al. (daily weather generator)
- Jones et al. (UKCP09 projections)
- FAO Paper 56 guidelines
- RWGEN demo notebook (binder-based resource)