# Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

- Purpose and scope
  - Creates a UK-wide 5x5 km grid of deposition and concentration data and links it to UK protected sites (SAC, SPA, SSSI/ASSI) for 2017–2019 (3-year rolling means).
  - Combines CBED (Concentration Based Estimated Deposition) modelling for deposition with PCM (Pollution Climate Mapping) modelling for concentrations.
  - Outputs are designed to be discoverable and usable for policy evaluation and site-specific assessments, with data structured for integration into portals/catalogues.

- Data sources and modelling approaches
  - CBED modelling
    - Produces 5x5 km resolution maps of wet and dry deposition for sulphur, nitrogen (oxidised and reduced), and base cations.
    - Uses concentration data from air and ions in precipitation (UKEAP network) plus a UK precipitation map to generate deposition values.
    - Dry deposition uses habitat-specific deposition velocities across five land-cover categories (forest, moorland, grassland, arable, urban).
    - Wet deposition includes direct and occult deposition (cloud). Separation of anthropogenic and total components uses sea-salt adjustments; includes orographic enhancement for uplands.
    - Outputs are averaged over 3 years to smooth inter-annual variability; provided as rolling 3-year means (except non-marine Ca+Mg values which are year-specific for 2019).
    - Ecosystem-specific deposition (moorland/forest) and grid-average values are produced for each site.
  - PCM modelling
    - Generates background pollutant concentration maps on a 1x1 km grid (NOx, NO2, SO2, PM, etc.) for the UK, including ~9,000 road-side values.
    - Supports scenario analysis, population exposure calculations, TEN applications, and policy support.

- Step-by-step data processing workflow
  - Step 1: Spatial mapping
    - Build a 5x5 km grid across the UK and clip to protected site boundaries (SAC, SPA, SSSI).
    - Merge the gridded deposition data with the 3-year CBED output to produce a UK protected sites CBED dataset.
    - Repeat the process for 1x1 km concentration grids for NOx and SO2 using PCM outputs.
  - Step 2: Deriving per-site statistics
    - For each protected site, compute minimum, maximum, and grid-average deposition/concentration using SQL over the gridded dataset.
    - Grid-average per site is calculated by weighting grid-square values by the relative area of the grid within the site (grid area times site proportion).
    - CBED deposition is combined with grid areas to yield site-level grid averages (Equation: CBEDDepositionValue × (GridArea / TotalSiteArea)).
  - Timing and variations
    - Deposition values are annual but provided as rolling 3-year means to reduce inter-annual variability.
    - Deposition values reflect ecosystem-specific assumptions (moorland/forest) and mixed-grid averages.

- Data products and structure (files and key contents)
  - File groups (12+ files) cover deposition and concentration data at 5x5 km and 1x1 km resolutions, for forest and moorland sites, plus grid-average summaries.
  - Examples of data categories:
    - Deposition by grid and site (APIS_deposition_forest_sitebygrid_2017_2019.csv; APIS_deposition_moorland_sitebygrid_2017_2019.csv; APIS_deposition_gridaverage_sitebygrid_2017_2019.csv)
    - Ammonia concentrations by grid/site (APIS_ammonia_concentration_sitebygrid_2017_2019.csv; APIS_ammonia_concentration_site_2017_2019.csv)
    - Nitrogen oxides concentrations by grid/site (APIS_nox_concentration_sitebygrid_2017_2019.csv; APIS_nox_concentration_site_2017_2019.csv)
    - Sulphur dioxide concentrations by grid/site (APIS_so2_concentration_sitebygrid_2017_2019.csv; APIS_so2_concentration_site_2017_2019.csv)
  - Common fields across files
    - SITECODE, SITENAME, SITEAREA (ha), CENTROID_X, CENTROID_Y, COUNTRY, DESIGNATION (SAC/SPA/SSSI), YEAR (mid-year of 3-year rolling mean), GRIDAREA (overlap with site in hectares)
    - Deposition variables (keq ha-1 year-1) and concentration variables (µg m-3) with site- and grid-level granularity
  - Specific variable examples
    - Deposition: NH3_NH4_FOREST, NO2_NO3_FOREST, SO2_SO4_NM_FOREST, CA_MG_NM_FOREST
    - Concentrations: NH3_CONC, NO2_CONC, SO2_CONC
    - For each pollutant, data exist as minimum, maximum, average, and grid-average values in appropriate files (e.g., MIN_NO2_NO3_FOREST, AVG_NO2_NO3_GRIDAVERAGE)

- Units and data quality
  - Deposition values: kilo-equivalents per hectare per year (keq ha-1 year-1). Conversion guidance provided to kg S ha-1 year-1 and kg N ha-1 year-1.
  - Concentration values: micrograms per cubic meter (µg m-3).
  - Quality control
    - Methods align with government QA for analytical models; CBED data peer-reviewed and inter-comparison-reviewed (e.g., Carslaw 2011).
    - Documentation, version control, central storage of code, and mass-balance checks for deposition estimates.
    - Outputs have been published in peer-reviewed literature and approved by senior responsible officers.
  - Data updates and limitations
    - Outputs reflect inter-annual variability; 3-year means are used to provide stable estimates.
    - Data are specifically tied to protected sites and clipped 5x5 km grids; site overlap areas are explicitly quantified (GRIDAREA).

- Metadata, documentation and access
  - Detailed data dictionaries and file-level metadata outline site codes, designations, grid areas, and all deposition/concentration fields.
  - Resource locators provided for primary data sources and modelling tools:
    - UK Acidifying and Eutrophying Atmospheric Pollutants (ukeap) information
    - UK Air Defra pages (network info for ukeap)
    - Pollution Climate Mapping (PCM) data portal
  - File-level descriptions specify the intended use and the structure of each dataset (e.g., site-by-grid, grid-average, forest vs moorland deposition).

- Governance considerations for Data Stewards
  - Data are structured to support discovery, reuse, and integration into data portals and catalogues, with clear mapping between grid-level data and site-level summaries.
  - Clear provenance: CBED (deposition) and PCM (concentration) modelling combined with site geometry to produce reproducible per-site metrics.
  - Documentation and versioning: method development, central code storage, and regular QA align with governance expectations for complex environmental modelling datasets.
  - Access and reuse: datasets are segmented by site designation and by grid resolution, facilitating user-driven analyses across protected sites and across time.

- Summary of relevance to data governance
  - End-to-end data lineage from model input data to site-level outputs, with explicit data products suitable for discovery and reuse.
  - Consistent schema across multiple files/files groups, enabling cross-dataset integration and automated validation.
  - Well-defined units, rolling-time aggregation, and clear conversion guidance to support secondary analyses and policy interpretation.
  - Robust quality assurance framework and transparent methodological references to underpin data trust and reproducibility.