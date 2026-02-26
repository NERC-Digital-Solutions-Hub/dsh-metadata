# Supporting information for Grid-to-Grid model estimates of monthly mean flow and soil moisture for Great Britain: weather@home2 (climate model) driving data [MaRIUS-G2G-WAH2-monthly]

## Overview
- Presents grid-to-grid (G2G) model estimates of monthly mean river flow and soil moisture across Great Britain.
- Driven by the MaRIUS weather@home2 climate model dataset; part of the MaRIUS project on drought and water scarcity risk.
- Outputs are on a 1 km x 1 km grid with 15-minute model time steps, covering historical and future periods.

## What the MaRIUS-G2G-WAH2-monthly dataset provides
- Monthly mean hydrological variables:
  - Flow (m3 s-1)
  - Soil moisture (mm water per m soil)
- Time periods:
  - Historical Baseline (1900–2006)
  - Baseline (1975–2004)
  - Near-Future (2020–2049)
  - Far-Future (2070–2099)
- Spatial data to support interpretation:
  - Digitally-derived catchment areas on a 1 km grid
  - Estimated locations of flow gauging stations on a 1 km grid (NRFA)

## Hydrological model and driving data
- Model: Grid-to-Grid (G2G), a national-scale hydrological model for GB using 1 km grid, 15-minute time steps.
- Land cover and soil properties drive hydrology; urban/suburban effects on runoff are included, calibration is not used for individual catchments.
- Calibration approach: relies on spatial fields rather than catchment-specific parameter calibration.
- Inputs:
  - Precipitation and potential evapotranspiration (PE) from MaRIUS WAH2 regional climate model (RCM).
  - Bias correction applied to precipitation; PE derived via Penman-Monteith, with two versions for future periods (one with adjusted stomatal resistance).
- Future scenarios:
  - Based on RCP8.5; ensembles include multiple SST warming patterns, with 100-member G2G runs per period.

## Data format and organization
- Grid: 700 km x 1000 km GB domain; 1 km x 1 km grid cells; land-only cells (sea set to -9999).
- Temporal format: 30-day months due to 360-day calendar; time units are days since 1900-01-01.
- Variables: flow, soil (monthly means of daily values).
- Ensemble and file structure:
  - 100 ensembles for each period (HISTBS, BS, NF, FF)
  - NetCDF4 format; one file per period and ensemble member
  - File naming: G2G_WAH_var_<period>*1.nc (where var is flow or soil)
- Additional data:
  - MaRIUS_G2G_CatchmentAreaGrid.nc: catchment areas (km2) per 1 km grid box
  - MaRIUS_G2G_NRFAStationIDGrid.nc and MaRIUS_NRFAStationIDs.csv: NRFA gauging station mappings to 1 km grid cells

## How to use MaRIUS-G2G-WAH2-monthly
- Comparisons:
  - For baseline time slices (HISTBS and BS), compare G2G outputs to observational-driven G2G runs (e.g., MaRIUS-G2G-Oudinmonthly) or NRFA observations, not as exact time-series matches but as statistical comparisons over long periods.
  - For future time slices (NF and FF), compare changes relative to the Baseline (BS) rather than to observations.
  - Impacts analyses (economic, ecological, agricultural) using future G2G outputs should be compared to BS results, not to observed real-world outcomes.
- Ensemble interpretation:
  - Treat each ensemble member as a plausible realization; analyze differences across distributions rather than focusing on single-member outcomes.
  - Do not directly compare ensemble members by index across periods (e.g., BS1 vs NF1).
- Data to aid interpretation:
  - NRFA station locations on the 1 km grid allow comparison of grid-based flows to observed station data at corresponding locations.
  - Catchment-area grid helps assess drainage basins for each grid cell.

## Practical considerations and caveats
- G2G limitations:
  - Does not model abstractions or discharges; focuses on natural hydrological response.
  - Calibration is grid-based rather than catchment-specific; uses nationally applicable parameter values.
  - Snow module is not used; precipitation is treated as rain, which may influence interpretation of droughts.
- Data and metadata considerations:
  - Some spatial discretisation can yield catchment-area mismatches for small basins; NRFA-based validation may be affected in such cases.
  - SB/ NF/ FF spin-up periods (first two years of NF/FF and HISTBS) should be ignored for analysis or used to spin up the model.
  - PRISM bias corrections are applied to precipitation; PE is not bias-corrected in all configurations.
- Data governance and sharing:
  - The dataset is provided to support transparent evaluation of drought and water scarcity impacts, with accompanying metadata and documentation.
  - Users should be mindful of the absence of direct one-to-one time-series correspondence with observations; statistical comparisons are appropriate.

## Acknowledgements and references
- Funded by UK NERC as part of MaRIUS (NE/L010208/1) under the UK Drought and Water Scarcity programme.
- Key references related to the G2G model, climate driving data, and methodologies are provided (e.g., Bell et al., 2007; 2009; 2016; Guillod et al., 2018; Kay et al., 2018; Rudd et al., 2017).