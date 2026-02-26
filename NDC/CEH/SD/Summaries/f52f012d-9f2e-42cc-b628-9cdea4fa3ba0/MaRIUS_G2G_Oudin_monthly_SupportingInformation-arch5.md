# Supporting information for Grid-to-Grid model estimates of monthly mean flow and soil moisture for Great Britain (1891 to 2015): observed driving data [MaRIUS-G2G-Oudin-monthly]

## Overview
- MaRIUS project (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity), UK NERC-funded (2014-2017).
- Provides Grid-to-Grid (G2G) model estimates of monthly mean hydrological variables on a 1 km x 1 km grid across Great Britain for 1891-2015.
- Variables: Flow (m3 s-1) and soil moisture (mm water per m soil); monthly means of daily values (09:00–09:00).
- Two supporting spatial datasets are included to aid interpretation: catchment areas and estimated NRFA gauging station locations.

## Data content
- Primary variables:
  - Flow (m3 s-1)
  - Soil moisture (mm water/m soil) — interpreted as depth-integrated soil moisture (0 ≤ θ ≤ 1)
- Temporal coverage: 1891–2015 (historic period)
- Spatial coverage: Great Britain on a 1 km x 1 km grid (non-sea grid; sea values are missing -9999)
- Additional datasets:
  - Digitally-derived catchment areas on a 1 km x 1 km grid (MaRIUS_G2G_CatchmentAreaGrid.nc)
  - Estimated NRFA gauging station locations on the 1 km x 1 km grid and a CSV with NRFA station IDs
  - NRFA station mapping grids: MaRIUS_G2G_NRFAStationIDGrid.nc; MaRIUS_NRFAStationIDs.csv

## Model, inputs, and driving data
- Hydrological model: Grid-to-Grid (G2G) running at 1 km resolution with a 15-minute time-step; parameterised from soil and land-cover datasets; accounts for urban/suburban land-cover effects on runoff.
- Input meteorology:
  - Daily rainfall on 1 km x 1 km CEH-GEAR grids
  - Monthly potential evaporation (PE) on 5 km x 5 km grid (derived from temperature)
- Data treatment:
  - Early 20th-century rainfall measurements (where sparse) spatially infilled
  - PE estimated using a temperature-based method (Oudin et al. 2005) with long-term mean corrections to fit MORECS values
  - Precipitation and PE are distributed uniformly to the 15-minute time-step
- Snow module not used; precipitation treated as rain
- Model outputs are monthly averages of daily natural flows and soil moisture

## Format and data structure
- Primary NetCDF4 file: G2G_Oudin_var_1891_2015.nc
  - Variables: 'flow' and 'soil'
  - Time reference: days since 1891-01-01; monthly values assigned to the first day of each month
  - Spatial domain: 700 km x 1000 km; 1 km x 1 km grid cells; land-only values; sea set to -9999
- Supporting files for NRFA alignment:
  - MaRIUS_G2G_NRFAStationIDGrid.nc (1 km grid with NRFA station IDs)
  - MaRIUS_NRFAStationIDs.csv (NRFA station IDs for which a corresponding grid cell is available)
- Documentation notes:
  - Time series limited to natural flows (no anthropogenic abstractions or discharges modeled)
  - NRFA station alignment may introduce small discrepancies in catchment areas for some small basins due to grid discretisation

## How to use and interpret
- Validation context:
  - G2G flow estimates compare to observed NRFA gauged flows; best for catchments with natural flow regimes and accurate gauged records
  - Less accurate where artificial water use or discharges dominate, or where sub-surface hydrology is complex
- Cautions:
  - For small catchments, grid discretisation can lead to mismatches between modeled catchment areas and observed NRFA catchments
  - PE estimation pre-1960 uses a temperature-based approach; users should be aware of potential biases in earlier periods
- Usage options:
  - Compare G2G monthly flows to NRFA observations to assess drought and low-flow characteristics (as per related analyses)
  - Use catchment-area and NRFA station mapping to link modeled grid outputs to observed station data

## Data provenance and acknowledgements
- Outcome of the MaRIUS project (NE/L010208/1) under the UK Drought and Water Scarcity programme
- Acknowledgements to contributors for advice and data availability
- Key references include foundational G2G methodology and supporting datasets for rainfall, evaporation, and catchment delineation

## References and related materials
- Bell VA, Kay AL, Jones RG et al. (2009); Bell VA, Kay AL, Davies HN, Jones RG (2016)
- Hough M, Jones RJA (1997); Keller VDJ, Tanguy M et al. (2015); Oudin L et al. (2005)
- Perry M, Hollis D (2005); Rudd AC, Bell VA, Kay AL (2017); Tanguy M, Dixon H et al. (2016)
- Figures and supplementary materials illustrating example outputs and NRFA station locations