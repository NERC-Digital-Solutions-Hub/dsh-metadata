# Supporting information for Grid-to-Grid model estimates of monthly mean flow and soil moisture for Great Britain (1891 to 2015): observed driving data [MaRIUS-G2G-Oudin-monthly]

## Overview
- Provides Grid-to-Grid (G2G) model estimates of monthly mean flow and soil moisture across Great Britain for 1891–2015.
- Part of the MaRIUS project (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity); dataset driven by observation-based meteorological data.

## Data content
- Variables included:
  - Flow (m3 s-1)
  - Soil moisture (mm water per m of soil)
- Both are monthly means of daily values (09:00 to 09:00), historical period 1891–2015.

## Spatial and temporal context
- 1 km x 1 km grid on a 700 km × 1000 km GB domain; land grid cells only (sea cells set to missing).
- Outputs are provided as monthly values assigned to the first day of each month.
- Time reference: days since 1891-01-01; calendar is Gregorian (365 or 366 days).

## Auxiliary spatial datasets
- Digitally-derived catchment areas on a 1 km grid (MaRIUS_G2G_CatchmentAreaGrid.nc).
- Estimated locations of river flow gauging stations on the 1 km grid and a CSV with NRFA station IDs (MaRIUS_NRFAStationIDs.csv and MaRIUS_G2G_NRFAStationIDGrid.nc).

## Model and inputs
- Hydrological model: Grid-to-Grid (G2G), national-scale, 1 km grid, 15-minute time-step.
- Parameterised with soil and land-cover data; accounts for urban/suburban land-cover effects on runoff.
- Calibrations are not performed per catchment; uses globally applicable parameter values.
- Snow module not used here; precipitation input treated as rain.
- G2G outputs represent natural flows (i.e., not adjusted for abstractions or discharges).

## Meteorological driving data
- Daily rainfall: 1 km x 1 km CEH-GEAR dataset.
- Potential evaporation (PE): monthly estimates derived from gridded temperature (5 km × 5 km) using a temperature-based method (Oudin et al., 2005); long-term mean alignment to MORECS via spatial correction factors.
- Early 20th-century rainfall sparsity addressed by spatial infilling (Keller et al., 2015; Rudd et al., 2017).
- PE values are distributed to corresponding 1 km grid cells and split evenly across the 15-minute model time-step.

## Data format and file structure
- Main data file: MaRIUS-G2G-Oudin-monthly 1 km × 1 km gridded data in NetCDF4, named G2G_Oudin_var_1891_2015.nc.
  - Variables: 'flow' or 'soil'
  - Domain: 700 km × 1000 km, center of each 1 km grid cell
  - Time: calendar days since 1891-01-01; monthly values assigned to the first day of each month
- Additional supporting files:
  - MaRIUS_G2G_CatchmentAreaGrid.nc — catchment area (km2) draining to each grid cell
  - MaRIUS_G2G_NRFAStationIDGrid.nc — NRFA station ID mapping per grid cell
  - MaRIUS_NRFAStationIDs.csv — list of NRFA station IDs for which a corresponding 1 km grid cell is identified

## How to use and interpret
- Purpose: Compare G2G flow outputs to observed river flows (e.g., NRFA data) and assess model performance.
- Performance: Generally reasonable for catchments with natural flow regimes; less accurate where artificial abstractions or discharges dominate, or where sub-surface hydrology is complex.
- Station mapping caveat: The NRFA station locations mapped to 1 km grid cells may not perfectly align with observed NRFA catchments, especially for small basins due to discretisation.
- Use cases include drought and low-flow analyses in a historical context, supported by referenced validation studies (e.g., Bell et al. 2009; Rudd et al. 2017; Kay et al. 2018).

## Caveats and data quality
- Model does not account for human abstractions and discharges; suitability is higher for natural-flow-dominated regimes.
- Potential differences between grid-derived catchments and official NRFA catchments for smaller basins.
- Rainfall sparsity in early data mitigated via infilling; PE derived from temperature with long-term corrections.

## Acknowledgements and references
- Dataset outcome of the MaRIUS project funded by the UK Natural Environment Research Council (NE/L010208/1) as part of the UK Drought and Water Scarcity programme.
- Acknowledges contributions from named researchers; references include foundational methods and validation studies (Bell et al. 2009; Rudd et al. 2017; Kay et al. 2018; and others).