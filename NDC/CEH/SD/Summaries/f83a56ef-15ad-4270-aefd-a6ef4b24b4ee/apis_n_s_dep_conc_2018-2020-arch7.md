# Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

- Purpose
  - Create a gridded dataset to understand deposition and concentration at UK protected sites (SAC, SPA, SSSI) using map-based data products.
  - Enable analysis of spatial features (deposition and pollutants) across protected sites.

- Data sources and grid construction
  - Build a 1x1 km UK grid; clip to boundaries of protected sites to produce site-specific gridded data.
  - Merge gridded CBED outputs (3-year mean: 2018–2020) with site boundaries to produce a UK protected-sites CBED dataset.
  - Generate gridded concentration maps for NOx and SO2 from PCM model data.
  - Data on protected-site boundaries and site lists were downloaded from respective national sources.

- Step 1 outputs
  - UK protected sites CBED dataset (deposition by 1x1 km grid intersected with SAC/SPA/SSSI extents).
  - Associated 1x1 km concentration grids for NOx and SO2 (from PCM).

- Process details (depiction)
  - A Figure (UK protected site as a 5x5 km grid merged with the 3-year CBED data) illustrates the integration approach.

- Step 2: Generating minimum, maximum, and grid average values
  - For each protected site, compute:
    - Minimum deposition/concentration across its grid cells.
    - Maximum deposition/concentration across its grid cells.
    - Grid-average deposition/concentration by weighting each 1x1 km cell by its area relative to the total site area and summing.
  - Calculation approach (summary of Equation 1):
    - Grid-average value = CBED deposition value × (Grid Area / Total Site Area), then sum across grid cells within the site.

- CBED Modelling (background)
  - CBED creates 1x1 km resolution maps of wet and dry deposition for sulphur, oxidised/reduced nitrogen, and base cations from air concentrations and precipitation-derived ions.
  - Wet deposition: uses precipitation maps, cloud-precipitation contributions, and an orographic enhancement factor for upland regions.
  - Dry deposition: combines gas/PM deposition with habitat-specific deposition velocities for five land-cover categories (forest, moorland, grassland, arable, urban).
  - Ecosystem-specific application:
    - Moorland vs forest deposition values applied to non-woodland vs woodland habitats respectively.
  - Inter-annual variability: annual deposition can vary; CBED values are averaged over three years (rolling mean) to reduce variability.
  - Outputs and ecosystem scenarios: annual data presented as rolling 3-year means; ecosystem-specific values include moorland/forest assumptions and a grid-average.

- PCM Modelling (background)
  - Pollution Climate Mapping model produces 1x1 km background concentration maps for UK pollutants.
  - PCM consists of separate models per pollutant (NOx, NO2, PM10/PM2.5, SO2, etc.), with base-year and projection components.
  - Outputs include grid-wide background concentrations and around 9,000 representative roadside values.
  - Applications: scenario assessment, population exposure calculations, and support for policy/ TEN (Time Extension Notification) requirements.

- Quality and validation
  - Methods align with QA/GA procedures for government analytical models; extensively published and peer-reviewed.
  - CBED/PCM undergo peer review and inter-comparison exercises; mass-balance checks ensure numerical consistency.
  - Version control and documentation practices enforced; responsible-officer oversight.

- Data structure and files (overview)
  - The dataset comprises multiple CSV files (12 primary data files) covering:
    - Site-level and grid-level deposition data (forest, moorland, grid-average) for nitrogen and sulphur compounds.
    - Concentration data for ammonia (NH3), nitrogen oxides (NOx), and sulphur dioxide (SO2) at site and grid levels.
    - Minimum, maximum, and average deposition values by ecosystem type and across grid averages.
    - Yearly 3-year means (2018–2020) for various pollutants, with site, centroid, extent, and grid-area fields.

- Resource locators
  - UK Acidifying and Eutrophying Atmospheric Pollutants (ukeap)
    - http://www.pollutantdeposition.ceh.ac.uk/ukeap
  - UK Air Defra network information
    - https://uk-air.defra.gov.uk/networks/network-info?view=ukeap
  - PCM data and model information
    - https://uk-air.defra.gov.uk/data/pcm-data

- Nature and units of recorded values (highlights)
  - Deposition values (nitrogen and sulphur) are in keq ha-1 year-1 and can be converted to kg ha-1 year-1 by multiplying by 14 (N) or 16 (S).
  - Concentration values are in micrograms per cubic metre (µg m-3).
  - 3-year means are ecosystem-specific and presented as minimum/maximum/average values where applicable.

- Data structure details (summary)
  - File 1–3: Site-by-grid deposition data for forest/moorland and grid-average; 2018–2020 3-year means; various deposition components (NH3/NH4, NO2/NO3, SO2/SO4, Ca/Mg).
  - File 4–6: Ammonia, NOx, and SO2 concentration data by grid; 2018–2020 3-year means.
  - File 7–9: Generated minimum, maximum, and grid-average deposition data by ecosystem type (forest, moorland) and grid-average.
  - File 10–12: Concentration data (NH3, NO2, SO2) with min/max/avg by site/GRIDAVERAGE or by ecosystem type.
  - All files use consistent fields: SITECODE, SITENAME, SITEAREA, CENTROID_X/Y, COUNTRY, DESIGNATION, YEAR, deposition/concentration values by pollutant/measure, GRIDAREA.

- Key outputs and intended use
  - A harmonized, gridded representation of deposition and concentrations for UK protected sites to support policy analysis, impact assessment, and visualization via GIS.
  - Foundations for further spatial analysis, reporting, and decision-making related to nutrient and acid deposition on protected habitats.

- Note on steps and scope
  - Step 1 established the spatial mapping framework (1x1 km grid clipping to protected sites and merging with CBED/PCM outputs).
  - Step 2 computed site-level summaries (min, max, grid-average) using area-weighted aggregation.

- End-to-end perspective
  - Integrates gridded deposition (CBED) and concentration (PCM) data with site boundaries to produce ready-to-map, policy-relevant indicators for protected sites across the UK.