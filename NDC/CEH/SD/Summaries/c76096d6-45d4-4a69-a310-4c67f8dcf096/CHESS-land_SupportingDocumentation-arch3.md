# Water, carbon and energy fluxes simulation for Great Britain using the JULES Land Surface Model and the Climate Hydrology and Ecology research Support System meteorology dataset (1961-2015) [CHESS-land]

- Purpose: Assess the 1961–2015 Great Britain-wide balance of water, energy and carbon fluxes using the JULES land surface model driven by CHESS meteorology; CHESS-land bundles model output, ancillary files, and forcing data for these simulations.

- Data and forcing inputs
  - CHESS-met meteorological dataset at 1 km2 resolution, combining observed daily precipitation (CEH-GEAR and MORECS downscaled data) with other meteorological inputs.
  - Land cover fixedMap: CEH Land Cover 2000 (8 categories: broadleaf trees, needleleaf trees, grass, crops, shrubs, water, bare soil, urban).
  - Phenology prescribed monthly for deciduous vegetation and crops.
  - Soil hydrology based on Darcy–Richards equations with four vertical layers (0.0–0.1 m, 0.1–0.35 m, 0.35–1 m, 1–3 m).
  - Runoff generation via PDM approach with topographic data from CEH-IHDTM.
  - Time step: 30 seconds; outputs available as daily and monthly averages.

- Model and implementation
  - JULES version: vn4.5, branch r3488_albmar_spdm.
  - Configuration and driving data described in the Met Office JULES repository; access instructions provided on the project website.
  - Data and configuration are organized in a rose suite (u-aixxx) with access via the Met Office JULES ecosystem.

- Data products and formats
  - NetCDF files, CF-compliant, following CEH gridded dataset conventions.
  - Two time-averaging resolutions: daily (subset of variables) and monthly (full variable set).
  - Yearly files, with variables split into two sets:
    - HydEn set: hydrology and energy variables (e.g., gridbox moisture and heat fluxes, surface temperature, albedo, evapotranspiration, snow, runoff, routing, soil moisture across layers, and related fluxes).
    - BGC set: biogeochemistry variables (e.g., NPP, GPP, plant and soil respiration).
  - Z-dimension role: tile (surface type), plant functional type (PFT), or soil layer (when present).
  - Example HydEn variables include surface fluxes (latent and sensible heat), soil moisture, runoff, evapotranspiration, surface temperature, albedo, snow mass, and related fluxes.
  - Example BGC variables include net and gross primary productivity and plant/soil respiration.

- Data provenance and accessibility
  - Core methodology and data sources documented in the associated literature (e.g., Best et al. 2011; Clark & Gedney 2008; Fuller et al. 2002; Keller et al. 2015; Robinson et al. 2017a,b; Blyth et al.).
  - CHESS-met v1.2 and related datasets described in dedicated references.
  - Access instructions and additional configuration details available on the project website and in the Met Office JULES repository.
  - Emphasis on reproducibility: clear model versioning, data provenance, and repository-based access to configurations and forcing data.

- Relevance for monitoring frameworks
  - Provides long-term, high-resolution (1 km, 1961–2015) simulation outputs of key environmental fluxes (water, energy, carbon) suitable for monitoring policy outcomes and trends.
  - Facilitates evaluation of hydrological and carbon cycles at national scale with detailed diagnostics ( HydEn and BGC outputs).
  - Demonstrates open-data style practices: CF-compliant NetCDF, well-documented metadata, and transparent data lineage and model configuration.

- Practical considerations and challenges for monitoring teams
  - High data volume and complexity: large CF-compliant NetCDF files with multiple variable sets and resolutions.
  - Metadata completeness and data governance: ensuring adequate metadata for verification and reuse across different teams and dashboards.
  - Data access barriers: although access instructions exist, researchers may need to navigate repository systems and licensing to obtain data.
  - Data transformation and harmonization: preparing inputs/outputs for integration into monitoring dashboards may require substantial processing to align with local schemas and standards.
  - Staying up to date: model configuration and forcing data sources may evolve; version control and documentation are essential for reproducibility.