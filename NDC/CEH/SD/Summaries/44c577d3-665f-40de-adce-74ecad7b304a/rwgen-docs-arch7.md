# Rainfall and Weather GENerator (RWGEN) Code and Data: Supporting Documentation

## Overview
- Provides stochastic RWGEN model code and observed historical climate input data for UK applications.
- Simulates one or more stochastic realizations of rainfall, temperature, and potential evapotranspiration at hourly or longer timesteps.
- Supports single-site or spatial simulations for historic/reference or perturbed/future climate.

## Data Collection and Generation Methods
- Input data: historical hourly rainfall and daily weather time series from UK Met Office MIDAS-Open across the UK.
- Coverage: 1853–2020; hourly data for 331 stations; daily data for 1000 stations.
- Training data: used to train RWGEN for UK locations or catchments; users may supply alternative data.
- Data gaps: MIDAS-Open data coverage is inconsistent before the mid-20th century; some variables are not consistently available for all stations.
- RWGEN handles partial data availability internally for some variables.

## Data Structure and Organization
- Historical climate input data stored in two folders:
  - historical_daily-weather: 1000 CSV files containing daily weather series for 1000 stations.
  - historical_hourly-rainfall: 331 CSV files containing hourly rainfall values for 331 stations.
- File naming convention: XXXXX_YYYYY.csv where XXXXX is MIDAS station number and YYYYY is station name (lowercase, e.g., lerwick).
- station_metadata.csv contains metadata with:
  - Point_ID, Station_Name, File_Name, Latitude, Longitude, Easting, Northing (OSGB36/UK grid).
- Data format: CSV with the first column as Date/Time; subsequent columns as time series values.
  - Hourly rainfall files: single rainfall column.
  - Daily weather files: multiple weather variables.
- Code and package organization (rwgen-0.0.5):
  - environment.yml, setup.py
  - rwgen/
    - __init__.py, model.py
    - rainfall/ (analysis, fitting, model, nsproc, perturbation, plotting, properties, shuffling, simulation, utils)
    - weather/ (fa56.py, model.py, preprocessing.py, simulation.py)

## Nature and Units of Recorded Values
- Data come from UKMO MIDAS-Open observing network; units defined in the documentation:
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
- Station metadata aligns with MIDAS-Open identifiers and coordinates (Latitude/Longitude and OSGB36 Easting/Northing).

## Quality Control
- Data derived from the quality-controlled MIDAS-Open dataset (qc1).
- Additional spot checks performed to verify extraction, processing, and reformatting.
- Users are encouraged to perform further quality checks in their applications.
- RWGEN has been tested against RainSim V3 and observations; generally consistent but with model limitations; users should assess fitness-for-purpose.

## RWGEN Model Components
- Snapshot of core RWGEN components from the RWGEN GitHub repository; newer releases available online.
- Rainfall component: based on the Neyman-Scott Rectangular Pulse (NSRP) process, following RainSim V3 (Burton et al., 2008).
- Weather and PET component: regression-model-based approach following Kilsby et al. (2007), Jones et al. (2010), and FAO Paper 56 guidance.
- Documentation and installation: full package docs are available online; a demo Jupyter notebook is provided for a beginner-friendly RWGEN tutorial.
- Installation: pip install -e in the root rwgen-0.0.5 directory.

## Access, Installation, and Documentation
- References and resources:
  - Met Office MIDAS Open data (UK land-surface stations)
  - RWGEN GitHub repository
  - RWGEN package documentation (online HTML)
  - Foundational papers: RainSim (Burton et al. 2008), Kilsby et al. 2007, Jones et al. 2010, FAO Paper 56
- Demo notebook available via online bindings (no prior Python knowledge required for the tutorial).

## Data Use in GIS and Practical Considerations
- GIS-enabled use: data enable spatial rainfall and weather simulations across UK stations/catchments for map-based analyses and visualization.
- Key GIS-relevant assets:
  - station_metadata.csv with precise coordinates (Latitude/Longitude and OSGB36 coordinates) for spatial mapping.
  - Hourly and daily time-series inputs suitable for GIS-driven rainfall/runoff modeling and climate risk mapping.
- Considerations for GIS workflows:
  - data coverage gaps and varying temporal resolutions across stations require careful preprocessing.
  - alignment of station metadata with spatial layers and coordinate systems used in GIS projects.
  - quality control and documentation should accompany any GIS data products to ensure traceability and reproducibility.

## Endnotes and References
- References to MIDAS-Open data and RWGEN resources, including:
  - Met Office MIDAS Open data documentation
  - RWGEN GitHub repository
  - RWGEN package documentation
  - RainSim (Burton et al. 2008)
  - Kilsby et al. (2007), Jones et al. (2010)
  - FAO Irrigation and drainage paper 56
  - RWGEN demo notebook and installation guidance