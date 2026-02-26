# Rainfall and Weather GENerator (RWGEN) Code and Data: Supporting Documentation

## Overview
- Provides stochastic RWGEN model code and observed historical climate input data for UK applications.
- RWGEN can generate one or more stochastic realizations of rainfall, temperature, and potential evapotranspiration at hourly or longer timesteps, for single sites or spatial simulations (historical/reference or perturbed/future climate).

## Data sources and collection
- Observational input data come from UK Met Office MIDAS-Open (historical hourly rainfall and daily weather time series across the UK).
- Coverage: 1853–2020.
  - Hourly rainfall: 331 stations.
  - Daily weather: 1000 stations.
- Training data for RWGEN can be used as provided or substituted with user-supplied data.
- MIDAS-Open data coverage is uneven before the mid-20th century; some variables are not consistently available for all stations over the full period.

## Data structure and content
- Historical climate input data are stored as CSV files directly compatible with RWGEN.
  - Hourly rainfall files: one column date/time, subsequent columns rainfall values (mm/hour).
  - Daily weather files: date, prcp (mm/day), temp_mean, temp_min, temp_max, temp_avg, rel_hum, vap_press, sun_dur, wind_speed (with appropriate units).
- NA values indicate missing or low-quality data per UKMO QC procedures and are removed accordingly.
- Folder layout:
  - historical_daily-weather: 1000 CSV files (daily weather for 1000 stations).
  - historical_hourly-rainfall: 331 CSV files (hourly rainfall for 331 stations).
  - station_metadata.csv: station metadata (Point_ID, Station_Name, File_Name, Latitude, Longitude, Easting, Northing).
- File naming convention: XXXXX_YYYYY.csv (XXXXX = MIDAS station number; YYYYY = station name in lowercase, e.g., lerwick).
- Data interpretation and units are documented in the accompanying "Nature and Units of Recorded Values" section.

## Metadata and quality control
- Metadata provided in station_metadata.csv with geographic coordinates in OSGB36 and MIDAS identifiers.
- Data sourced from the quality-controlled MIDAS-Open qc1 dataset; additional spot checks performed.
- Users are encouraged to perform further quality checks for their specific applications.
- RWGEN has been tested against RainSim V3 and observations; generally good consistency, but users should assess fit-for-purpose for their use case.

## RWGEN model components and data usage
- Model core components are a snapshot of the RWGEN GitHub repository (rwgen-0.0.5).
  - Rainfall: Neyman-Scott Rectangular Pulse (NSRP) process (aligned with RainSim V3).
  - Weather and PET: regression-based component drawing on Kilsby et al. (2007), Jones et al. (2010), and FAO Paper 56 guidance.
- Documentation and references available describing model concepts, use, and typical applications.

## Software, installation, and access
- Installation: pip install -e (within the rwgen-0.0.5 directory).
- After installation, examples and full package references are available; templates for new model setups are provided.
- A demo Jupyter notebook is available (no prior Python knowledge required) via an online notebook link (mybinder).

## Usage and reproducibility
- Data can be used to train RWGEN for UK locations or catchments or to simulate perturbed/future climate scenarios.
- The dataset and code are structured to support reproducible experiments, with explicit data files, metadata, and model components.
- The package documentation (online) provides installation specifics, typical use cases, and templates for setting up new models.

## Limitations and caveats
- Historical MIDAS-Open data have non-uniform coverage, particularly before the mid-20th century.
- Some daily variables are not consistently available for all stations across the entire period.
- Although RWGEN aligns with established models (RainSim V3, FAO methods), users should validate model suitability for their specific policy questions and ensure data quality for their applications.

## References
- Met Office MIDAS Open data (2019) and associated documentation.
- RWGEN GitHub repository (Pritchard et al., 2022).
- RWGEN package documentation (online).
- Foundational works: RainSim (Burton et al. 2008), Kilsby et al. (2007), Jones et al. (2010), FAO Paper 56, and related methodological papers.

## Relevance for monitoring frameworks
- Provides a transparent, data-driven basis for generating climate inputs used in environmental health monitoring and policy evaluation.
- Supports scenario analysis and assessment of policy interventions under UK climate variability and change.
- Highlights governance considerations: data provenance, metadata completeness, data quality assurance, data accessibility, and reproducibility of monitoring outputs.