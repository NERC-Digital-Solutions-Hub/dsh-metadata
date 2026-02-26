# Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

- Purpose
  - Create a harmonised, time-averaged view of pollutant deposition and concentrations at UK protected sites to support environmental health assessment and policy evaluation.

- Overall approach
  - Use GIS and data processing tools (R, QGIS, FME) to generate a 5x5 km grid covering the UK, clipped to SAC, SPA, and SSSI boundaries.
  - Merge grid data with three-year average CBED outputs (2015–2017) for deposition; incorporate 1x1 km PCM-derived concentration data for NOx and SO2.

- Data sources and preparation
  - Protected site boundaries downloaded from respective national websites.
  - CBED: Concentration-Based Estimated Deposition model outputs from UK Eutrophying and Acidifying Pollutants (UKEAP) network; provides wet and dry deposition estimates.
  - PCM: Pollution Climate Mapping model outputs providing background concentrations on a 1x1 km grid.
  - Wet deposition: combines ion concentrations in precipitation with UK precipitation map; accounts for occult deposition to vegetation; includes orographic enhancement for uplands.
  - Dry deposition: derived from gas/PM concentrations and habitat-specific deposition velocities across five land-cover categories (forest, moorland, grassland, arable, urban).

- Step 1: Spatial mapping workflow
  - Generate 5x5 km UK grid and clip to protected sites (SAC, SPA, SSSI).
  - Merge gridded CBED deposition data with the clipped sites dataset (UK protected sites CBED dataset) using FME.
  - Repeat for 1x1 km NOx and SO2 concentration datasets from PCM.
  - Data fields include site codes, site areas, centroids, grid areas, and designated site type.

- Step 2: Generating deposition/concentration metrics for each site
  - Compute minimum, maximum, and grid-average deposition/concentration values per protected site.
  - Grid-average calculation: grid-square area proportion within the site multiplied by the CBED deposition value, then summed across grid squares to yield a site-level value.
  - Expression used: CBEDDepositionValue × (GridArea / TotalSiteArea).

- Modelling components
  - CBED Modelling
    - Produces 5x5 km resolution maps of wet and dry deposition for S, N (oxidised and reduced forms), and base cations.
    - Inputs: gas/PM concentrations and precipitation ion concentrations; precipitation map from UK Met Office; habitat-specific deposition velocities for five land-cover types.
    - Dry deposition specifics: gases (SO2, HNO3, NO2, NH3) and PM (sulphate, nitrate, ammonium, Ca, Mg) to vegetation; deposition to non-woodland vs woodland habitats applied accordingly.
    - Wet deposition: includes direct and occult deposition; segregates anthropogenic vs total sulphur and calcium using sea-salt ratios; includes an orographic enhancement factor (observations from Great Dun Fell and Holme Moss).
    - Temporal aspect: results are inherently variable year-to-year, so 3-year means are used; outputs are provided as rolling 3-year means with ecosystem-specific variants (moorland, forest, and grid-average).
    - Outputs used for critical-load exceedance calculations; values expressed in keq ha-1 yr-1; conversions to kg ha-1 yr-1 provided.
  - PCM Modelling
    - Produces background maps and 1x1 km grid concentrations for UK pollutants (NOx, NO2, PM10, PM2.5, SO2, etc.) per pollutant, with a base-year and projection runs.
    - Used for policy development, population exposure assessments, and TEN (Time Extension Notification) applications.

- Data quality and governance
  - Methods align with QA standards for government analytical models; extensive peer review and participation in Defra model inter-comparison (e.g., Carslaw 2011).
  - Version control, method documentation, and central storage of code.
  - Mass-balance checks and validation against previous years.

- Data structure and datasets (high-level)
  - Dataset themes cover 3-year means for 2015–2017, at 5x5 km grid resolution (deposition) and 1x1 km grid resolution (concentrations), plus site-level minimum/maximum/average values.
  - Examples of dataset types:
    - By-grid deposition to forest and moorland, plus grid-average deposition (datasets 1–3, 7–9, 11).
    - By-grid concentrations for ammonia, NOx, and SO2 (datasets 4–6).
    - Site-level deposition and concentration summaries (datasets 7–12, with minimum, maximum, and average values for forest or moorland habitats).
  - Data fields typically include SITECODE, SITENAME, SITEAREA, centroids, COUNTRY, DESIGNATION (SAC/SPA/SSSI), GRIDAREA, YEAR, and relevant pollutant-specific metrics (e.g., NH3_NH4_FOREST, NO2_NO3_FOREST, SO2_SO4_NM_FOREST, NH3_CONC, NO2_CONC, SO2_CONC, etc.).

- Units and interpretation
  - Deposition values: keq ha-1 year-1 (convertible to kg of S or N ha-1 year-1 using factors; 16 for S, 14 for N).
  - Concentrations: µg m-3 for NH3, NOx, NO2, SO2.

- Data access and resources
  - Multiple data resources and supporting information pages are provided (e.g., UK Aired pollutant datasets, PCM data portals) with direct links for further detail and data download.

- Key considerations for Analysts
  - Inter-annual variability is smoothed by using rolling 3-year means; still, significant year-to-year fluctuations can occur due to weather, emissions, and atmospheric transport.
  - The datasets are designed to be combined with other data sources to increase their value beyond single-use applications.
  - Emphasis on ensuring access to underlying data to support transparency and re-use in policy assessment and environmental health monitoring.

- Practical applications
  - Used to assess spatial patterns and intensities of deposition and ambient concentrations at protected sites.
  - Supports evaluation of critical-load exceedances and informs habitat-specific exposure assessments and policy decisions.
  - Provides standardized, exportable formats (maps, charts, and tables) for reporting and portal upload.