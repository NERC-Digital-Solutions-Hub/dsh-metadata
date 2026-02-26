# CBED and PCM Modelling for UK Protected Sites

- Purpose and scope
  - Implements environmental health monitoring methods to assess deposition and concentration of pollutants at UK protected sites (SACs, SPAs, and SSSIs).
  - Combines CBED (Concentration Based Estimated Deposition) for deposition mapping with PCM (Pollution Climate Mapping) for concentration mapping.
  - Produces 3-year rolling mean outputs (2013-2015) at different grid resolutions to inform policy decisions and exceedance assessments.

- Step 1: Spatial Mapping to protected sites
  - Create a 5x5 km grid for the UK, clipped to SAC/SPA/SSSI boundaries.
  - Merge gridded deposition data with 3-year CBED outputs to create a UK protected sites CBED dataset.
  - Repeat a similar process for 1x1 km concentration data for NOx and SO2 using PCM outputs.
  - Data sources: boundary and site data from JNCC and national sources; Figure illustrates grid-site integration.

- Step 2: Deriving minimum, maximum, and grid-averaged values
  - For each protected site, compute minimum, maximum, and grid-average deposition/concentration via SQL on the gridded dataset.
  - Grid-average calculation uses site area weighting: CBEDDepositionValue × (GridArea / SiteTotalArea), summed across grid squares within the site.
  - Outputs include site-level deposition and concentration metrics used for exceedance and habitat impact assessments.

- CBED modelling: deposition mapping details
  - Generates 5x5 km resolution maps of wet and dry deposition for nitrogen (oxidised/reduced), sulphur, and base cations using gas/PM concentrations and precipitation-derived wet deposition.
  - Dry deposition: uses concentration maps, habitat-specific deposition velocities, and five land-cover categories (forest, moorland, grassland, arable, urban).
  - Wet deposition: includes direct deposition, occult deposition to vegetation, and an orographic enhancement factor for uplands (seeded from Great Dun Fell and Holme Moss observations).
  - Ecosystem-specific application for exceedance: moorland for non-woodland habitats; forest for woodland habitats.
  - Temporal aspect: inter-annual variability due to weather and atmospheric processes; three-year means used to smooth variability.
  - Outputs: annual values presented as rolling 3-year means, with ecosystem-specific and grid-average variants.

- PCM modelling: concentration mapping details
  - Produces 1x1 km background concentration maps for multiple pollutants, in support of UK EU Directive 2008/50/EC reporting.
  - Components: a base-year model and a projections model per pollutant (NOx, NO2, PM10, PM2.5, SO2, etc.).
  - Outputs include ~9,000 road-side representative values and scenario/exposure calculations for policy development and TEN (Time Extension Notification) applications.

- Data types, units, and conversions
  - Deposition values: recorded as keq ha-1 year-1 (kiloequivalents per hectare per year); convert to kg S ha-1 year-1 by multiplying by 16 (for sulfur) and to kg N ha-1 year-1 by multiplying by 14 (for nitrogen).
  - Concentration values: expressed as µg/m3.
  - Total nitrogen deposition is the sum of NO2_NO3 and NH3_NH4 components.

- Data quality and governance
  - Methods align with QA standards for government analytical models; peer-reviewed and inter-comparison tested (e.g., Carslaw 2011).
  - Documentation, versioning, and central code storage maintained; mass-balance checks performed to ensure numerical consistency with prior years.
  - Extensive publication of CBED and PCM results; governance by senior responsible officers for methodological updates.

- Data structure and datasets (2013-2015 3-year means)
  - Datasets include:
    - 5x5 km grid deposition by site for moorland and forest ecosystems (NH3/NH4, NO2/NO3, SO2/SO4, etc.) at 5x5 km resolution.
    - 1x1 km grid concentrations for NOx and SO2 at site-level by grid.
    - Site-by-grid datasets detailing deposition and concentration with fields for SITECODE, SITENAME, SITEAREA, CENTROID coordinates, GRIDAREA, YEAR, and ecosystem-specific deposition/concentration values (minimum, maximum, average, and grid-average variants).
  - Outputs are grid-weighted site statistics and 3-year means for both deposition (keq ha-1 year-1) and concentrations (µg/m3).

- Supporting information and resources
  - Access to related supporting information, data portals, and PCM model data via Defra/UK air and CEH resources.
  - Data tables and CSVs provide site metadata and detailed deposition/concentration metrics across moorland, forest, and grid-average scenarios.

- What this means for monitoring frameworks
  - Provides a structured, governance-ready approach to spatially map pollutant deposition and concentrations to protected habitats.
  - Delivers policy-relevant metrics (min/max/average, site-by-grid, ecosystem-specific) to assess ecological risk and inform future decisions.
  - Combines robust QA, metadata management, and transparent data sharing foundations to enable reproducibility and stakeholder scrutiny.