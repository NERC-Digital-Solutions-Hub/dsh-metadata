Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain (1891 to 2015): observed driving data [MaRIUS-G2G-Oudin-daily]

## Overview
- MaRIUS is a UK NERC-funded project (2014-2017) focused on drought and water scarcity risk assessment.
- Provides Grid-to-Grid (G2G) model estimates of daily mean river flow for gauged catchments across Great Britain (1891-2015) at 260 NRFA gauging stations, representing natural (unabstractions/discharges) flows.
- Dataset enables comparison between high-resolution modelled natural flows and observed gauged flows, supporting drought/water scarcity analyses.

## Model and driving data
- Grid-to-Grid (G2G) model:
  - National-scale hydrological model on a 1 km x 1 km grid with a 15-minute time-step.
  - Parameterised using spatial datasets (soil, land cover); accounts for urban/suburban land-cover effects on runoff.
  - Calibrations are not performed per catchment; where parameters are needed, nationally-applicable values are used.
  - Optional snow module not used here; precipitation input treated as rain.
  - Produces daily natural flows (m3 s-1) for 260 sites; best for catchments with natural flow regimes; limited where human abstractions/discharges dominate.
- Driving meteorology:
  - Rainfall: 1 km x 1 km CEH-GEAR daily rainfall data.
  - Potential evapotranspiration (PE): monthly, derived from temperature data on a 5 km x 5 km grid (Oudin et al., 2005); long-term mean values adjusted to match MORECS (Rudd et al., 2007).
  - Early-20th-century rainfall data gaps are spatially infilled (Keller et al., 2015; Rudd et al., 2017).
  - PE estimates based on temperature-based method (Perry & Hollis 2005) for 1891-2015.

## Data products and format
- Output: natural daily river flow estimates (m3 s-1) for 260 NRFA sites, 1891-2015.
- Time convention: flows are 09:00 to 09:00 the following day.
- Grid cell matching: the G2G cell is chosen to best represent each NRFA station’s location and catchment area; checks ensure correct river tributary.
- File formats:
  - G2G_Oudin_flow_1891_2015.csv: daily flows; first column is date, subsequent columns correspond to each catchment.
  - MaRIUS_NRFAStationInfo.csv: metadata for the 260 NRFA stations (station ID, river, location, G2G coordinates, catchment area, data issues).
- Catchment-area comparison: G2G catchment areas are within 8% of NRFA catchment areas.

## How to use and interpret
- Primary use: compare G2G natural-flow estimates to observed gauged flows from NRFA to assess model performance and drought/low-flow risk analyses.
- Performance expectations:
  - Generally performs well for natural-flow regimes.
  - Performance degrades in catchments with significant human influence (abstractions/discharges) or complex subsurface hydrology.
- Practical considerations:
  - Ensure correct mapping between NRFA gauges and G2G grid cells; small catchments may have larger discretisation errors.
  - Use as a baseline natural-flow reference, with caution where anthropogenic factors are important.

## Data quality, limitations, and governance
- Limitations:
  - Outputs represent natural flows only; do not include human water management effects.
  - PE estimation relies on a temperature-based method for 1891-2015 due to historical data constraints; early-period rainfall data have gaps infilled, introducing potential biases.
  - 1 km grid discretisation can yield catchment-area differences relative to NRFA definitions (up to 8%).
- Metadata and provenance:
  - Data built on CEH-GEAR rainfall (Keller et al., 2015; Tanguy et al., 2016) and PE estimates linked to temperature observations (Perry & Hollis, 2005; MORECS adjustments in Rudd et al., 2007).
  - Validation and drought-focused analyses documented in related works (e.g., Bell 2009; Rudd et al. 2017; Kay et al. 2018).
- Data governance and sharing:
  - Data are published as part of the MaRIUS project outputs; associated metadata provided in MaRIUS_NRFAStationInfo.csv.
  - Acknowledgements note contributions from collaborators and funding sources (NERC NE/L010208/1).

## Access and references
- Data availability: NERC Environmental Information Data Centre (MaRIUS-G2G-Oudin-daily; related NRFA station info).
- Key references for methods and validation:
  - Bell et al. (2009, 2016), Rudd et al. (2017), Perry & Hollis (2005), Keller et al. (2015), Oudin et al. (2005), Tanguy et al. (2016), etc.
- Acknowledgments: project team and funding; appreciation for data providers and advisors.