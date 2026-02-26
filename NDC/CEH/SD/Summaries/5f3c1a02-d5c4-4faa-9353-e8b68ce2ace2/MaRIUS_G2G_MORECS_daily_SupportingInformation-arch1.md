# Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain (1960 to 2015): observed driving data [MaRIUS-G2G-MORECS-daily]

## Overview
- Provides Grid-to-Grid (G2G) model estimates of daily mean river flow for 260 NRFA gauged stations across Great Britain, 1960–2015.
- Variable: river flow (m3 s-1), daily mean from 09:00 to 09:00 the next day.
- Enables comparison between modelled natural flows and observed gauged flows; highlights performance across catchments with varying influence from human activity.

## Model and driving data
- Hydrological model: Grid-to-Grid (G2G) on a 1 km x 1 km grid with 15-minute time steps; parameterised from spatial datasets (soil, land-cover) rather than per-catchment calibration.
- Optional snow module not used; precipitation input treated as rain.
- Meteorological drivers:
  - 1 km x 1 km daily rainfall (CEH-GEAR)
  - Monthly potential evapotranspiration (PE) data on a 40 km grid (MORECS)
- Model outputs natural river flows (no abstractions/discharges included) for 260 sites over 1960–2015; spin-up not included.

## NRFA station matching and catchment details
- Each NRFA gauging station is paired with the G2G grid cell that best represents its location and catchment area, with additional checks to ensure correct river tributary attribution.
- In some cases, the G2G-derived catchment area draining to the chosen 1 km cell differs from the NRFA catchment area; however, all G2G catchment areas are within 8% of NRFA catchment areas.

## Data format and files
- MaRIUS-G2G-MORECS-daily dataset: G2G_MORECS_flow_1960_2015.csv
  - CSV with a header row; first column is date, subsequent columns are catchments.
  - Time reference: 09:00 on each day to 09:00 the following day.
- Related file: MaRIUS_NRFAStationInfo.csv
  - Details of the 260 NRFA stations, including station ID, river name, location, G2G coordinates, catchment area, and data issues.

## How to use and interpretation
- Use G2G daily natural-flow estimates to compare with observed NRFA river flows; assess model accuracy across catchments with natural vs. anthropogenically influenced regimes.
- Performance: G2G generally performs well for catchments with natural flow regimes and accurate observed records; performance declines where artificial abstractions, discharges, or complex subsurface hydrology are important.
- Practical considerations:
  - G2G cell proximity and catchment-area matching are approximate; small catchments may incur larger proportional errors due to discretisation.
  - Flows represent natural conditions; not suitable for analyses requiring reported abstractions/discharges unless adjusted.
- Data quality caveats:
  - Recommended to reference the NRFA for observed data comparisons; acknowledge potential mismatches in catchment delineations.

## Acknowledgments and references
- Funded by the UK Natural Environment Research Council (MaRIUS project: Managing the Risks, Impacts and Uncertainties of droughts and water Scarcity).
- References include foundational work on high-resolution grid-based hydrological modelling, MORECS, CEH-GEAR, and related drought analyses.