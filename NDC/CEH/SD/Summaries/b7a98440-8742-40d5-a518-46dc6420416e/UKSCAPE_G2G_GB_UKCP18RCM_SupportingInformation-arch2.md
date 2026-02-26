# Grid-to-Grid model estimates of river flow for Great Britain driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

- Purpose and scope
  - Provides Grid-to-Grid (G2G) hydrological model estimates of river flow for Great Britain, driven by UKCP18 Regional (12km) projections.
  - Part of UK-SCAPE WP2 research on climate-change impacts on water quantity, focusing on river flow via a high-resolution 1km grid.

- What is included
  - Monthly mean river flow (m3 s-1) on a 1km × 1km grid.
  - Annual maxima of daily mean river flow (m3 s-1) with dates of occurrence.
  - Annual minima of 7-day mean river flow (m3 s-1) with dates of occurrence.
  - Coverage: non-sea, non-tidal grid cells with catchment area ≥ 50 km2, across Great Britain ( GB domain 700 km × 1000 km).
  - Two supporting spatial datasets: digitally-derived catchment areas (1km grid) and estimated NRFA gauging-station locations (1km grid) with station info.

- Model and inputs
  - Hydrological model: Grid-to-Grid (G2G), a national-scale, grid-based model operating at ~1km resolution with a 15-minute time-step.
  - Driving meteorology: UKCP18 Regional (12km) projections, 12 ensemble members (perturbed parameter ensemble PPE).
  - Period and emissions: December 1980 to November 2080 under RCP8.5.
  - Data requirements: daily precipitation, daily min/max temperature, and daily potential evapotranspiration (PE).
  - Bias correction and downscaling:
    - Precipitation bias-corrected using monthly multiplicative factors.
    - PE derived via Penman-Monteith, aligned with MORECS methodology, with adjustments for CO2-driven stomatal closure.
    - 12km meteorological data downscaled to 1km using spatial weighting; daily PE downscaled to 1km; daily min/max temperatures downscaled with elevation-based lapse rates and daily sine-temporal shaping.
  - Calendar: 360-day year in model input (months of 30 days).

- Data format and structure
  - Output: NetCDF4 files, one file per ensemble member and per variable.
  - File naming:
    - Monthly mean flow: G2G_GB_mmflow_UKCP18RCM_ensnum_1980_2080.nc
    - Annual maxima: G2G_GB_amaxflow_UKCP18RCM_ensnum_1980_2080.nc
    - Annual minima: G2G_GB_aminflow_UKCP18RCM_ensnum_1980_2080.nc
  - Ensemble members: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15 (02, 03, 14 excluded).
  - Spatial domain: 700 km × 1000 km GB national grid; grid cell centers represent 1km × 1km cells.
  - Data coverage and limitations:
    - Values outside non-tidal river cells are set to missing (-9999).
    - Times and dates: monthly flows nominally assigned to the first day of each month; annual maxima/minima associated with specific water-year or December–November periods; dates of occurrence provided as days since 1900-01-01.
  - Supporting datasets:
    - CatchmentAreaGrid.nc (km2) for each 1km cell.
    - NRFAStationIDGrid.nc with gauging-station locations; NRFAStationIDs.csv provides station identifiers and notes.

- How to use the dataset (analyst-focused)
  - Historical comparison:
    - Compare G2G outputs driven by UKCP18 (12km) with those driven by observation-based inputs or observed river flow, but only via statistical multi-decadal comparisons (not point-by-point time series).
  - Baseline vs. future assessment:
    - Use the same ensemble member for baseline and future periods to assess climate-change impacts on flows.
  - Ensemble considerations:
    - Treat ensemble members as separate realizations; avoid cross-member mixing between periods.
  - Relation to observations:
    - Use NRFA-station grid to compare modeled flows to observed flows at corresponding locations, recognizing potential catchment discretisation differences, especially for smaller basins.
  - Context and comparability:
    - The future G2G outputs are analogous to MaRIUS-G2G-WAH2 products and should be interpreted within the same methodological framework.
  - Practical notes:
    - Direct point-by-point weather-flux equivalence is not expected between PPE-driven projections and observed weather; rely on long-term statistical analyses for interpretation.

- Accessibility and provenance
  - Dataset development supported by NERC UK-SCAPE programme (NE/R016429/1) under National Capability.
  - Related methodological references and prior datasets cited (e.g., Bell et al., Kay et al., Rudd et al., Guillod et al.) to contextualize model structure, calibration approach, and past applications.

- Limitations and caveats
  - Model performance is best for catchments with natural flow regimes; reduced fidelity where significant anthropogenic control or complex subsurface hydrology exists.
  - Discretisation to 1km grid can introduce catchment-area differences for smaller basins relative to observed NRFA catchments.
  - Calendar assumption (360-day year) and downscaling choices introduce temporal and spatial simplifications that should be accounted for in analyses.

- Acknowledgements
  - Acknowledges support from the Natural Environment Research Council and contributions from named researchers.

- References (selected context)
  - Foundational G2G methodological and application studies (Bell et al.; Kay et al.; Rudd et al.; Guillod et al.; Murphy et al.; Monteith; MORECS) used to develop, bias-correct, and downscale inputs and to interpret outputs.