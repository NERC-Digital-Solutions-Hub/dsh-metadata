# The Concentration-Based Estimation of Deposition (CBED) methodology

- Purpose and scope
  - Generates 5×5 km resolution gridded estimates of deposition flux for nitrogen, sulphur, and base cations.
  - Uses observed gas/PM concentrations in air and ion concentrations in precipitation from the UK Eutrophying and Acidifying Pollutants (UKEAP) network.
  - Produces both wet and dry deposition estimates; dry deposition uses land-cover–specific deposition velocities across five land-cover categories (forest, moorland, grassland, arable, urban).

- Data inputs and sources
  - Gas/PM concentration maps in air; ion concentrations in precipitation.
  - Wet deposition: precipitation flux plus occult deposition (direct deposition of cloud droplets) to vegetation.
  - Dry deposition: deposition velocities by land cover; components include SO2, HNO3, NO2, NH3, and PM (sulphate, nitrate, ammonium, Ca, Mg).

- Key components and methods
  - NO2: Pollution Concentration Mapping (PCM) model
  - Ammonia: FRAME model plus UKEAP measurements for local variability
  - SO2: rural measurements with urban enhancement factor
  - Anthropogenic vs total sulphur and calcium distinguished via sea-salt ratios
  - Orographic enhancement: seeder–feeder effect incorporated for upland regions
  - Interannual variability: values averaged over a three-year period to reduce weather-variability noise

- Uncertainty and limitations
  - Substantial uncertainty from sparse observation networks and natural annual variability.
  - Early years (pre-1996) have higher uncertainty due to incomplete aerosol measurements; retrospective estimates rely on long-term fractions.
  - Differences between the original Genstat implementation and the current R version (kriging interpolation and use of long-term means) introduce small numerical differences.

- Modeling implementation and quality control
  - Originally implemented in Genstat; re-implemented in R.
  - Subject to extensive peer review; included in Defra model inter-comparison exercises.
  - Mass-balance checks and version control procedures ensure numerical consistency and documentation.

- Data structure and outputs
  - Outputs stored as three CSV files exporting raster data to xyz format:
    - rCBED_Fdep_gm2y_1986-2012_gridavg.csv (mean deposition weighted by land cover fractions)
    - rCBED_Fdep_gm2y_1986-2012_forest.csv (deposition to forest assuming full forest cover)
    - rCBED_Fdep_gm2y_1986-2012_moor.csv (deposition to moorland assuming full moorland cover)
  - Each file uses the same format:
    - Year (end-year of 3-year mean), easting, northing, and deposition fluxes for H, NOx, NHx, Ntot, SOx, xSOx, Ca, Mg, CaMg, Cl
  - Units: deposition fluxes in g m-2 year-1
  - Spatial reference: centre of 5×5 km OS Great Britain grid

- Data coverage and time period
  - Deposition estimates available for 1986–2012 (three-year means for current and two preceding years)

- Data accessibility and governance
  - Emphasizes the need for data to be available and openly shared to support monitoring and decision-making.
  - Metadata and documentation accompany datasets; data handling aligned with quality assurance standards.

- Relevance for monitoring frameworks
  - Provides a robust, multi-source approach to quantify deposition pressures on ecosystems across the UK.
  - Delivers spatially explicit deposition maps and land-cover–specific estimates useful for policy evaluation, trend analysis, and informing future decisions.
  - Highlights challenges in data availability, interoperability, and governance that monitoring bodies must plan for (e.g., data silos, metadata quality, data sharing barriers).