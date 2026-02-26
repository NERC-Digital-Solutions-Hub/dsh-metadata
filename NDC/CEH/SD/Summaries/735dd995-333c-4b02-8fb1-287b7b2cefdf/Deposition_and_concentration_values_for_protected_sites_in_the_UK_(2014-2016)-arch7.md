# Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

- Objective
  - Create gridded deposition and concentration data aligned to UK protected sites (SAC, SPA, SSSI) for assessment and visualization.
  - Generate per-site minimum, maximum, and grid-average deposition/concentration values.

- GIS workflow and data integration
  - Build a 5x5 km UK grid with Feature Manipulation Engine (FME).
  - Clip the grid to SAC/SPA/SSSI boundaries to produce site-by-grid datasets.
  - Merge gridded site data with 3-year CBED means (2014–2016) to produce UK protected sites CBED data.
  - Repeat for 1x1 km concentration data (NOx and SO2) derived from the PCM model.
  - Data sources: boundary and feature data for protected sites from JNCC and national sources; CBED outputs; PCM model outputs.

- Step 2: Generating minimum, maximum, and grid-average values
  - Use SQL on the gridded dataset to compute per-site statistics.
  - Grid-average value for a site: CBEDDepositionValue × (GridArea / TotalSiteArea); sum across grids to obtain the site grid-average.
  - Outputs include minimum, maximum, and grid-average deposition/concentration values for each site.

- CBED Modelling (deposition)
  - Produces 5x5 km resolution maps of wet/dry deposition for sulphur, oxidised/reduced nitrogen, and base cations.
  - Inputs: measured concentrations of gases/PM and ions in precipitation from the UK Eutrophying and Acidifying Pollutants (UKEAP) network; precipitation maps from the UK Met Office.
  - Dry deposition: uses habitat-specific deposition velocities mapped to five land cover categories (forest, moorland, grassland, arable, urban); applies deposition to forest/woodland vs other habitats.
  - Wet deposition: includes direct deposition and occult deposition; separates anthropogenic vs total sulphur and calcium using sea-salt ratios.
  - Orographic enhancement: accounts for uplift in upland regions (observations from Great Dun Fell and Holme Moss).
  - Inter-annual variability: deposition varies with weather; CBED values are averaged over a 3-year period to smooth fluctuations.
  - Outputs: annual deposition values presented as rolling 3-year means; ecosystem-specific values (moorland, forest) and a grid-average option (three ecosystem scenarios).

- PCM Modelling (concentrations)
  - Produces background maps and 1x1 km grids of pollutant concentrations (NOx, NO2, SO2, PM, etc.) for the UK.
  - PCM is a suite of models run for Defra; one model per pollutant with base-year and projection components.
  - Outputs: 1x1 km grid concentrations plus ~9,000 representative roadside values.
  - Uses: scenario assessment, population exposure calculations, and support for policy development and TEN applications.

- Data structure and datasets (3-year means, 2014–2016)
  - Datasets include 5x5 km grid deposition (nitrogen and sulfur compounds) per site, 1x1 km concentration grids, and site-by-grid summaries.
  - Outputs include minimum, maximum, and grid-average values for deposition to forest/moorland and grid-average scenarios.
  - Units:
    - Deposition: keq ha-1 year-1 (convertible to kg ha-1 year-1 for S by ×16 and for N by ×14).
    - Concentrations: µg m-3.
  - Examples of data coverage:
    - 5x5 km grid deposition data for forest/moorland or grid-average by site.
    - 1x1 km concentration data for NOx and SO2 by site.
    - 3-year means for each dataset (2014–2016) across the specified sites.

- Minimum, maximum, and area-weighted values (example datasets)
  - Forest-related deposition (MIN_NH3_NH4_FOREST, MIN_NO2_NO3_FOREST, MIN_SO2_SO4_NM_FOREST; etc.).
  - Moorland-related deposition (MIN_NH3_NH4_MOORLAND, MIN_NO2_NO3_MOORLAND, MIN_SO2_SO4_NM_MOORLAND; etc.).
  - Maxima and averages for each ecosystem and grid-average scenarios.

- Quality control and validation
  - Methods align with government QA for analytical models; CBED peer-reviewed and part of model inter-comparison exercises.
  - Version control, documentation of method developments, and central storage of code.
  - Mass-balance checks and cross-year comparisons to ensure numerical consistency.

- Units, conversion, and interpretation
  - Deposition values in keq ha-1 year-1; convert to kg S ha-1 year-1 or kg N ha-1 year-1 using factors (S: ×16; N: ×14).
  - Concentrations in µg m-3.
  - NaN values indicate missing data from the originating dataset.

- Practical GIS considerations
  - Handling multiple data resolutions (5x5 km vs 1x1 km) and site boundary clipping.
  - Aggregation across grid cells with accurate area weighting for site-level summaries.
  - Managing inter-annual variability by using rolling 3-year means.

- References and resources
  - Foundational papers and datasets for CBED and PCM modelling (e.g., Beswick et al., Dore et al., Fowler et al., RoTAP, multiple peer-reviewed sources).
  - Online resources for CBED/UK Eutrophying and Acidifying Pollutants (UKEAP) and PCM data.

- Applications for GIS Specialists
  - Enables map-based visualization of deposition and concentration patterns for protected sites.
  - Supports critical load exceedance assessments and policy-relevant analyses.
  - Provides structured, multi-resolution datasets suitable for spatial querying and reporting.