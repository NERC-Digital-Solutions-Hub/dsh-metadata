# UK Acidifying and Eutrophying Atmospheric Pollutants Supporting information

- Objective and scope
  - Map deposition and concentration of key pollutants to UK protected sites (SAC, SPA, SSSI/ASSI) using 1x1 km gridded data for the period 2018–2020 (3-year rolling means).
  - Integrate data from CBED (deposition) and PCM (concentrations) models to support assessments of nutrient and acidity stress on protected habitats.
  - Produce site-level statistics (minimum, maximum, and grid-average values) to inform exceedance calculations and policy/support decisions.

- Data sources and models
  - CBED (Concentration Based Estimated Deposition): generates 1x1 km maps of wet and dry deposition for sulphur, oxidised/reduced nitrogen, and base cations based on measured concentrations and habitat-specific deposition velocities; includes both wet and dry deposition components and habitat mixing (forest, moorland, grassland, arable, urban).
  - PCM (Pollution Climate Mapping): provides 1x1 km background concentration maps for pollutants (NOx, NO2, SO2, PM, etc.) and around 9,000 road-side values; used for scenario assessment and policy support.
  - Data are produced as rolling 3-year means (2018–2020) and include ecosystem-specific (moorland, forest) as well as grid-average outputs.

- Step 1: Spatial mapping and data preparation
  - Create a UK-wide 1x1 km grid and clip it to protected site boundaries (SAC, SPA, SSSI/ASSI).
  - Merge gridded deposition data (CBED) and concentration data (PCM) with site boundaries to form a UK protected sites CBED dataset and corresponding concentration datasets (NOx and SO2).
  - Retrieve site boundary and feature data from national sources; generate a combined gridded dataset for each site.

- Step 2: Deriving deposition/concentration statistics for each site
  - Compute minimum, maximum, and grid-average deposition/concentration for each protected site via SQL on the gridded dataset.
  - Grid-average calculation concept: grid-square area proportion within a site multiplied by the site’s CBED deposition value, then summed across all squares in the site (Equation 1).
  - Outputs cover deposition for nitrogen and sulphur compounds (NH3/NH4, NO2/NO3, SO2/SO4, Ca/Mg) with ecosystem-specific or grid-average contexts.

- CBED methodology details
  - Wet deposition: derived from precipitation, direct deposition to vegetation, and occult deposition (cloud droplet deposition).
  - Dry deposition: uses habitat-specific deposition velocities for five land cover types (forest, moorland, grassland, arable, urban); combines gas and particulate deposition to vegetation.
  - Ecosystem assignments: deposition values applied to moorland vs forest depending on habitat; sea-salt separation and wet deposition components accounted for.
  - Inter-annual variability: natural weather patterns cause variations; results are averaged over three years to smooth fluctuations.
  - Outputs: annual values presented as rolling 3-year means, with ecosystem-specific and grid-average options.

- PCM modelling details
  - Produces 1x1 km grid background pollutant concentrations and additional road-side values.
  - Used for baseline exposure, scenario analysis, and policy support (e.g., TEN applications for PM10/NOx).

- Data units and interpretation
  - Deposition: expressed as kilo-equivalents per hectare per year (keq ha-1 year-1); conversions to kg S ha-1 year-1 or kg N ha-1 year-1 via keq multipliers (S = 16, N = 14).
  - Concentrations: expressed as micrograms per cubic metre (µg m-3).
  - Total nitrogen deposition: sum of NO2/NO3 and NH3/NH4 components.
  - Output files provide 3-year means (2018–2020) for different deposition/concentration components and across habitat categories or grid-average.

- Data quality control and governance
  - Methods align with government QA practices; peer-reviewed CBED/PCM results and inter-comparison exercises (e.g., Carslaw 2011).
  - Mass balance checks ensure numerical consistency; method developments are reviewed and approved by senior responsible officers.
  - Documentation, version control, and centralized storage of code and method updates are maintained.

- Data structure and files (high-level)
  - Files deliver 3-year mean concentrations and deposition values at 1x1 km grid resolution for sites (SAC, SPA, SSSI).
  - Categories include forest, moorland, and grid-average ecosystem contexts.
  - Examples of data fields:
    - Site identifiers, designations (SAC/SPA/SSSI), site area, grid overlap, year (mid-year of rolling average).
    - Deposition fields by ecosystem (NH3/NH4, NO2/NO3, SO2/SO4, Ca/Mg) for forest, moorland, and grid-average.
    - Concentration fields for ammonia, nitrogen oxides, and sulphur dioxide (grid-average, forest/moorland contexts as applicable).
  - Files are organized to support minimum, maximum, and average (AVG) values for each pollutant-deposition component and ecosystem type.
  - Specific file examples include:
    - Forest deposition and concentration by grid, by year, and by 3-year means.
    - Moorland deposition and concentration by grid, by year, and by 3-year means.
    - Grid-average deposition and concentration by year and 3-year means.

- Practical implications for data leadership
  - Provides a robust, grid-level, site-specific basis for assessing deposition and concentration pressures on protected habitats.
  - Enables co-ownership of data products between policy, science, and data teams through clear data lineage, spatial granularity, and explicit uncertainty/variability considerations.
  - Highlights data gaps and access considerations (e.g., paywalls and data protection barriers) as ongoing challenges when aggregating model outputs with site boundaries.
  - Demonstrates the value of combining modelled deposition (CBED) with concentration maps (PCM) to derive actionable site-level metrics for policy and conservation planning.

- References and access
  - The methodology builds on a body of peer-reviewed work and Defra/UK air quality sources; inter-comparison and QA references are provided.
  - Resource links for CBED/PCM data and supporting information are included for data discovery and reproducibility.