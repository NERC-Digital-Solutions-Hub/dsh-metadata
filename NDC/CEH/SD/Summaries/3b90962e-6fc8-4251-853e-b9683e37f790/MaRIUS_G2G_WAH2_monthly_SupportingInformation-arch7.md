# Supporting information for Grid-to-Grid model estimates of monthly mean flow and soil moisture for Great Britain: weather@home2 (climate model) driving data [MaRIUS-G2G-WAH2-monthly]

## Overview
- Provides Grid-to-Grid (G2G) model estimates of monthly mean river flow and soil moisture on a 1 km x 1 km grid across Great Britain.
- Variables: Flow (m3 s-1) and soil moisture (mm water per m of soil), monthly means of daily values.
- Periods: historical, near-future, and far-future — enabling assessment of drought and water scarcity risks.
- Spatial extent and resolution: 700 km x 1000 km GB domain at 1 km resolution; data aligned to the GB national grid.
- Ensemble design: 100 G2G simulations for each period (historical baseline HISTBS, Baseline BS, Near-Future NF, Far-Future FF).

## Data and variables
- Primary outputs:
  - Flow: monthly average of daily mean flows (m3 s-1).
  - Soil moisture: monthly average of daily mean soil moisture (mm water/m soil); interpretable as depth-integrated θ (0 to 1).
- Supporting spatial datasets (all on 1 km x 1 km grid):
  - Digitally-derived catchment areas.
  - Estimated locations of flow gauging stations (NRFA) on the 1 km grid and as a CSV.
- Additional NRFA-related grids/files:
  - MaRIUS_G2G_NRFAStationIDGrid.nc: NRFA station IDs mapped to grid cells (1285 stations; land cells labeled 0, sea -9999, NRFA ID otherwise).
  - MaRIUS_NRFAStationIDs.csv: list of NRFA station IDs for which a corresponding 1 km grid box exists.

## Model and methods
- Hydrological model: Grid-to-Grid (G2G), 1 km grid, 15-minute time-step, parameterised with spatial data (soil, land cover, etc.).
- Key features:
  - Accounts for urban/suburban land-cover effects on runoff.
  - Generally used with spatial datasets rather than catchment-specific calibration; uses nationally applicable parameter values where needed.
  - Optional snow module not used here; precipitation treated as rain.
  - Calibrated for broad applicability; validated for low flows and drought detection.
- Driving meteorological data:
  - MaRIUS weather@home2 (WAH2) regional climate model (RCM) dataset, providing multiple ensemble simulations for historical and future climates.
  - Future scenarios driven by RCP8.5 emissions; precipitation underwent bias correction (monthly multiplicative factors); potential evaporation (PE) derived via Penman-Monteith from other WAH2 variables.
  - PE calculations: historical use MORECS-based stomatal resistance; future PE includes adjusted resistance to account for CO2 effects (modulates low-flow projections).
- Data preprocessing:
  - WAH2 precipitation and PE re-projected from ~25 km rotated lat/lon grid to 1 km G2G grid.
  - Within each RCM box, precipitation is spatially weighted to reflect typical annual rainfall patterns.
  - The WAH2 dataset uses a 360-day year (12 months of 30 days).

## Temporal coverage and ensembles
- Periods and members:
  - Historical Baseline (HISTBS): 1900–2006.
  - Baseline (BS): 1975–2004.
  - Near-Future (NF): 2020–2049.
  - Far-Future (FF): 2070–2099.
- Each period contains 100 ensemble members (1–100) representing plausible realizations of climate for that period.
- Spin-up notes:
  - The first two years of HISTBS, NF, and FF are spin-up years and should be ignored in analyses or used only for spin-up purposes.

## Format and structure
- Data format: NetCDF4, one file per period and ensemble member.
- File naming conventions:
  - HISTBS: G2G_WAH_var_HISTBS*.nc
  - BS: G2G_WAH_var_BS*.nc
  - NF: G2G_WAH_var_NF*.nc
  - FF: G2G_WAH_var_FF*.nc
  - Variables: flow or soil
- Spatial and temporal metadata:
  - Domain: 700 km x 1000 km GB grid from (0,0) to (700000,1000000) in metres.
  - Cells: every non-sea 1 km x 1 km grid box; sea cells are set to missing (-9999).
  - Time: 30-day months due to the 360-day calendar; time units are days since 1900-01-01; first day of each month is used.
- Grid alignment and NRFA mapping:
  - NRFA gauging station locations mapped to the closest 1 km cell with checks to ensure correct tributary catchment alignment.
  - Some small catchments may have differences between derived and observed catchments due to discretisation.

## Usage guidance and cautions
- Comparisons to observations:
  - Compare G2G-WAH2 outputs to observation-based G2G runs or NRFA data statistically (multi-year averages, distributions), not as direct time-series matches.
  - Baseline (BS) should be used for comparing future NF/FF results, not directly against observed historical series.
- Future analyses:
  - Compare NF/FF outputs to BS to assess projected changes, not to observed data.
  - Treat ensemble members as plausible realisations; do not directly compare members across periods with the same index (e.g., BS1 vs NF1).
- Interpretation caveats:
  - G2G flow outputs reflect natural flows and do not include abstractions or discharges; urban effects are represented only through land-use parameters.
  - The NRFA catchment mapping and 1 km grid discretisation may introduce some mismatches for small catchments.

## How to access and link datasets
- Core dataset: MaRIUS-G2G-WAH2-monthly (1 km x 1 km grid) with flow and soil moisture outputs for HISTBS, BS, NF, FF.
- Supporting spatial data:
  - MaRIUS_G2G_CatchmentAreaGrid.nc (catchment areas by grid cell).
  - MaRIUS_G2G_NRFAStationIDGrid.nc (NRFA station IDs mapped to grid cells).
  - MaRIUS_NRFAStationIDs.csv (NRFA station IDs for which grid boxes exist).
- Observational references for validation and comparison (examples):
  - NRFA (National River Flow Archive) for observed river flows.
  - Observational G2G runs driven by different inputs for cross-validation.

## Acknowledgements and references
- Produced as part of the MaRIUS project (Managing the Risks, Impacts and Uncertainties of droughts and water Scarcity), NE/NERC-funded.
- Key methodological references include Bell et al. (2007, 2009, 2016), Davies & Bell (2009), Guillod et al. (2018), Hough & Jones (1997), Monteith (1965), and Rudd et al. (2017, 2018).