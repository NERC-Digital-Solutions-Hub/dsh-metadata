# Supporting information for Grid-to-Grid model estimates of river flow for Great Britain driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

## Purpose and scope
- Provides Grid-to-Grid (G2G) hydrological model estimates of monthly mean river flow, and annual maxima/minima, for Great Britain on a 1km × 1km grid.
- Driven by UKCP18 Regional (12km) climate projections for December 1980 to November 2080 under RCP8.5.
- Outputs cover non-tidal rivers with catchment areas ≥50 km²; enables assessment of climate-change impacts on river flows and supports comparison with observation-based inputs.

## Model and approach (G2G)
- G2G is a national-scale, grid-based hydrological model running on a 1km grid with a 15-minute time-step to produce spatially consistent river-flow estimates for gauged and ungauged rivers.
- Calibrations are not performed for individual catchments; uses nationally applicable parameter values. Urban/suburban land cover effects are incorporated.
- Model performance: best for natural flow regimes; less accurate where artificial abstractions/discharges or complex subsurface hydrology prevail.
- Required inputs: precipitation, potential evapotranspiration (PE), daily min/max air temperatures (optional snow module).

## Input data and processing
- Meteorological inputs: daily precipitation, daily min/max temperature, daily PE (derived from meteorological variables); sourced from UKCP18 Regional (12km) PPE ensemble (12 members) for 1980–2080 under RCP8.5.
- Bias correction and downscaling:
  - Precipitation bias-corrected using monthly multiplicative factors.
  - PE computed with Penman-Monteith, aligned with MORECS methodology adjustments (to account for stomatal resistance changes over time).
  - 12km inputs downscaled to 1km via spatial weighting; daily PE copied to 1km grid; temperature downscaled with elevation-based lapse rate and diurnal sine-based temporal downscaling.
- Calendar and timing: dataset uses 30-day months and a 360-day calendar; time stamps are days since 1900-01-01; monthly flows nominally assigned to the first day of the month; annual maxima/minima assigned to the start year of the 12-month (water or Dec–Nov) period; dates of occurrence provided as additional variables.

## Outputs and formats
- Variables provided per 1km grid cell (non-tidal, catchment area ≥50 km²):
  - Monthly mean river flow (m³ s⁻¹)
  - Annual maxima of daily mean river flow (m³ s⁻¹)
  - Annual minima of 7-day mean river flow (m³ s⁻¹)
  - Dates of occurrence for the annual maxima and minima
- Ensemble structure: 12 PPE-driven members (01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15) corresponding to driving GCM PPE members.
- File format and naming:
  - NetCDF4 files per ensemble member and variable, following CEH conventions.
  - Examples:
    - G2G_GB_mmflow_UKCP18RCM_ensnum_1980_2080.nc
    - G2G_GB_amaxflow_UKCP18RCM_ensnum_1980_2080.nc
    - G2G_GB_aminflow_UKCP18RCM_ensnum_1980_2080.nc
  - Domain: 700 km × 1000 km GB grid; grid cell centers define coordinates; missing data (-9999) for cells with <50 km² catchment or non-river cells.
  - Time representation: 30-day months; days since 1900-01-01 timestamps; annual events tied to start year (e.g., 1981 for 1981–1982 period).
- Supporting datasets:
  - Catchment area grid (km²) draining to each 1km cell
  - NRFA station location grid with corresponding NRFA station IDs (and a CSV with station information)
  - These aid comparison with observed river flows and interpretation of spatial patterns

## Data quality, limitations, and considerations for monitoring
- Calibration: not tailored to individual catchments; uses nationally consistent parameters, which supports comparability across the UK but may limit accuracy in highly managed or heterogeneous basins.
- Uncertainties and performance caveats:
  - Greater uncertainty in areas with artificial water management or complex subsurface hydrology.
  - Small catchments may be more sensitive to discretisation effects on a 1km grid, affecting catchment area representations.
  - Bias correction and downscaling introduce additional uncertainty; the 360-day calendar and 30-day months differ from standard calendars, which can affect timing interpretation.
- Comparisons and usage guidance:
  - For historical periods, compare G2G outputs with observation-based inputs or observed river flows statistically (multi-decadal) rather than point-by-point time series alignment.
  - When comparing ensemble members across periods, use the same ensemble member to maintain consistency (e.g., baseline vs future).
  - Outputs are designed to inform climate-change impact assessments on river flows and hydrological extremes, and to support scenario analyses alongside other UK-SCAPE datasets (e.g., MaRIUS).
- Metadata and data governance:
  - Documentation includes methodology for bias correction, downscaling, and data structure; data provenance is anchored to UKCP18 and CEH conventions.
  - The dataset is part of the UK-SCAPE program and supported by NERC, emphasizing open data practices and scientific transparency, but users should note any implicit assumptions (e.g., non-calibrated parameters, 360-day calendar).

## Practical implications for monitoring frameworks
- Strengths for policy monitoring:
  - High spatial resolution (1km) enables fine-scale risk assessment and regional planning.
  - Ensemble structure provides uncertainty bounds for monitoring of river-flow-related indicators under climate change.
  - Time-series data can support trend analysis, drought/flood risk assessment, and evaluation of adaptation measures.
- Gaps and considerations:
  - Requires careful handling of timing and calendar conventions when aligning with other datasets.
  - Downscaling and bias-correction steps introduce uncertainties that should be characterized in monitoring reports.
  - Spatial misalignment with NRFA catchment delineations may affect comparisons for small basins; use the provided NRFA station grid for best-match comparisons.

## Acknowledgements and references
- Funded by the Natural Environment Research Council (award NE/R016429/1) as part of the UK-SCAPE National Capability.
- Acknowledges contributions from researchers and partner institutions; cites methodological and supporting literature outlining G2G development, bias correction, and prior MaRIUS work.