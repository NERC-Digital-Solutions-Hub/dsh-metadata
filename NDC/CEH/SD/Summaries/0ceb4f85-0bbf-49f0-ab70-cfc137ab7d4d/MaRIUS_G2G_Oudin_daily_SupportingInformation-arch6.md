Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain (1891 to 2015): observed driving data [MaRIUS-G2G-Oudin-daily] Bell VA, Rudd AC, Kay AL and Davies HN (2018). Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain (1891 to 2015): observed driving data [MaRIUS-G2G-Oudin-daily]. NERC Environmental Information Data Centre. https://catalogue.ceh.ac.uk/documents/0ceb4f85-0bbf49f0-ab70-cfc137ab7d4d

## Overview
- Describes the MaRIUS-G2G-Oudin-daily dataset, which provides Grid-to-Grid (G2G) model estimates of daily mean river flow for 260 gauged catchments across Great Britain from 1891 to 2015.
- Focuses on the observed driving data used to drive the G2G model: rainfall and potential evaporation (PE) inputs.

## What the dataset provides
- Daily natural river flow estimates (m3 s-1) for 260 NRFA gauging stations, on a 1 km x 1 km G2G grid, with flows recorded as 09:00 to 09:00 the following day.
- A companion file details the 260 NRFA gauging stations used to map each station to the corresponding G2G grid cell.

## Hydrological model and inputs (G2G)
- Grid-to-Grid (G2G) is a national, high-resolution hydrological model (1 km grid, 15-minute time-step) parameterised with soil and land-cover data.
- Requires input time-series of precipitation (daily rainfall) and potential evapotranspiration (PE).
- Driving meteorological inputs:
  - 1 km x 1 km daily rainfall grids (CEH-GEAR: Keller et al. 2015; Tanguy et al. 2016).
  - Monthly PE estimates derived from temperature on a 5 km x 5 km grid (Oudin et al. 2005).
- Early-20th-century rainfall data gaps were spatially infilled; PE uses a temperature-based method since pre-1960 MORECS data are not available.
- Snow module not used; precipitation treated as rainfall; spin-up not included.

## Model characteristics and caveats
- Driven by observed data, with calibration not performed at the catchment level; uses nationally applicable parameter values.
- G2G outputs reflect natural flows and are best for catchments with minimal anthropogenic influence; performance decreases where abstractions/discharges are significant or sub-surface hydrology is complex.
- Each NRFA station is matched to the nearest 1 km G2G cell representing the corresponding catchment; catchment areas can differ from NRFA definitions, especially for small catchments (differences within about 8%).

## Data format and files
- MaRIUS-G2G-Oudin-daily flow data stored as a CSV with a single header row.
- File: G2G_Oudin_flow_1891_2015.csv (columns: Date, followed by one column per catchment).
- Time reference: 09:00 to 09:00 daily mean flows; calendar follows Gregorian 365/366 days.
- Related file: MaRIUS_NRFAStationInfo.csv provides station details (ID, river, location, G2G coordinates, catchment area, data issues).

## How to use
- Compare G2G daily flows (1891–2015) with observed NRFA flows to assess model performance.
- Best for natural-flow regimes; interpret with caution where human abstractions/discharges shape flows.
- Use the mapped G2G cell closest to each NRFA station, with additional checks to ensure correct tributary representation.

## Data quality, limitations, and references
- Model performance documented in Bell et al. (2009) and Rudd et al. (2017); strongest for natural regimes and reliable NRFA records.
- Limitations include potential misalignment of very small catchments and lack of calibration for individual basins.
- Data provenance: MaRIUS project (Managing the Risks, Impacts and Uncertainties of droughts and water Scarcity), NERC grant NE/L010208/1; acknowledgments to contributors.

## Access and acknowledgements
- Data produced under MaRIUS (2014–2017) and made available through the NERC Environmental Information Data Centre.
- Acknowledges contributors and references foundational methodology and data sources (CEH-GEAR, MORECS, Oudin PE method, etc.).