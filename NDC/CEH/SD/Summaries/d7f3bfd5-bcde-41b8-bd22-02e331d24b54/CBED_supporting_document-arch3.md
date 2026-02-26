# Concentration Based Estimated Deposition (CBED) methodology

- Produces 5x5 km resolution maps of wet and dry deposition of sulphur, oxidised and reduced nitrogen, and base cations from measured air concentrations and precipitation ion concentrations within the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
- Spatially interpolates site measurements to UK-wide concentration maps and combines them with precipitation and habitat-specific deposition velocities to derive grid-square deposition values.
- Distinguishes dry deposition of gases (SO2, HNO3, NO2, NH3) and particulate matter to vegetation; wet deposition includes direct and occult (cloud) deposition to vegetation for multiple ions.

- Wet deposition components and separation:
  - Wet deposition includes precipitation deposition plus occult deposition to vegetation (for sulphate, ammonium, nitrate, calcium, magnesium, and acidity).
  - Anthropogenic vs total sulphur and calcium components are separated using sea-water ion ratios.
  - Orographic enhancement is applied to precipitation concentration in upland regions (seeder-feeder effect).

- Temporal and regional aggregation:
  - Calculations are annual but provided as rolling 3-year means to smooth inter-annual variability.
  - Outputs include ecosystem-specific values under two assumptions: moorland/short vegetation everywhere and forest everywhere, plus grid-averaged deposition.

- Land cover and deposition targets:
  - Deposition to five land cover categories: forest, moorland, grassland, arable, and urban.
  - For critical loads exceedance, deposition values for moorland are applied to all non-woodland habitats, and forest values are applied to woodland habitats.

- Data sources and modelling components:
  - Gas and PM concentrations from the UKEAP network; NO2 and NOx derived from PCM model data; ammonia from FRAME model and UKEAP measurements.
  - SO2 concentrations from rural measurements with an urban enhancement factor; ammonia provides local scale variability beyond network measurements.
  - UK Met Office precipitation maps provide wet deposition inputs.

- Data structure and fields:
  - 3-year mean deposition data organized by grid square with fields for each habitat category.
  - Example fields include:
    - For forest: nox_f (oxidised nitrogen), nhx_f (reduced nitrogen), nms_f (non-marine sulphur), nm_ca_mg_f (non-marine base cations)
    - For moorland: nox_m, nhx_m, nms_m, nm_ca_mg_m
    - Grid average: nox_ga, nhx_ga, nms_ga, nm_ca_mg_ga
  - Each value is reported in keq ha-1 year-1.

- Units and conversion factors:
  - All deposition values expressed as keq ha-1 year-1.
  - Conversions to kg ha-1 year-1:
    - Oxidised/reduced nitrogen: keq ha-1 year-1 × 14 = kg N ha-1 year-1
    - Sulphur: keq ha-1 year-1 × 16 = kg S ha-1 year-1
    - Base cations (Ca+Mg): keq ha-1 year-1 × 20 = kg Ca ha-1 year-1

- Quality assurance and governance:
  - CBED methods have undergone extensive peer review and participated in Defra model inter-comparison exercises.
  - Version control, central storage of code, and documentation of method developments.
  - Mass balance checks and comparisons to prior years to ensure numerical consistency.
  - Outputs published in peer-reviewed literature; methodology overseen by senior responsible officers.

- Data accessibility and use for policy:
  - Outputs are designed to support monitoring environmental health, evaluating policy, and informing future decisions.
  - Documentation includes data structure, unit conversions, and methodological details to support transparency and data governance.