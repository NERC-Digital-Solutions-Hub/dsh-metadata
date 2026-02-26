# Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

- Purpose
  - Map deposition and concentration to UK protected sites (SAC, SPA, SSSI) at 1x1 km resolution.
  - Produce site-level deposition/concentration values (minimum, maximum, grid average) to support assessments of environmental health and policy performance.
  - Integrate CBED (Concentration Based Estimated Deposition) outputs with PCM (Pollution Climate Mapping) model data for protected sites.

- Step 1: Spatial data preparation
  - Create a 1x1 km grid covering the UK domain using data processing tools (R and QGIS).
  - Clip the grid to UK protected site boundaries (SAC, SPA, SSSI/ASSI) to generate gridded datasets for all sites.
  - Merge gridded datasets with the 3-year averaged CBED output data (2018-2020) to form a UK protected sites CBED dataset (see Figure 1).
  - Repeat the process for 1x1 km concentration datasets for NOx and SO2 using PCM model outputs.
  - Data sources for boundaries and site lists are downloaded from respective national websites.

- Step 2: Generating deposition/concentration statistics per site
  - Use SQL queries on the gridded dataset to compute:
    - Minimum, maximum, and grid-average deposition/concentration values for each protected site.
    - Grid-average values are calculated by weighting grid-square deposition by the overlap area with the site (grid area / total site area) and summing across grid squares (Equation 1).
  - CBED modelling details
    - CBED provides 1x1 km resolution maps of wet and dry deposition for sulphur, oxidised and reduced nitrogen, and base cations from measured air concentrations and precipitation chemistry (UK Eutrophying and Acidifying Pollutants network, UKEAP).
    - Concentrations are interpolated to maps; wet deposition combines precipitation with direct deposition of cloud droplets (occult deposition) and uses an annual precipitation map to derive wet deposition.
    - Dry deposition uses deposition velocities for five land-cover categories (forest, moorland, grassland, arable, urban) and combines with land-cover proportions to yield grid-square deposition.
    - Dry deposition includes gases (SO2, NO2, HNO3, NH3) and PM (SO4, NO3, NH4, Ca, Mg); wet deposition includes sulphate, ammonium, nitrate, calcium, magnesium, and acidity (H+).
    - For critical-load exceedance, deposition values are assigned to moorland or forest depending on habitat type.
    - Orographic enhancement is applied to precipitation for upland regions (seeder-feeder effect).
    - Inter-annual variability is smoothed by using a rolling 3-year mean (data are calculated annually but presented as rolling 3-year means; non-marine Ca+Mg values are treated specially).
    - Outputs are ecosystem-specific with three scenarios: moorland/short vegetation everywhere, forest everywhere, and a grid-average across ecosystems.
  - PCM modelling details
    - PCM generates background maps and 1x1 km grids of pollutant concentrations (NOx, NO2, PM10, PM2.5, SO2, etc.) for the UK.
    - Runs per pollutant (base year and projection model) and provides ~9,000 road-side values.
    - Used for scenario assessments, population exposure calculations, and policy support (e.g., TEN applications for PM10 and NOx).

- Data products and structure
  - 12 data files contained in the CBED/PCM outputs (3-year means for 2018-2020) covering various deposition and concentration metrics at SAC/SPA/SSSI sites, at different ecological contexts (forest, moorland) and grid-average values.
  - Examples of data content across files:
    - Site metadata: SITECODE, SITENAME, SITEAREA, CENTROID_X/Y, COUNTRY, DESIGNATION, YEAR.
    - Deposition fields by ecosystem: NH3/NH4, NO2/NO3, SO2/SO4, CA/MG for forest, moorland, or grid average.
    - Concentration fields: NH3, NOx, NO2, SO2 concentrations (grid-average and site-by-grid). 
    - For each site, multiple summary statistics are provided: MIN, MAX, AVG, and sometimes MIN/AVG/MAX per ecosystem or grid-average.
  - Units and conversions
    - Deposition values are in keq ha-1 year-1 (convertible to kg ha-1 year-1 using factors: S deposition multiply by 16; N deposition multiply by 14).
    - Concentrations are in µg m-3.

- Quality control and data management
  - Methods align with government QA practices for analytical models; CBED/PCM results are peer-reviewed and subject to inter-comparison (e.g., Carslaw 2011).
  - Documented versioning, centralized code storage, and mass-balance checks to ensure numerical consistency year-to-year.
  - Method developments are overseen by senior responsible officers.

- Data accessibility and stewardship
  - Data and outputs are stored in a structured format with clear data-files documentation.
  - Acknowledges the challenge of increasing dataset value by combining with other data and enabling access for others; the workflow supports storing and distributing underlying data for transparency and reuse.

- References and resources
  - Key literature and model reference sources (e.g., Beswick et al., Fowler et al., RoTAP) and Defra/UK AIR resources for CBED/PCM.
  - Resource locators for CBED/ukeap information, Defra network info, and PCM data.

- Enduring context
  - The workflow supports consistent, shareable, and policy-relevant assessments of environmental health across UK protected sites by integrating high-resolution deposition/concentration datasets with site boundaries and ecosystem contexts.