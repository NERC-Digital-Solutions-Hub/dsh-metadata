# Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

- Purpose and context
  - Maps deposition and concentrations to UK protected sites (SAC, SPA, SSSI) using 1x1 km gridded data.
  - Integrates CBED deposition outputs (nitrogen, sulfur compounds) with PCM-derived pollutant concentrations to support assessments of deposition relative to protected sites.
  - Produces 3-year rolling means (2018–2020) to smooth inter-annual variability and provides ecosystem-specific and grid-average scenarios.

- Data sources and boundaries
  - CBED model outputs: wet and dry deposition for S, N species, and base cations, derived from gas/PM concentrations and precipitation, with habitat-specific deposition velocities.
  - PCM model outputs: background concentrations on a 1x1 km grid for NOx, NO2, SO2, NH3, PM, etc., including representative road-side values; used for scenario planning and TEN applications.
  - UK protected site boundaries: SAC, SPA, and SSSI/ASSI boundaries downloaded from respective national sources.
  - Site area overlap: 1x1 km grid squares clipped to protected site boundaries; gridSquare area and site area used to compute site-relevant values.

- Step 1: Spatial data processing
  - Create a 1x1 km UK grid and clip to protected site boundaries to form a gridded dataset for all SAC, SPA and SSSI sites.
  - Merge gridded UK CBED deposition data (2018–2020 3-year mean) with the clipped grid to generate a UK protected sites CBED dataset.
  - Repeat the process for 1x1 km concentration datasets for NOx and SO2 (PCM-based).

- Step 2: Deriving minimum, maximum, and grid-average values
  - Use SQL on the gridded dataset to calculate per-site minimum, maximum, and grid-average deposition/concentration values.
  - Grid-average calculation: grid-area-weighted deposition value for each grid cell within a site, summed across the site.
  - Equation (conceptual): site CBED deposition value × (grid area / total site area), summed across grid cells overlapping the site.
  - Outputs support exposure and ecosystem-impact assessments under different habitat assumptions.

- CBED modelling details
  - Produces 1x1 km resolution maps of wet and dry deposition for S, N, and base cations from measured air concentrations and precipitation-derived inputs.
  - Wet deposition: precipitation concentrations plus occult deposition; non-marine/sea-salt fraction distinguished via ion ratios.
  - Dry deposition: deposition velocities across five land-cover categories (forest, moorland, grassland, arable, urban) applied to gas/PM species; grid-square deposition weighted by habitat proportions.
  - Ecosystem-specific deposition: separate values for moorland vs forest; critical-load comparisons use moorland values for non-woodland habitats and forest values for woodland habitats.
  - Inter-annual variability: deposition values averaged over three years to smooth fluctuations.

- PCM modelling details
  - Builds background concentration maps on a 1x1 km grid for multiple pollutants; includes base-year and projection models per pollutant.
  - Supports scenario assessment, population exposure calculations, and policy development; used for TEN-related model runs.
  - Outputs include thousands of road-side values and grid-average values used in site-level analyses.

- Data outputs and file structure (12 primary files)
  - File 1: Forest deposition by grid, 2018–2020, 3-year mean (NH3/NH4_FOREST, NO2_NO3_FOREST, SO2_SO4_NM_FOREST, CA_MG_NM_FOREST)
  - File 2: Moorland deposition by grid, 2018–2020 (NH3_NH4_MOORLAND, NO2_NO3_MOORLAND, SO2_SO4_NM_MOORLAND, CA_MG_NM_MOORLAND)
  - File 3: Grid-average deposition by site, 2018–2020 (NH3_NH4_GRIDAVERAGE, NO2_NO3_GRIDAVERAGE, SO2_SO4_NM_GRIDAVERAGE, CA_MG_NM_GRIDAVERAGE)
  - File 4: Ammonia concentration by grid, 2018–2020 (NH3_CONC)
  - File 5: Nitrogen oxides concentration by grid, 2018–2020 (NO2_CONC)
  - File 6: Sulphur dioxide concentration by grid, 2018–2020 (SO2_CONC)
  - File 7: Minimum/Maximum/Average forest deposition values (NO2_NO3_FOREST, NH3_NH4_FOREST, SO2_SO4_NM_FOREST, CA_MG_NM_FOREST)
  - File 8: Minimum/Maximum/Average moorland deposition values (NO2_NO3_MOORLAND, NH3_NH4_MOORLAND, SO2_SO4_NM_MOORLAND, CA_MG_NM_MOORLAND)
  - File 9: Minimum/Maximum/Average grid-average deposition values (NO2_NO3_GRIDAVERAGE, NH3_NH4_GRIDAVERAGE, SO2_SO4_NM_GRIDAVERAGE, CA_MG_NM_GRIDAVERAGE)
  - File 10: Ammonia concentration by site (MIN_NH3_CONC, AVG_NH3_CONC, MAX_NH3_CONC)
  - File 11: NOx concentration by site (MIN_NO2_CONC, AVG_NO2_CONC, MAX_NO2_CONC)
  - File 12: SO2 concentration by site (MIN_SO2_CONC, AVG_SO2_CONC, MAX_SO2_CONC)
  - Each file includes site-level metadata: SITECODE, SITENAME, SITEAREA, CENTROID_X, CENTROID_Y, COUNTRY, DESIGNATION, YEAR, plus the respective deposition/concentration metrics.

- Metadata, units, and data governance
  - Nature and units
    - Deposition values: keq ha-1 year-1 (S and N species, forest, moorland, grid-average, and minimum/maximum/average values).
    - Concentrations: micrograms per cubic metre (µg m-3) for NH3, NOx, and SO2.
    - Conversion guidance provided to kilograms per hectare per year (e.g., multiply keq ha-1 y-1 by 16 for S, by 14 for N) where needed.
  - Data structure and documentation
    - Detailed per-file schemas describing field names, units, and descriptions (SITECODE, SITENAME, GRIDAREA, YEAR, species-specific columns).
    - Emphasizes 3-year rolling means (2018–2020) and ecosystem-specific vs grid-average representations.
  - Quality control
    - Methods align with government QA practices; peer-reviewed CBED/PCM data and model inter-comparison (e.g., Carslaw 2011).
    - Mass-balance checks for deposition consistency; documented method developments with version control and centralized code storage.

- Access and references
  - Resource locators and supporting information:
    - UK Acidifying and Eutrophying Atmospheric Pollutants Supporting information
    - UK Air Defra network pages and PCM data portal
  - Core references include peer-reviewed studies and Defra inter-comparison reports that underlie CBED and PCM methodologies.

- Practical implications for data stewardship
  - Ensures standardized, area-weighted deposition values and grid-average concentrations are consistently derived and stored for protected-site analyses.
  - Maintains comprehensive metadata and file-level schemas to support discoverability, reuse, and updates.
  - Provides a robust QA framework and versioned data pipeline suitable for governance within large datasets and organizational data networks.
  - Documents the spatial mapping workflow, model inputs/assumptions, and data limitations (e.g., inter-annual variability and orographic adjustments) to guide data users and maintainers.