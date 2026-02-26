# Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain (1960 to 2015): observed driving data [MaRIUS-G2G-MORECS-daily]

## Brief overview
- MaRIUS (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity) was a UK NERC-funded project (2014–2017) developing a risk-based approach to drought and water scarcity.
- The MaRIUS-G2G-MORECS-daily dataset provides Grid-to-Grid (G2G) model estimates of daily mean river flow for 260 NRFA gauged catchments in Great Britain, covering 1960–2015.
- Purpose: enable comparison between modeled natural flows and observed gauged flows for model validation, drought assessment, and policy-relevant monitoring.

## What the dataset contains
- River flow (m3 s-1), daily (09:00 to 09:00) mean of G2G flows at locations corresponding to 260 NRFA gauging stations.
- Driving meteorological data:
  - 1 km x 1 km grids of daily rainfall (CEH-GEAR).
  - Monthly potential evaporation (PE) on a 40 km grid (MORECS).
- 260 NRFA station details are provided in a related file to verify correct station-to-grid cell mapping.

## Hydrological model and driving data (G2G)
- Grid-to-Grid (G2G) is a national-scale hydrological model on a 1 km x 1 km grid with a 15-minute time-step, parameterised using digital datasets (soil, land cover).
- Accounts for urban/suburban land-cover effects on runoff; calibrations are largely avoided in favor of spatial data-based parameters; nationally applicable values used where needed.
- Requires input time-series of precipitation and PE; snow module not used here (precipitation treated as rain).
- Spin-up period not included in these outputs.
- Performance: generally good for catchments with natural flow regimes; reduced accuracy in areas affected by abstractions/discharges or complex sub-surface hydrology.
- The 1 km G2G cell is selected to best represent each NRFA station’s location and catchment area; some small catchments may have catchment-area mismatches. All G2G catchment areas are within 8% of the NRFA catchment areas.

## How to use for monitoring and policy decisions
- Compare natural-flow estimates from G2G with observed NRFA gauged flows to assess drought risk, water scarcity scenarios, and potential management responses.
- Use across multiple catchments to identify where data quality, boundary definitions, or anthropogenic influences affect model performance.
- Assess data gaps and metadata quality to inform future monitoring improvements and data governance.

## Format and data access
- Format: CSV file with a single header line.
  - First column: date.
  - Subsequent columns: daily river flows for each catchment.
- File name: G2G_MORECS_flow_1960_2015.csv (1960–2015).
- Time: daily mean from 09:00 on one day to 09:00 on the following day.
- Related station information file: MaRIUS_NRFAStationInfo.csv with NRFA station ID, river name, location, grid coordinates, G2G catchment, and data issues.

## Metadata, governance, and provenance
- Data driving inputs are observation-based (CEH-GEAR rainfall, MORECS PE).
- Model outputs produced as part of MaRIUS, funded by NERC; open data practices and attribution acknowledged.
- Important caveat: outputs reflect natural flows; artificial abstractions/discharges and complex subsurface hydrology can affect accuracy in certain catchments.

## Acknowledgements and references
- Acknowledgements: MaRIUS project and NERC funding; thanks to collaborators for assistance in data provision.
- Key references include foundational G2G development and performance assessments (Bell et al. 2007, 2009; Rudd et al. 2017; Bell et al. 2016) and input data sources (CEH-GEAR, MORECS, Monteith 1965; Hough & Jones 1997; Keller et al. 2015; Tanguy et al. 2016).