# Methods

- The Concentration Based Estimated Deposition (CBED) methodology creates 5x5 km resolution maps of wet and dry deposition for sulphur, oxidised and reduced nitrogen, and base cations using measured air concentrations of gases/particulates and precipitation ion concentrations from the UK Eutrophying and Acidifying Pollutants (UKEAP) network.

- Data flow and inputs
  - Site measurements are interpolated to generate UK-wide concentration maps.
  - Wet deposition is derived by combining precipitation concentrations with an annual UK precipitation map and includes direct deposition of cloud droplets (occult deposition).
  - Dry deposition uses gas and particulate concentration maps together with habitat-specific deposition velocities to produce deposition for five land cover categories: forest, moorland, grassland, arable, and urban.
  - Deposition to non-woodland habitats uses moorland values; deposition to woodland habitats uses forest values.

- Species-specific approaches
  - SO2 concentration for dry deposition is estimated from rural measurements with an urban enhancement factor.
  - Oxidised nitrogen dry deposition:
    - Nitric acid concentrations are interpolated from ~30 sites.
    - NO2 concentrations come from the Pollution Concentration Mapping (PCM) model (combining rural measurements with point/line source modelling).
  - Ammonia concentrations combine outputs from the FRAME atmospheric transport model and annual UKEAP measurements to capture local variability.

- Wet deposition details
  - Includes both wet precipitation deposition and occult deposition on vegetation.
  - Anthropogenic versus total sulphur and calcium are separated using sea-water sodium (Na) ratios.
  - Orographic enhancement is applied to precipitation in upland regions using an observation-based factor from Great Dun Fell and Holme Moss studies.

- Temporal aspects and smoothing
  - Inter-annual variations due to weather and atmospheric processes exist; to address this, CBED deposition estimates are averaged over a three-year period.
  - Calculations are annual but provided as rolling 3-year means.

- Outputs and ecosystem options
  - Produces two ecosystem-specific datasets:
    - Moorland/short vegetation everywhere
    - Forest everywhere
  - Also provides grid-average values, all as 3-year rolling means.

- Data units and conversions
  - All deposition values are expressed as keq ha^-1 year^-1.
  - Conversions to kg S ha^-1 year^-1 or kg N ha^-1 year^-1:
    - Sulphur: keq × 16
    - Oxidised/reduced nitrogen: keq × 14
    - Combined base cations (Ca+Mg): keq × 20 (as calcium equivalents)

- Quality control and validation
  - Methods align with government QA standards for analytical models and have undergone peer review and participation in Defra model inter-comparisons.
  - Documentation, version control, and central storage of code are maintained.
  - CBED results are widely published; method developments are approved by senior officers.
  - Mass balance checks are routinely performed to ensure numerical consistency and comparability with previous years.

- Data structure and fields
  - Outputs are organized as 3-year mean data for each grid square, with fields for:
    - easting and northing (centre of 5x5 km square)
    - deposition to forest (nox_f, nhx_f, nms_f, nm_ca_mg_f)
    - deposition to moorland (nox_m, nhx_m, nms_m, nm_ca_mg_m)
    - grid-average deposition (nox_ga, nhx_ga, nms_ga, nm_ca_mg_ga)
  - Each set includes species-specific deposition values (oxidised nitrogen, reduced nitrogen, non-marine sulphur, non-marine base cations) in keq ha^-1 yr^-1.