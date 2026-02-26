# Rainfall and Weather GENerator (RWGEN) Code and Data: Supporting Documentation

- A dataset comprising stochastic RWGEN model code and historical UK climate input data for use in UK applications.
- RWGEN can simulate one or more stochastic realizations of rainfall, temperature, and potential evapotranspiration at hourly or longer timesteps, for single sites or spatial catchments, covering historical, reference, or perturbed/future climates.

## Data Collection and Generation

- Observational climate input data are historical hourly rainfall and daily weather series from selected UK Met Office MIDAS-Open stations (1853–2020).
- Hourly rainfall data: available for 331 stations; daily weather data: available for 1000 stations.
- MIDAS-Open data may have inconsistent coverage, especially before the mid-20th century; RWGEN can use provided data or user-supplied training data.
- Data are stored as CSVs and organized into two folders:
  - historical_daily-weather
  - historical_hourly-rainfall
- A station_metadata.csv accompanies the data, providing station identifiers, names, file mappings, and geographic coordinates (lat/long and OSGB36 coordinates).

## Data Structure and Contents

- File naming: XXXXX_YYYYY.csv, where XXXXX is the MIDAS station number and YYYYY is the lowercase station name.
- Historical daily-weather CSVs: multiple daily weather variables per station.
- Historical hourly-rainfall CSVs: single rainfall variable per file.
- The first column in both types is a date/time stamp; subsequent columns contain time series values.
- Metadata columns include Point_ID, Station_Name, File_Name, Latitude, Longitude, Easting, and Northing.
- The RWGEN code is provided in a separate folder (rwgen-0.0.5), which contains a snapshot of the GitHub repository with modules for environment setup and rainfall/weather components.

## Nature and Units of Recorded Values

- Hourly rainfall files contain:
  - Date/time (DateTime): YYYY-MM-DD HH:MM:SS
  - Rainfall (Precipitation): mm/hour
- Daily weather files contain:
  - Date/time (datetime): YYYY-MM-DD
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

## Quality Control and Provenance

- Data were extracted from the QC version (qc1) of UKMO MIDAS-Open; additional spot checks confirm processing fidelity.
- Users are encouraged to perform further quality checks in their applications.
- RWGEN has been tested against RainSim V3 and observations; users should assess fitness-for-purpose for their specific use cases.

## RWGEN Model and Reproducibility

- Model components:
  - Rainfall: Neyman-Scott Rectangular Pulse (NSRP) process, following RainSim V3 concepts.
  - Weather and PET: regression-based component following FAO 56 guidance and related UK studies.
- Reference material and implementations are available via:
  - RWGEN GitHub repository (core concepts and code)
  - RWGEN package documentation (installation and usage)
  - Demo Jupyter notebook for an approachable RWGEN tutorial
- Installation:
  - pip install -e (from the rwgen-0.0.5 directory)
  - After installation, examples and templates are available for setting up new models.

## Access, Use, and Documentation

- Data source: UK Met Office MIDAS-Open data (open data access for UK land surface stations).
- Code source: RWGEN repository on GitHub; a snapshot is provided in the rwgen-0.0.5 folder.
- Documentation and tutorials are available online, including installation guides and a demo notebook.
- The dataset supports training RWGEN on UK locations or catchments and can incorporate user-supplied data.

## Practical Considerations for Data Leaders

- Discoverability and discoverable metadata: station_metadata.csv and standardized file naming aid data discovery across platforms.
- Data gaps and granularity: uneven historical coverage, especially before the mid-20th century; user may need supplementary data for certain applications.
- Data quality and reliability: reliance on MIDAS-Open QC; additional independent quality checks recommended.
- Interoperability and reuse: CSV format with clear variable units; compatible with RWGEN modeling workflows and reproducible analyses.
- Collaboration and community: dataset references and open-source code encourage cross-team collaboration and validation against other tools (e.g., RainSim V3).

## Endnotes and References

- Meta-knowledge and validation references for RWGEN and related methods are included in the supporting documentation, including:
  - Met Office MIDAS Open data reference
  - RWGEN GitHub repository and package documentation
  - Foundational papers on NSRP rainfall modeling (RainSim V3) and UK climate generator methods
  - FAO Paper 56 guidelines and related climate/evapotranspiration sources
  - Demo notebook and installation instructions

- For users seeking to deploy RWGEN in policy or operational environments, ensure alignment with data quality checks, data availability for your specific sites, and fit-for-purpose validation against observed or trusted benchmarks.