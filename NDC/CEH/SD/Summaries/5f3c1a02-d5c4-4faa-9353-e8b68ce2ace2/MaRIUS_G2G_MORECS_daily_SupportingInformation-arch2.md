# Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain (1960 to 2015): observed driving data [MaRIUS-G2G-MORECS-daily]

## Overview
- MaRIUS project (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity) funded by UK NERC (2014–2017).
- Provides Grid-to-Grid (G2G) model estimates of daily mean river flow for 260 NRFA gauged catchments across Great Britain for 1960–2015.
- Dataset: MaRIUS-G2G-MORECS-daily, with flows (m3 s-1) at 09:00–09:00 for the location corresponding to NRFA gauges.
- A related file describes the 260 NRFA gauging stations used.

## Dataset contents and scope
- Variable: River flow (m3 s-1), daily mean (09:00–09:00) for locations matching NRFA gauges.
- Coverage: 260 NRFA gauging stations across Britain, 1960–2015.
- Output file: G2G_MORECS_flow_1960_2015.csv (daily flows; one column per catchment; header line with dates).
- Supporting station details: MaRIUS_NRFAStationInfo.csv (station ID, river name, location, G2G coordinates, catchment area, data issues).

## Model and driving data (Grid-to-Grid, G2G)
- Model: Grid-to-Grid hydrological model at 1 km x 1 km resolution, 15-minute time-step; parameterised from digital datasets (soil, land-cover, topography).
- Purpose: Estimate natural river flows, suitable for comparison with observed flows where anthropogenic influences are minimal.
- Notable features:
  - Accounts for urban/suburban land-cover effects on runoff.
  - Primarily uses spatial data; limited calibration at the catchment level (nationally applicable parameter values).
  - Snow module not used here; precipitation treated as rain.
  - Spin-up not included in these files.

## Meteorological driving data
- Precipitation: 1 km x 1 km CEH-GEAR daily rainfall (Keller et al. 2015; Tanguy et al. 2016).
- Evaporation: Monthly potential evaporation (PE) data on a 40 km grid (MORECS; Hough and Jones 1997).
- PE values are distributed to 1 km boxes and, together with rainfall, are divided across 15-minute model time-steps.

## How to use the dataset
- Purpose: Compare G2G natural-flow estimates with observed gauged flows from NRFA.
- Performance notes:
  - G2G performs well for catchments with natural flow regimes and accurate observed records.
  - Less accurate where artificial abstractions/discharges are significant or where sub-surface hydrology is complex.
- Matching approach:
  - Each G2G flow value is taken from the 1 km grid cell closest to the NRFA gauge, chosen to best represent the gauge location and catchment area.
  - Additional checks ensure the correct river tributary is used; differences in catchment area between derived G2G cell and NRFA catchment can occur, particularly for small catchments (up to ~8% area difference).

## Data format and accessibility
- Format: CSV with a single header line; first column is date, subsequent columns correspond to each catchment.
- File details:
  - Historical file: G2G_MORECS_flow_1960_2015.csv
  - Time convention: daily mean from 09:00 to 09:00 the following day
- Additional information file: MaRIUS_NRFAStationInfo.csv (station metadata and data issues)

## Data quality, caveats, and limitations
- Spin-up period is not included in these simulations.
- Potential catchment misalignment for small catchments due to 1 km grid discretisation; overall catchment areas are within 8% of NRFA catchment areas.
- Model emphasizes natural flows and may underrepresent human influences such as abstractions and discharges.

## Data provenance and acknowledgements
- Dataset outcome of the MaRIUS project (Managing the Risks, Impacts and Uncertainties of droughts and water Scarcity) funded by the UK Natural Environment Research Council (NE/L010208/1).
- Acknowledgements to individuals for advice and assistance in data availability.
- Related methodological references and data descriptions provided (Bell et al., Rudd et al., etc.).

## References (key sources)
- Bell VA, Kay AL, Jones RG, Moore RJ (2007)
- Bell VA, Kay AL, Jones RG et al. (2009)
- Bell VA, Kay AL, Davies HN, Jones RG (2016)
- Hough M, Jones RJA (1997)
- Keller VDJ, Tanguy M et al. (2015)
- Monteith JL (1965)
- Rudd AC, Bell VA, Kay AL (2017)
- Tanguy M, Dixon H et al. (2016)