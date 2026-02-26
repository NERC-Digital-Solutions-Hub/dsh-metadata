# Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain (1960 to 2015): observed driving data [MaRIUS-G2G-MORECS-daily]

- Overview
  - MaRIUS (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity) was a UK NERC-funded project (2014–2017) focused on a risk-based approach to drought and water scarcity.
  - This dataset provides Grid-to-Grid (G2G) model estimates of daily mean river flow for gauged catchments across Great Britain, covering 1960–2015 and 260 NRFA gauging stations.
  - Variable: river flow (m3 s−1), daily mean from 09:00 to 09:00 the following day.

- Hydrological model and approach
  - Grid-to-Grid (G2G) is a national-scale hydrological model running on a 1 km × 1 km grid with a 15-minute time-step, parameterised from digital datasets (soil, land-cover, etc.).
  - The model emphasizes natural (uninfluenced) flow regimes; it does not account for artificial abstractions or discharges.
  - Calibration focuses on data-driven, grid-based parameters rather than catchment-specific calibration. A snow module is not used in this dataset; precipitation input is treated as rain.

- Input driving data
  - Meteorological driving data are observation-based:
    - 1 km × 1 km daily rainfall grids (CEH-GEAR; Keller et al. 2015; Tanguy et al. 2016).
    - Monthly potential evapotranspiration (PE) data on a 40 km grid (MORECS; Hough and Jones 1997).
  - PE values are copied to each 1 km grid box and distributed equally to the 15-minute model time-step alongside rainfall.
  - Spatial data for model configuration include topography and soil data consistent with Bell et al. (2009).

- Outputs and interpretation
  - Natural-flow estimates produced for 260 sites across Britain (1960–2015); these can be compared to observed NRFA flows.
  - Model performance is best for catchments with natural flow regimes; less accurate where artificial abstractions/discharges or complex subsurface hydrology are influential.
  - The chosen G2G grid cell for each NRFA station is the closest in location and catchment area, with checks to ensure correct river tributary attribution. Some small catchments may still experience discrepancies between G2G and NRFA catchment areas (up to ~8%).

- Data format and related files
  - MaRIUS-G2G-MORECS-daily flow data are stored in a CSV file with a single header line.
  - File: G2G_MORECS_flow_1960_2015.csv
    - First column: date
    - Subsequent columns: daily mean flows for each catchment
    - Period: 1960–2015 (calendar includes 365 or 366 days per year)
    - Time convention: flows are 09:00 to 09:00 the next day
  - Related file: MaRIUS_NRFAStationInfo.csv
    - Details for the 260 NRFA gauging stations, including station ID, river name, location, G2G grid mapping, catchment area, and data issues

- Usage guidance and limitations
  - The dataset supports evaluation of modeled natural river flows against observed NRFA data.
  - Best used for drought and water-scarcity analyses in natural-flow-dominated regions; caution advised in areas with strong human modifications.
  - Spin-up period is not included; potential discretisation differences can affect small catchments.
  - Acknowledges uncertainties in catchment-area mapping between NRFA and 1 km G2G cells, and the general limitation of not modelling certain human interventions.

- Acknowledgements and references
  - Funded by the UK Natural Environment Research Council (NE/L010208/1) as part of the MaRIUS program.
  - Acknowledgements to contributors for data preparation and dissemination.
  - Key references include Bell et al. (2007, 2009, 2016), Hough & Jones (1997), Keller et al. (2015), Monteith (1965), Rudd et al. (2017), and Tanguy et al. (2016).