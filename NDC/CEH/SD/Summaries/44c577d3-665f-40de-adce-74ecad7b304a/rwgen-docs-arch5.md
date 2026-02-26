# Rainfall and Weather GENerator (RWGEN) Code and Data: Supporting Documentation

## Overview
- Contains the stochastic Rainfall and Weather GENerator (RWGEN) model code and observed historical climate input data for UK applications.
- RWGEN can simulate one or more stochastic realizations of rainfall, temperature, and potential evapotranspiration at hourly or longer timesteps for single sites or spatial regions.

## Data Components
- Observational historical climate input data:
  - Historical hourly rainfall time series (331 stations).
  - Historical daily weather time series (1000 stations).
  - Period: 1853 to 2020, sourced from UK Met Office MIDAS-Open datasets.
- RWGEN model code (snapshot) from RWGEN GitHub (rwgen-0.0.5).
- Station metadata (station_metadata.csv) and accompanying package documentation.

## Data Collection and Source
- Data sourced from UK Met Office MIDAS-Open (Met Office Integrated Data Archive System).
- Training data can be used to train RWGEN for UK locations or catchments; users may supply alternative training data.
- MIDAS-Open data coverage is uneven through 1853–2020 (less data before mid-20th century); internal handling exists for partial data.

## Data Structure and Files
- Observed data stored in two folders:
  - historical_daily-weather: 1000 CSV files (daily variables) named XXXXX_YYYYY.csv (station ID and lowercase station name).
  - historical_hourly-rainfall: 331 CSV files (hourly rainfall) with the same naming convention.
- station_metadata.csv contains metadata for stations (Point_ID, Station_Name, File_Name, Latitude, Longitude, Easting, Northing).
- RWGEN code is contained in rwgen-0.0.5, a Python package snapshot with a structure including rwgen, rainfall, and weather submodules.

## Data Content and Units
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
- Missing data indicated by NA values, following UKMO quality control procedures.

## Metadata and Provenance
- station_metadata.csv links MIDAS station identifiers to file names and geographic coordinates (Latitude/Longitude, Easting/Northing).
- Data quality controlled using the UKMO MIDAS-Open qc1 dataset; users are encouraged to perform additional quality checks.
- RWGEN model component is a snapshot of the core code from the RWGEN GitHub repository; updated releases exist online with accompanying package documentation.

## Quality Assurance and Limitations
- QA checks performed on extraction/processing; model has been tested against RainSim V3 and observations with good consistency in test cases.
- Limitations acknowledged; users should verify fitness-for-purpose for their specific applications.

## Access, Installation, and Reuse
- Installation: navigate to the root rwgen-0.0.5 directory and run: pip install -e .
- Full package documentation and examples are available online; a demo Jupyter notebook provides an accessible RWGEN tutorial without requiring local installation.

## Usage Notes for Data Stewards
- Monitor updates/releases beyond the 0.0.5 snapshot to maintain current governance and interoperability.
- Maintain data lineage and metadata alignment with MIDAS-Open sources; document any data changes or replacements.
- Be explicit about data availability across stations and periods, and communicate any partial data or QC limitations to data users.