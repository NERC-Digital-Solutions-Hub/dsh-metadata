# Supporting information for Grid-to-Grid model estimates of monthly mean flow and soil moisture for Great Britain: weather@home2 (climate model) driving data [MaRIUS-G2G-WAH2-monthly]

## Overview
- Provides Grid-to-Grid (G2G) model estimates of monthly mean river flow and soil moisture across Great Britain on a 1 km × 1 km grid.
- Part of MaRIUS (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity), a UK NERC-funded project (2014–2017) focused on drought and water scarcity risk.

## What’s in the dataset
- Variables:
  - Flow (m³ s⁻¹): monthly means of daily mean natural river flow.
  - Soil moisture (mm water m⁻¹ soil): monthly means of daily mean soil moisture (depth-integrated across the soil profile).
- Spatial and temporal coverage:
  - 1 km × 1 km grid across Great Britain; non-sea grid cells only.
  - Periods and ensembles:
    - Historical Baseline (HISTBS): 1900–2006
    - Baseline (BS): 1975–2004
    - Near-Future (NF): 2020–2049
    - Far-Future (FF): 2070–2099
  - Each period includes 100 ensemble members (100 realizations).
- Supporting spatial datasets:
  - Digitally-derived catchment areas on 1 km grid.
  - Estimated locations of 1 km × 1 km NRFA river gauging stations (plus a CSV with NRFA IDs).

## Model and driving data
- Hydrological model: Grid-to-Grid (G2G), a national-scale, grid-based model that uses digital soil and land-cover data; accounts for urban/rural land-cover effects on runoff but not abstractions/discharges.
- Driving meteorology:
  - MaRIUS weather@home2 (WAH2) regional climate model dataset, using ensembles of historical and future climates.
  - Future scenarios based on the RCP8.5 pathway; multiple SST patterns, with bias-corrected precipitation and Penman-Monteith evaporation (PE).
  - PE calculations:
    - Historical: uses prescribed stomatal resistance values from MORECS.
    - Future: uses adjusted r_s to reflect CO₂ effects on stomatal conductance.
- Model inputs:
  - Precipitation and PE re-projected from ~25 km (0.22°) RCM grid to 1 km G2G grid; bias correction applied to precipitation only.
  - 360-day year with 30-day months; time stamps are days since 1900-01-01.
- Spin-up notes:
  - HISTBS first two years treated as spin-up; NF and FF also have spin-up years (2020–2021) before use.

## Temporal and spatial coverage
- Spatial domain: 700 km × 1000 km GB national grid (0,0 to 700000,1000000 m); grid cell centers used for data.
- Time-resolution: monthly means (30-day months) of daily values.
- Special considerations:
  - G2G does not include snow module; precipitation is treated as rain only.
  - Ensembles: avoid direct one-to-one comparisons between ensemble members across periods; compare distributions statistically.

## Data format and structure
- File format: NetCDF4
- File organization: one NetCDF per period and per ensemble member (e.g., G2G_WAH_var_HISTBS*.nc, G2G_WAH_var_BS*.nc, G2G_WAH_var_NF*.nc, G2G_WAH_var_FF*.nc).
- Data fields:
  - Flow: monthly mean river flow (m³ s⁻¹).
  - Soil: monthly mean soil moisture (mm water per m soil; depth-integrated).
- Coordinate and ancillary data:
  - NRFA station locations grid (MaRIUS_G2G_NRFAStationIDGrid.nc) with NRFA IDs.
  - Catchment area grid (MaRIUS_G2G_CatchmentAreaGrid.nc) in km².
  - CSV with NRFA station IDs for reference.
- Example outputs and figures illustrate flows, soil moisture, and gauge locations.

## How to use and compare
- Benchmarking:
  - Compare G2G-WAH2-monthly outputs to observational G2G runs (MaRIUS-G2G-Oudinmonthly) or to observed NRFA data, but only as statistical comparisons over long periods, not exact time-series matches.
  - For future periods (NF/FF), compare to Baseline (BS) rather than to observations.
  - Impacts models using NF/FF outputs should be compared to BS outputs, not to observed impacts.
- Ensemble interpretation:
  - Each ensemble member is a plausible realization of its period; compare distributions across ensembles rather than individual members.
  - Do not assume a direct one-to-one relationship between same-number ensemble members across different periods (e.g., BS1 should not be compared to NF1).
- Application scope:
  - Useful for national-scale drought and low-flow analyses, hydrological drought assessments, and hydrological impact modeling (e.g., ecological, agricultural, economic assessments).

## Related datasets and access
- Observational comparison data: MaRIUS-G2G-Oudinmonthly for observational-driven comparison.
- NRFA (National River Flow Archive) data for observed river flow benchmarks.
- Data hosted by NERC Environmental Information Data Centre (EIDC) with CEH documentation and datasets.

## Limitations and considerations
- G2G assumes natural flow regime and does not incorporate abstractions or discharges.
- Snow module not used; precipitation bias correction applied, but PE is not bias-corrected.
- 360-day calendar (months of 30 days) may affect interpretation of monthly values.
- Spatial discretisation may yield catchment-area discrepancies for small basins when mapping NRFA gauges to 1 km grid cells.
- Users should interpret results at the statistical level (differences between periods and ensemble distributions) rather than exact time-series replication.