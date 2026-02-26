# Methods

- Purpose and scope
  - Describes the Concentration Based Estimated Deposition (CBED) methodology that creates 5x5 km gridded data for wet and dry deposition of sulphur, oxidised and reduced nitrogen, and base cations.
  - Data derived from measured gas/particulate concentrations in air and ion concentrations in precipitation, collected via the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
  - Deposition values are used to assess critical load exceedances and are provided as rolling 3-year means.

- Data sources and aggregation
  - Site measurements are interpolated to generate UK-wide concentration maps.
  - Wet deposition: combines precipitation ion concentrations with an annual precipitation map; includes direct cloud deposition (occult) and an urban enhancement factor for SO2.
  - Dry deposition: uses concentration maps plus habitat-specific deposition velocities to produce deposition for five land-cover categories (forest, moorland, grassland, arable, urban); grid-square values are produced by weighting these by land-cover proportions.

- Deposition components and species
  - Dry deposition includes SO2, HNO3, NO2, NH3, and PM constituents (sulfate, nitrate, ammonium, Ca, Mg) to vegetation.
  - Moorland deposition applied to non-woodland habitats; forest deposition applied to woodland habitats for critical loads.

- Calculation specifics
  - SO2 concentrations derived from rural measurements with an urban enhancement factor.
  - Oxidised nitrogen dry deposition based on interpolated nitric acid and NO2 from PCM model data.
  - Ammonia concentrations from FRAME model plus annual UKEAP measurements.
  - Wet deposition accounts for sea-salt separation of S and Ca, and includes an orographic enhancement factor in upland areas (e.g., Pennine observations).

- Temporal considerations
  - Inter-annual variability acknowledged; CBED deposition data are averaged over a three-year period to smooth fluctuations.
  - Data are annual but presented as rolling 3-year means; ecosystem-specific outputs include moorland-only, forest-only, and grid-average scenarios.

- Data structure and contents
  - Three ecosystem-specific data files for 2014–2016:
    - CBED-deposition-moorland-2014-2016.csv: moorland deposition values
    - CBED-deposition-forest-2014-2016.csv: forest deposition values
    - CBED-deposition-gridaverage-2014-2016.csv: grid-average deposition values
  - Common structure in each file:
    - easting and northing: centre coordinates of each 5x5 km grid square (metres, OS Great Britain grid)
    - deposition fields for each species, with suffixes indicating the ecosystem:
      - moorland: nox_m, nhx_m, nms_m, nm_ca_mg_m
      - forest: nox_f, nhx_f, nms_f, nm_ca_mg_f
      - grid average: nox_ga, nhx_ga, nms_ga, nm_ca_mg_ga
  - Units: all deposition values are keq ha-1 year-1
  - Data can be converted to kg units using:
    - S deposition: keq ha-1 year-1 × 16 = kg S ha-1 year-1
    - N deposition: keq ha-1 year-1 × 14 = kg N ha-1 year-1
    - Base cations (Ca+Mg): keq ha-1 year-1 × 20 = kg Ca ha-1 year-1

- Quality control and documentation
  - Methods align with government QA for analytical models; extensive peer review and participation in Defra model inter-comparison exercises.
  - Version control, centralized code storage, and documentation of method developments.
  - Mass-balance checks and comparisons to previous years to ensure numerical consistency.
  - Results are published in peer-reviewed literature; method developments overseen by senior responsible officers.

- Access and references
  - Resource links provided for the UK Eutrophying and Acidifying Atmospheric Pollutants (UKEAP) and related networks.
  - Supporting information and fieldwork/lab instrumentation notes indicate no additional external data requirements beyond described measurements and models.