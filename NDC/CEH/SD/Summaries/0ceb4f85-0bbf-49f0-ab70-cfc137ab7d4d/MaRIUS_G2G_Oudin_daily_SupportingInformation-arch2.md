# Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain (1891 to 2015): observed driving data [MaRIUS-G2G-Oudin-daily]

## Overview
- MaRIUS (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity) was a UK NERC-funded project (2014–2017) developing a risk-based drought and water scarcity framework.
- The MaRIUS-G2G-Oudin-daily dataset provides Grid-to-Grid (G2G) model estimates of daily mean river flow for 260 NRFA gauged catchments across Great Britain from 1891 to 2015.
- Variable provided: River flow (m3 s-1), daily mean from 09:00 to 09:00, at the grid cell closest to each NRFA gauge; a related file lists the 260 NRFA gauging stations.

## Model and inputs
- Hydrological model: Grid-to-Grid (G2G) is a national-scale, 1 km x 1 km grid model running at 15-minute time steps, parameterised from soil, land-cover and other spatial data. It accounts for urban/suburban runoff effects and is designed for natural-flow regimes.
- Calibration: Uses spatial datasets for parameters rather than catchment-specific calibration; nationally applicable values are used when needed (e.g., kinematic wave speeds). The model is noted to perform well for low flows and drought identification; less well where artificial abstractions/discharges dominate.
- Forcing data: G2G requires precipitation and potential evaporation (PE).
  - Precipitation: 1 km x 1 km grids of daily rainfall (CEH-GEAR; Keller et al. 2015; Tanguy et al. 2016).
  - PE: Monthly PE estimates derived from temperature on a 5 km x 5 km grid (Rudd et al. 2017; Oudin et al. 2005); a temperature-based method is used (MORECS-compatible adjustments) to match long-term means.
- Snow module: Not used here; precipitation input is treated as rain.
- Time handling: PE and rainfall are distributed to the 15-minute model time-step; PE copies to corresponding 1 km boxes.
- Data preparation: Early 20th-century rainfall data with identified gaps were spatially infilled (Keller et al. 2015; Rudd et al. 2017).

## Data format and scope
- Output format: CSV file named G2G_Oudin_flow_1891_2015.csv with a single header line.
  - First column: date.
  - Subsequent columns: daily mean river flow for each catchment (0-filled or missing values as applicable).
  - Time reference: 09:00 to 09:00 the following day.
- Supporting station information: MaRIUS_NRFAStationInfo.csv provides details for the 260 NRFA gauging stations, including station ID, river name, location, G2G easting/northing, catchment area, and data issues.
- Spin-up period: not included in these files.
- Geographic matching: Each G2G flow value is associated with the NRFA station by selecting the closest 1 km grid cell representative of the station’s location and catchment. In some cases, the G2G-derived catchment area draining to the selected cell may differ from the NRFA catchment area; typical differences are within 8%.

## Data quality, performance and caveats
- Use cases: G2G provides “natural” river-flow estimates suitable for comparison with observed gauged flows (NRFA) and for drought-focused analyses.
- Strengths: Reasonable agreement for catchments with natural flow regimes and well-measured gauges.
- Limitations: Reduced accuracy in catchments heavily affected by artificial abstractions or discharges or with complex subsurface hydrology; no calibration to individual catchments.
- Important caveat: The dataset reflects natural flows without spin-up; users should account for potential discrepancies in small catchments due to discretisation to a 1 km grid.

## Access, acknowledgements and references
- Acknowledgements: MaRIUS project (NERC) and contributors (Nuria Bachiller-Jareno, Matt Fry, Maliko Tanguy) for guidance and data availability.
- Funding: UK Natural Environment Research Council (NE/L010208/1) as part of the UK Drought and Water Scarcity programme.
- Key references for methods and datasets include Bell et al. (2007, 2009, 2016), Hough & Jones (1997), Monteith (1965), Oudin et al. (2005), Perry & Hollis (2005), Rudd et al. (2017), Tanguy et al. (2016), Keller et al. (2015), and Kay et al. (2018).

## Relevance for Analysts Monitoring the Environment
- Provides a standardized, QA’d long-term dataset (1891–2015) enabling consistent assessment of environmental health and drought risk across multiple catchments.
- Supports cross-catchment comparisons using a uniform modelling framework, reducing calibration bias at individual catchments.
- Facilitates data integration by delivering both the main flow dataset and station metadata, enabling transparent provenance and traceability.
- Highlights the value of combining datasets (e.g., G2G outputs with observed NRFA data) and ensuring accessible data through recognized portals; mindful of limitations where anthropogenic influences or discretisation affect accuracy.