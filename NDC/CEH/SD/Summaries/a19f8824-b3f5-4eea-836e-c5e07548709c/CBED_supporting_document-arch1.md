# Methods

- Purpose and scope
  - CBED (Concentration Based Estimated Deposition) produces 5x5 km gridded deposition data for wet and dry deposition of sulphur, oxidised nitrogen, reduced nitrogen, and base cations.
  - Based on measured concentrations of gases/particulate matter in air and ions in precipitation from the UK Eutrophying and Acidifying Pollutants network (UKEAP).
  - Used for assessing critical loads and informing environmental decision-making.

- Data inputs and spatial mapping
  - Site measurements interpolated to generate UK concentration maps.
  - Wet deposition: combine ion precipitation concentrations with annual precipitation maps; includes direct cloud (occult) deposition to vegetation; accounts for orographic enhancement in upland regions.
  - Dry deposition: use gas/PM concentration maps and habitat-specific deposition velocities; applied to five land cover categories (forest, moorland, grassland, arable, urban).
  - For critical loads, moorland deposition is applied to all non-woodland habitats and forest deposition to all woodland habitats.

- Temporal framing
  - Calculations are annual but are provided as rolling 3-year means to smooth inter-annual variability.
  - Data are ecosystem-specific with two primary setups: moorland everywhere and forest everywhere, plus grid-average values.

- Process for oxidised/reduced nitrogen, sulphur, and base cations
  - Oxidised nitrogen (NO2/NO3) and reduced nitrogen (NH3/NH4) deposition modeled with site measurements plus interpolations/model inputs (e.g., PCM for NO2, FRAME for NH3).
  - Sulphur (non-marine) deposited as SO2/SO4 components; separation of anthropogenic vs total sulphur/calcium based on sea-salt ion ratios.
  - Wet deposition includes sulphate, ammonium, nitrate, calcium, magnesium, and acidity (hydrogen ion).

- Time-averaged data and ecosystem-specific sets
  - 3-year means provided for each grid square and ecosystem scenario (moorland vs forest) and a grid-average mean.

- Data structure and file formats
  - Three 2015–2017 CBED data files:
    - CBED-deposition-moorland-2015-2017.csv: easting, northing, nox_m, nhx_m, nms_m, nm_ca_mg_m.
    - CBED-deposition-forest-2015-2017.csv: easting, northing, nox_f, nhx_f, nms_f, nm_ca_mg_f.
    - CBED-deposition-gridaverage-2015-2017.csv: easting, northing, nox_ga, nhx_ga, nms_ga, nm_ca_mg_ga.
  - Units: keq ha-1 year-1; conversion to kg ha-1 year-1 via multipliers:
    - S: keq × 16 = kg S ha-1 year-1
    - N (oxidised/reduced): keq × 14 = kg N ha-1 year-1
    - Base cations (Ca+Mg): keq × 20 = kg Ca ha-1 year-1
  - Location coordinates: centre of each 5x5 km grid square (easting/northing in metres).

- Quality control and documentation
  - Adheres to quality assurance practices aligned with government analytical model review.
  - Extensive peer review and participation in Defra model inter-comparison exercises.
  - Versioned code management, thorough method documentation, and mass-balance checks against prior years.
  - Results published in peer-reviewed literature; method developments overseen by senior responsible officers.

- Access and supporting information
  - Data and supporting information available via specified URLs (UK pollutant deposition resources and DEFRA/UK-AIR portals).

- Practical notes for analysts
  - Data are designed to support analyses of deposition impacts at local to regional scales, with explicit habitat-specific deposition assumptions and rolling 3-year summaries to reduce year-to-year noise.
  - The grid-average and ecosystem-specific outputs enable flexible aggregation and comparison across land-cover types and spatial scales.