# Methods The Concentration-Based Estimation of Deposition (CBED) methodology (Smith et al. 2000; Smith and Fowler 2001)

- Purpose and outputs
  - Generates 5x5 km resolution gridded estimates of deposition flux for nitrogen, sulfur, and base cations in the UK.
  - Combines observed gas/particle concentrations in air with ion concentrations in precipitation to map wet and dry deposition.

- Data sources and modeling approach
  - Observations from the UK Eutrophying and Acidifying Pollutants (UKEAP) network inform air concentrations and precipitation ions.
  - Wet deposition: uses precipitation data plus direct cloud droplet deposition to vegetation (occult deposition) for several species (e.g., sulfate, ammonium, nitrate, calcium, magnesium, hydrogen ion).
  - Dry deposition: applies land-cover-specific deposition velocities for five categories (forest, moorland, grassland, arable, urban) to derive deposition per grid square.
  - Specific pollutant components: NOx (via PCM), NHx (FRAME model plus UKEAP data), SOx (rural measurements with urban enhancement factor).
  - Anthropogenic vs. natural/seasalt separation for sulfur and calcium via sea-water ion ratios; includes orographic enhancement for upland regions.

- Temporal handling and uncertainty
  - Interpolation across a sparsely measured UK network introduces significant uncertainty; results are averaged over three-year periods to smooth inter-annual variability.
  - Earlier years (pre-1996) have higher uncertainty due to missing components (e.g., aerosols) and retrospective estimation based on long-term fractionings.
  - Long-term mean orographic factors are used in some cases rather than recalculating yearly; this contributes to numerical differences from earlier implementations.

- Implementation and reproducibility
  - Originally implemented in Genstat; re-implemented in R with small numerical differences (kriging interpolation and year-averaged factors).
  - Documentation and versioning practices align with QA standards and model inter-comparison exercises (e.g., Defra).

- Data products and structure
  - Three output CSV files (1986-2012) representing 3-year mean deposition per grid cell, weighted by land cover fractions or for specific land-cover assumptions:
    - rCBED_Fdep_gm2y_1986-2012_gridavg.csv
    - rCBED_Fdep_gm2y_1986-2012_forest.csv
    - rCBED_Fdep_gm2y_1986-2012_moor.csv
  - Grid and unit schema
    - Spatial: year (end-year of the 3-year period), easting, northing (OS Great Britain grid; centre of 5x5 km square)
    - Deposition components: H (hydrogen ions), NOx (oxidised nitrogen), NHx (reduced nitrogen), Ntot (total nitrogen), SOx (sulfur), xSOx (non-marine sulfur), Ca, Mg, CaMg (calcium+magnesium), Cl
    - Units: g m^-2 year^-1 (various components as listed)
  - Temporal scope: mean deposition for the period 1986-2012, covering current and two preceding years (e.g., 2012 represents 2010-2012)

- Quality control and governance
  - Extensive peer review and inclusion in Defra model inter-comparison exercises.
  - Clear documentation practices, version control, and centralized code storage.
  - Mass-balance checks and consistency comparisons with previous years.

- Data provenance, access, and metadata
  - Data exported from raster format to CSV with explicit field definitions and unit descriptions.
  - Accompanied by field-by-field metadata (names, units, descriptions) for reproducibility and audit trails.
  - Supporting information and network references available via provided URLs.

- Limitations and caveats
  - Uncertainty increases for years with sparse measurements and missing components (especially early period data).
  - Differences between the Genstat and R implementations due to interpolation methods and year-specific factor usage.
  - Some components estimated retrospectively, introducing additional uncertainty for pre-1996 data.

- References and context
  - Foundational publications and supporting references detailing methodology, uncertainty, and model components.