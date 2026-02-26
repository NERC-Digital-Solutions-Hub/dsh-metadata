# Supporting information for Grid-to-Grid model estimates of monthly mean flow and soil moisture for Great Britain: weather@home2 (climate model) driving data [MaRIUS-G2G-WAH2-monthly]

## Overview
- Provides Grid-to-Grid (G2G) model estimates of monthly mean river flow and soil moisture for Great Britain on a 1 km x 1 km grid.
- Driven by weather@home2 (WAH2) climate-model data; part of the MaRIUS project (drought and water scarcity risk assessment).
- Time slices and ensembles:
  - Historical Baseline (HISTBS): 1900–2006
  - Baseline (BS): 1975–2004
  - Near-Future (NF): 2020–2049
  - Far-Future (FF): 2070–2099
  - Each slice has 100 ensemble members.
- Variables: flow (m3 s-1) and soil moisture (mm water per m soil), monthly means.
- Ancillary datasets: digitally-derived catchment areas and estimated NRFA gauging station locations on the 1 km grid.
- Format: NetCDF4; CEH grid conventions; separate file per period and ensemble member.

## Data model and hydrology
- Hydrological model: Grid-to-Grid (G2G) national-scale model for Britain, 1 km grid, 15-minute time-step; accounts for urban/suburban land-cover effects on runoff; calibrated with geopotential datasets rather than catchment-specific calibration.
- Input requirements: precipitation and potential evaporation (PE).
- Notable design choices:
  - Snow module not used here; precipitation treated as rain.
  - Uses spatially distributed parameters; calibration not performed per-catchment.
- Climate driving data: MaRIUS WAH2 RCM dataset; multiple ensembles, historical and future scenarios; future runs use RCP8.5.

## Data content and structure
- Grid and domain: 1 km x 1 km grid covering Great Britain; land grid boxes only; flows computed where rivers exist; sea cells set to missing.
- Temporal structure:
  - 30-day months (360-day calendar in climate input).
  - Spin-up periods to be ignored in analyses:
    - HISTBS first two years
    - NF and FF first two years
- Files and naming:
  - Historical Baseline: G2G_WAH_var_HISTBS*.nc
  - Baseline: G2G_WAH_var_BS*.nc
  - Near-Future: G2G_WAH_var_NF*.nc
  - Far-Future: G2G_WAH_var_FF*.nc
  - Variables: flow or soil
- Outputs:
  - Flow: monthly averages of daily mean natural flow (m3 s-1)
  - Soil moisture: monthly averages of daily mean soil moisture (mm water per m soil) or depth-integrated θ (0–1 depth-integrated)
- Ancillary spatial data:
  - Catchment area per 1 km grid cell (MaRIUS_G2G_CatchmentAreaGrid.nc)
  - NRFA gauging station locations on the 1 km grid (MaRIUS_G2G_NRFAStationIDGrid.nc) and station IDs file (MaRIUS_NRFAStationIDs.csv)

## Data inputs and processing
- Meteorological drivers: precipitation and PE from MaRIUS WAH2; data re-projected from ~0.22° grid to 1 km; precipitation distributed within each box using standard weights.
- Precipitation bias correction: monthly multiplicative bias-correction applied to precipitation (per Guillod et al. 2018).
- Potential Evaporation (PE):
  - Derived via Penman-Monteith using related variables.
  - Historical r_s values from MORECS used for the historical baseline; future PE uses PE versions with stomatal resistance adjusted for CO2 effects.
  - PE for future periods uses adjusted r_s values; not bias-corrected, as per Guillod et al. 2018.
- Data alignment: all meteorological inputs re-projected to the 1 km G2G grid; land-only grid cells used for outputs.

## Usage guidance and caveats
- Comparisons:
  - Baseline (BS) vs future (NF/FF) should be statistical comparisons of distributions, not direct time-series matches to observations.
  - Comparisons to observation-driven G2G runs or NRFA data are statistical; do not expect exact time-series equivalence.
  - Do not compare individual ensemble members across periods (e.g., BS1 with NF1); ensemble members are independent realizations.
- Spin-up considerations: first two years of HISTBS and NF/FF should be treated as spin-up and not used for primary analyses.
- Spatial mapping caveats:
  - NRFA gauging locations are mapped to the closest 1 km grid cell; some small catchments may have imperfect catchment-area alignment due to grid discretisation.
- Data interpretation:
  - Soil moisture values are depth-integrated across the soil column; site- and soil-property variability are spatially represented but not calibrated per-catchment.
- Documentation and references: extensive methodological references provided; dataset adheres to CEH conventions and includes provenance and acknowledgments.

## provenance, governance, and access
- Source project: MaRIUS (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity), UK NERC-funded.
- Data governance: clearly documented dataset with versioned NetCDF4 files and accompanying spatial datasets; metadata follows CEH conventions; multiple references cited for model components and methods.
- Access and citation: dataset hosted by NERC Environmental Information Data Centre; accompanying documentation includes usage notes, caveats, and references.

## References and acknowledgments
- Key methodological and model references include Bell et al. (2007, 2009, 2016), Davies & Bell (2009), Guillod et al. (2018), Hough & Jones (1997), Kay et al. (2018), Monteith (1965), Rudd et al. (2017, in prep), among others.
- Acknowledgments to contributors for data provision and assistance.