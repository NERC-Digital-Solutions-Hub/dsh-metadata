# Supporting information for Grid-to-Grid model estimates of monthly mean flow and soil moisture for Great Britain (1891 to 2015): observed driving data [MaRIUS-G2G-Oudin-monthly]

## Overview
- MaRIUS project (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity) funded by UK NERC (2014–2017) to develop a risk-based drought and water scarcity framework.
- Dataset provides Grid-to-Grid (G2G) model estimates of monthly mean hydrological variables on a 1 km × 1 km grid across Great Britain (GB) for 1891–2015.
- Variables: 
  - Flow (m3 s−1)
  - Soil moisture (mm water per m soil)
- Outputs are monthly means of daily values (09:00 to 09:00).
- Two auxiliary spatial datasets accompany the data:
  - Digitally-derived catchment areas on a 1 km grid
  - Estimated locations of flow gauging stations on a 1 km grid and as a CSV

## G2G model at a glance
- National-scale hydrological model for GB, running on a 1 km grid with a 15-minute time-step.
- Parameterised using digital datasets (soil types, land-cover) and accounts for urban/suburban land-cover effects on runoff and downstream flows.
- Calibrations are not used to identify parameters for individual catchments; instead, spatial datasets are used.
- Snow module not used here; precipitation input is treated as rain.
- Outputs provided as:
  - Monthly averages of daily mean natural flows (m3 s−1)
  - Monthly averages of daily mean soil moisture (mm water per m soil)
- Time step and spatial resolution imply depth-integrated soil moisture values across variable soil depths (0 to several metres).

## Input driving data
- Meteorological driving data are observation-based:
  - 1 km × 1 km daily rainfall grids (CEH-GEAR)
  - Monthly potential evaporation (PE) estimates on a 5 km × 5 km grid (derived from temperature)
- Early 20th century rainfall data (where measurements were sparse) were spatially infilled.
- PE estimation:
  - Temperature-based method (Oudin et al. 2005) used to estimate monthly PE from gridded temperatures (1891 onward)
  - Monthly spatial correction factors applied to align long-term means with MORECS (Rudd et al. 2007)
- PE values are copied to the corresponding 1 km grid cells; both rainfall and PE are divided down to the 15-minute model time-step.
- Other spatial data used to configure G2G (topography, soil data) follow Bell et al. 2009.

## Data products and format
- G2G output: MaRIUS-G2G-Oudin-monthly 1 km × 1 km grids in NetCDF4
  - File name: G2G_Oudin_var_1891_2015.nc
  - Variables: 'flow' or 'soil'
  - Domain: 700 km × 1000 km GB grid (0,0 to 700000,1000000 metres); land grid boxes only; sea values set to -9999
  - Time: days since 1891-01-01; monthly values assigned to the first day of each month
- Supporting spatial datasets:
  - MaRIUS_G2G_CatchmentAreaGrid.nc — catchment area (km2) draining to each 1 km grid box
  - MaRIUS_G2G_NRFAStationIDGrid.nc — 1 km grid with NRFA gauging station IDs (1285 stations)
  - MaRIUS_NRFAStationIDs.csv — list of NRFA station IDs
- NRFA gauging station mapping notes:
  - The best 1 km grid cell for each NRFA gauging station is selected based on proximity and catchment area, with checks to ensure correct tributary attribution
  - Some small catchments may have catchment areas that differ between the NRFA and the 1 km grid due to discretisation

## Usage, interpretation, and limitations
- Use-case: compare G2G natural-flow outputs to observed gauged river flows (e.g., NRFA data).
- Model performance:
  - Reasonably good for catchments with natural flow regimes and accurate observational records
  - Less accurate where artificial abstractions/discharges are significant or where subsurface hydrology is unusually complex
- Calibration approach:
  - G2G relies on spatial data and nationally applicable parameter values rather than catchment-specific calibration
- Important caveats:
  - G2G provides natural-flow estimates; the presence of human water management can affect real-world flows
  - The NRFA catchment areas and gauging station mapping may not perfectly align for all small catchments due to grid discretisation

## Figure and references
- Figure 1 illustrates example grids for flow and soil moisture, NRFA gauge locations, and catchment-area grid over Wales.
- Key references include Bell et al. (2009, 2016), Davies & Bell (2009), Hough & Jones (1997), Keller et al. (2015), Rudd et al. (2017), Oudin et al. (2005), Perry & Hollis (2005), and related MaRIUS outputs.
- Acknowledgement: dataset produced as part of MaRIUS project (NE/L010208/1) under UK Drought and Water Scarcity programme.