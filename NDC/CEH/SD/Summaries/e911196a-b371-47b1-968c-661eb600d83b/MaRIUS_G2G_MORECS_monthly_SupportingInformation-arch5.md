# Supporting information for Grid-to-Grid model estimates of monthly mean flow and soil moisture for Great Britain (1960 to 2015): observed driving data [MaRIUS-G2G-MORECS-monthly]

## Overview
- MaRIUS project (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity), UK NERC-funded (2014–2017), developed a risk-based approach to drought and water scarcity.
- Provides Grid-to-Grid (G2G) model estimates of monthly mean hydrological variables on a 1 km x 1 km grid across Great Britain for 1960–2015.
- Variables: 
  - Flow (m3 s-1)
  - Soil moisture (mm water per m soil), as monthly means of daily values (09:00 to 09:00).
- Additional spatial datasets included to aid interpretation:
  - Digitally-derived catchment areas on a 1 km x 1 km grid.
  - Estimated locations of flow gauging stations on a 1 km x 1 km grid and as CSV.
- Observed driving data used to drive the G2G model (meteorology): 
  - CEH-GEAR daily rainfall at 1 km grid
  - MORECS-based monthly potential evapotranspiration (PE) at 40 km grid

## Data content and structure
- G2G model outputs:
  - Natural flow estimates: monthly averages of daily mean flows (m3 s-1)
  - Soil moisture estimates: monthly averages of daily mean soil moisture (mm water per m soil)
  - Domain: 700 km x 1000 km GB national grid; 1 km x 1 km grid cells; land cells only; sea cells set to -9999
  - Time: Gregorian calendar (365 or 366 days); time in NetCDF as days since 1900-01-01; monthly values assigned to the first day of the month
- Input data:
  - Rainfall: 1 km x 1 km CEH-GEAR daily grids
  - Evapotranspiration: 40 km MORECS data, copied to the 1 km grid and downscaled to the 15-minute model time-step
- Additional files to support interpretation and validation:
  - MaRIUS_G2G_CatchmentAreaGrid.nc: catchment area (km2) draining to each 1 km grid cell
  - MaRIUS_G2G_NRFAStationIDGrid.nc: grid identifying NRFA gauging stations
  - MaRIUS_NRFAStationIDs.csv: NRFA station IDs and details
- File naming and conventions:
  - NetCDF4 format following CEH gridded dataset conventions
  - File: G2G_MORECS_var_1960_2015.nc (var = flow or soil)
  - Spatial domain: 0–700000, 0–1000000 meters (GB National Grid)
  - Missing values: -9999
  - Time: days since 1900-01-01; monthly values aligned to first day of month

## Model and data provenance
- Model: Grid-to-Grid (G2G) hydrological model, 1 km grid, 15-minute time-step, parameterised with digital soil/land-cover data; urban/suburban land-cover effects included for runoff.
- Calibration: Nationally applicable parameter values used where needed; parameterization relies on spatial data rather than catchment-specific calibration.
- Snow module not used in this dataset; precipitation input treated as rain.
- Model performance: generally reasonable for catchments with natural flow regimes; reduced accuracy where artificial abstractions/discharges are important or where sub-surface hydrology is complex.

## Usage and interpretation
- Recommended use: compare G2G natural-flow outputs to observed gauged flows (e.g., NRFA) for validation and drought assessment.
- Strengths: high-resolution, national-scale, consistent framework for multiple years; explicit accounting of urban effects and catchment-area context via supplementary grids.
- Limitations and caveats:
  - Some mismatch between NRFA observed catchments and discretised 1 km G2G catchments, especially for small basins.
  - Data best suited for natural-flow regimes; performance may be affected by anthropogenic influences (abstractions, discharges) not included in the model.
  - The NRFA station placement grid is a best effort to map gauging sites to the 1 km grid; users should check site-to-grid alignment for specific applications.
- Related documentation and references: Bell et al. (2009, 2016); Davies & Bell (2009); Hough & Jones (1997); Keller et al. (2015); Rudd et al. (2017); Tanguy et al. (2016).

## Access, license, and provenance
- Outcome of the MaRIUS project, funded by the UK Natural Environment Research Council (NE/L010208/1) as part of the UK Drought and Water Scarcity programme.
- Acknowledges contributions from collaborators (Nuria Bachiller-Jareno, Matt Fry, Maliko Tanguy).
- Dataset references and links provided for further details and performance assessments:
  - Key publications and data center references listed in the document.