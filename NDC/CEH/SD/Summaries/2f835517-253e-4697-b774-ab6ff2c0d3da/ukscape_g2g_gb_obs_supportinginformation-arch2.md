# Supporting information for Grid-to-Grid model estimates of river flow for Great Britain driven by observed data (1980 to 2011)

- UK-SCAPE program context: Five-year programme funded by NERC; Work Package 2 investigates climate-change impacts on water quantity, providing Grid-to-Grid (G2G) hydrological model estimates of river flow across Britain on a 1 km grid.

- What the dataset provides:
  - Grid-to-Grid model estimates of river flow driven by observed meteorological data (1980–2011) for Great Britain.
  - Monthly mean river flow (m3 s-1) on a 1 km grid.
  - Annual maxima of daily mean river flow (m3 s-1).
  - Annual minima of 7-day mean river flow (m3 s-1).
  - Spatially continuous, natural-flow estimates for gauged and ungauged rivers; includes non-tidal river cells with catchment area ≥ 50 km².

- Model description (Grid-to-Grid, G2G):
  - National-scale hydrological model running on a 1 km grid with a 15-minute time-step.
  - Outputs natural river flows; largely parameterized with nationally applicable values rather than catchment-specific calibration.
  - Accounts for urban/suburban land-cover effects on runoff and downstream flows.
  - Calibrated performance: strong for natural-flow regimes; weaker where artificial abstractions, discharges, or complex subsurface hydrology dominate.

- Input data and downscaling:
  - Precipitation: daily 1 km CEH-GEAR dataset.
  - Potential evaporation (PE): monthly 40 km MORECS dataset.
  - Temperature: daily 1 km HadUK-Grid (Met Office HadCAMS) data; temperature downscaled within the day using a sine function to daily resolution.
  - Spatial data (topography, soils) as per Bell et al. 2009.

- Time and spatial coverage:
  - Domain: 700 km × 1000 km GB National Grid (0–700000, 0–1000000 metres); 1 km grid cells.
  - River cells with catchment area ≥ 50 km²; non-river or smaller catchments set to missing (-9999).
  - Time reference: days since 1900-01-01; monthly means assigned to the first day of each month; annual maxima assigned to the start of the 12-month period (water year Oct 1981–Sep 1982 for 1981; etc.); annual minima assigned to Dec of the start year (Dec 1981–Nov 1982 for 1981).

- Output formats and accompanying data:
  - NetCDF4 files, one per variable:
    - G2G_GB_mmflow_obs_1980_2011.nc: monthly mean river flow (1980–2011, Dec 1980–Nov 2011).
    - G2G_GB_amaxflow_obs_1980_2011.nc: annual maxima of daily mean river flow (Oct 1981–Sep 2011).
    - G2G_GB_aminflow_obs_1980_2011.nc: annual minima of 7-day mean river flow (Dec 1980–Nov 2011).
  - Grid cell details: values provided for non-tidal river cells with catchment area ≥ 50 km²; missing elsewhere.
  - Time stamp: days since 1900-01-01; monthly values anchored to first day of month.

- Supporting spatial datasets:
  - CatchmentAreaGrid (UKSCAPE_G2G_GB_CatchmentAreaGrid.nc): catchment area (km²) draining to each 1 km grid cell.
  - NRFAStationGrid (UKSCAPE_GB_NRFAStationIDGrid.nc) and NRFAStationIDs.csv: estimated locations of NRFA gauging stations aligned to 1 km grid cells; used to compare G2G outputs with observed NRFA river flows.
  - Notes: minor discrepancies can occur where derived catchments differ from observed NRFA catchments, especially for small rivers.

- How to use the data:
  - Compare G2G outputs to observed NRFA river flows to assess model performance for historical context.
  - Combine with UKCP18 regional climate projections for scenario analyses (datasets available alongside).
  - Use alongside MaRIUS-G2G-MORECS-monthly outputs (1980–2011) with noted differences (period, land-sea mask, discretisation).

- Key caveats and considerations:
  - G2G relies on globally applicable parameters rather than catchment-specific calibration; performance varies with regime naturalness and data quality.
  - Potential mismatches between G2G-derived catchment areas and NRFA catchments, particularly for small catchments due to 1 km discretisation.
  - Some outputs are best interpreted in aggregate across the domain rather than at highly disaggregated local scales.

- Acknowledgements and references:
  - Funded by NERC award NE/R016429/1 under the UK-SCAPE National Capability programme.
  - Acknowledgement of contributions from specified researchers; key references include Bell et al. 2009, 2016, 2018; Rudd et al. 2017; Davies & Bell 2009; Formetta et al. 2018; Tanguy et al. 2016; Met Office HadUK-Grid data.

- Access and provenance:
  - Dataset produced as part of UK-SCAPE; associated DOI and links provided for access and traceability.