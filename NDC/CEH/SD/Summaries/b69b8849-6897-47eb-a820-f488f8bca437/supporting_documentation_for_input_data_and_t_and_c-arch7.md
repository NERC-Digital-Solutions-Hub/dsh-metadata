# The energy and mass balance of Peruvian glaciers

- This data collection supports the Peru GROWS and PEGASUS projects (NERC grants NE/S013296/1, NE/S013318/1) and is tied to the paper The energy and mass balance of Peruvian glaciers (Fyffe et al., accepted, J. Geophysical Research: Atmospheres). It documents meteorological inputs, data processing, and model implementation (Tethys-Chloris) used to calculate melt and mass balance at point scale for five Peruvian glaciers.

## Scope and geographic context for GIS work

- On-glacier weather stations used for modelling:
  - Shallap Glacier (Cordillera Blanca)
  - Artesonraju Glacier (Cordillera Blanca)
  - Cuchillacocha Glacier (Cordillera Blanca)
  - Quisoquipina Glacier (Cordillera Vilcanota)
  - Quelccaya Ice Cap (Cordillera Vilcanota)
- Data include precise station coordinates, elevations, and instrument heights, enabling GIS mapping of meteorological inputs and model domains.
- Outputs and inputs are designed for integration with spatial analyses and map-based visualizations of energy balance components and glacier responses.

## Data content and structure

- Data are organized into three main folders:
  - Input_data: cleaned and filled on-glacier meteorological inputs (hourly timeseries) for five stations; includes Ta, Pr, U, Ws, Rsw, Latm, L_out, NetR, SR_50, zatm_hourly_m, Ameas, and related metadata.
  - Main_run_code: codes for running the Peru-specific Tethys-Chloris (T&C) model (e.g., T_and_C_Peru_EIDC.m, PARAM_Peru.m, Peru_Automatic_Radiation_Partition_I.m, Precipitation_partition_Ding.m).
  - T_and_C: model functions used in simulations (numerous energy balance, radiation, soil, and hydrology components).
- Documentation and data include both MATLAB data files (.mat) and CSV exports:
  - Some files contain final corrected inputs ready for model run; others hold raw or intermediate data.
  - Key CSV fields in on-glacier inputs: Datetime, Ta (°C), Pr (mm h-1), U (fraction), Ws (m s-1), Rsw (W m-2), Rsw_out, Latm (W m-2), L_out, NetR, SR_50 (m), zatm_hourly_m, Ameas (albedo).
- Off-glacier data are used to fill gaps where on-glacier data are missing, with site-specific corrections to preserve diurnal/seasonal patterns.
- Some data gaps remain (notably 1 Dec 2011 to 27 May 2012 for Shallap), due to limited overlap among Shallap stations and lack of appropriate donor data.

## Data cleaning and gap-filling approach

- Quality control and cleaning rules:
  - Remove clearly erroneous data; cap RH at 100%; correct negative/invalid shortwave radiation values to 0; ensure S↑ ≤ S↓; remove non-positive wind speeds before filling.
  - Wind-related gaps and zero wind values are replaced with monthly hourly averages to maintain sensible turbulent fluxes.
  - Large jumps flagged (e.g., Ta changes > 10°C, RH changes > 40%) are inspected and corrected or removed.
- Gap filling and data replacement strategies:
  - On-glacier time series are extended by using nearby off-glacier data or data from other years when appropriate, with emphasis on preserving diurnal and seasonal cycles.
  - When necessary, Weather Research and Forecasting (WRF) model outputs or relationships with donor stations are used to fill missing periods.
  - Precipitation data corrections:
    - Off-glacier precipitation is adjusted to be representative of on-glacier conditions (e.g., adjusting for elevation and undercatch).
    - Snowfall corrections use undercatch factors for snow under snow conditions and are integrated with liquid precipitation to form corrected hourly series.
- Station-specific notes:
  - Shallap data had extensive gaps; corrections are largely restricted to on-glacier data, with limited cross-site filling due to lack of overlap.
  - Cuchillacocha data relied heavily on relationships with off-glacier data (CQ) due to limited on-glacier coverage; corrections include temperature and humidity adjustments to align with on-glacier conditions.

## Tethys-Chloris model (TC) integration

- All TC model code used to run the point-scale simulations is provided.
- The main execution file is T_and_C_Peru_EIDC.m, which loads input data, applies site-specific parameters (PARAM_Peru.m), and runs MAIN_FRAME.m and related TC functions.
- Model inputs required for site adaptation include Ta, U, Ws, Rsw, and Pr; optional inputs include L↓ and cloudiness if longwave data are not provided; albedo and snow/ice properties can be simulated or provided as inputs.
- Output conventions:
  - Flux directions follow the technical reference; later analysis codes convert fluxes to downward-positive conventions as needed.
- Model documentation references:
  - TC_Variable_and_Parameter_List.pdf and TeC_technical_reference.pdf contain parameter definitions, equations, and structure.
- For GIS users, the climate and radiative partition inputs can be spatially mapped, with model runs enabling generation of glacier-energy-balance rasters or time-series per station/region.

## Data formats, access, and reuse

- Input_data contains per-station meteorological inputs in .csv and .mat formats:
  - On-glacier observations (Ta, Pr, U, Ws, Rsw, L↓, L↑, SR_50, etc.)
  - Station metadata: location, elevation, instrument heights, and measured variables
- Data are prepared for ingestion by the T&C model and suitable for GIS integration as point-based climate inputs or for driving spatially interpolated fields.
- Metadata and documentation include:
  - Detailed station tables (instrument types, heights, and measurement variables)
  - Data correction rules and filling procedures
  - Model parameter references and structure
- The dataset is intended to support the creation of map-based representations of glacier energy balance and mass-balance processes across Peruvian glacier regions.

## Practical implications for GIS specialists

- Enables mapping of meteorological inputs and modelled energy balance across Peruvian glacier sites.
- Provides hourly time-series data and station metadata suitable for spatial analyses, interpolation, and visualization of spatial patterns in temperature, humidity, radiation, precipitation, and wind.
- The three-folder structure (Input_data, Main_run_code, T_and_C) supports reproducible GIS workflows and potential replication of model runs for new sites with adjusted parameters.
- Caution: some data gaps remain; plan for gap-aware analyses or supplement with modelled inputs (WRF, off-glacier relationships) where necessary.