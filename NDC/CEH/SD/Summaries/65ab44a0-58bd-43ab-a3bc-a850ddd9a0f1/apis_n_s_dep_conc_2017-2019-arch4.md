# UK Acidifying and Eutrophying Atmospheric Pollutants Supporting information

## Executive summary
- Describes a data-products workflow combining CBED deposition modelling and PCM concentration modelling to map and quantify deposition and concentrations over UK protected sites (SAC, SPA, SSSI).
- Produces grid-based deposition (5x5 km) and concentration (1x1 km) outputs, aggregated to site boundaries, with 3-year rolling means (2017–2019).
- Distinguishes forest and moorland deposition, includes grid-average and ecosystem-specific values, and provides minimum, maximum, and average deposition values for sites and grids.
- Data are obtained from UK national datasets (UKEAP for CBED and Defra PCM) and are accompanied by detailed metadata, QA, and published methodology.
- Includes a variety of tabular data files (deposition and concentration by site/grid, at multiple resolutions) and clear units, with supporting information and access links.

## Data system and modelling approaches
- Step 1: Spatial mapping
  - Create a UK 5x5 km grid and clip to protected site boundaries to produce site-specific gridded data for SAC, SPA, and SSSI.
  - Merge with 3-year CBED outputs (2017–2019) to generate UK protected sites CBED dataset.
  - Repeat for 1x1 km concentration datasets (NOx and SO2) from the PCM model.
  - Data sources for site boundaries and features are downloaded from each country’s national websites.
- Step 2: Deriving deposition/concentration metrics
  - Use SQL on the gridded data to compute minimum, maximum, and grid-average deposition/concentration per site.
  - Grid-average deposition is computed as CBED deposition value multiplied by (GridArea / Total Site Area) and then summed for the site.
- CBED modelling (Concentration Based Estimated Deposition)
  - Produces 5x5 km resolution maps for wet/dry deposition of nitrogen and sulfur species and base cations.
  - Interpolates site measurements to concentration maps; combines with precipitation data to obtain wet deposition; uses land-cover–specific deposition velocities for dry deposition across five land-cover types.
  - Distinguishes contributions to non-woodland habitats vs. woodland habitats; accounts for occult deposition and orographic enhancement.
  - Averaged over rolling 3-year periods to smooth inter-annual variability; values provided as annual but delivered as 3-year means (exception: non-marine Ca+Mg for 2019).
- PCM modelling ( Pollution Climate Mapping)
  - Produces baseline maps and 1x1 km grids of pollutant concentrations (NOx, NO2, PM10, PM2.5, SO2, etc.) for the UK.
  - Runs per pollutant with base year and projection scenarios; supports policy development, scenario assessment, and TEN applications.
- Timeframe and outputs
  - Outputs are anchored to 2017–2019 rolling means; some data (e.g., non-marine Ca+Mg) have special handling (2019 only for certain metrics).
  - Outputs include both ecosystem-specific (moorland/forest) and grid-average values.

## Data assets and structure
- Data sources and file types
  - 3-year mean concentrations/depositions for SAC/SPA/SSSI across grid squares (5x5 km for deposition; 1x1 km for concentrations).
  - Ecosystem-specific deposition by forest and moorland, including min, max, and average values at 5x5 km resolution.
  - Grid-average deposition and concentration values (5x5 km and 1x1 km) for multiple pollutants.
  - Ammonia concentration data at 5x5 km and site level; NOx and SO2 concentration data at 1x1 km or 5x5 km as applicable.
- Data products (examples of content)
  - Deposition: NH3/NH4, NO2/NO3, SO2/SO4, Ca/Mg NM, for forest, moorland, and grid-average; includes min, max, avg, and area-weighted values.
  - Concentrations: NH3_CONC, NO2_CONC, SO2_CONC at site-by-grid resolutions; max/min/avg where applicable.
  - Site-level attributes: SITECODE, SITENAME, SITEAREA, CENTROID coordinates, COUNTRY, DESIGNATION, YEAR.
- Timeframe and resolution
  - 3-year means for 2017–2019.
  - 5x5 km grid data for deposition; 1x1 km grid data for concentrations.
- Units and interpretation
  - Deposition: keq ha-1 year-1 (convertible to kg S ha-1 year-1 or kg N ha-1 year-1 as needed).
  - Concentrations: µg m-3.
- Data governance and quality
  - Method developments follow QA guidelines and are documented with version control; mass-balance checks performed.
  - CBED/PCM data subjected to peer review and inter-comparison exercises; results published in the literature.

## Data quality, standards, and metadata
- Quality control
  - Extensive peer review of CBED methods; participation in Defra model inter-comparison exercises.
  - Documentation practices include versioning, central storage, and routine mass-balance checks against prior years.
- Metadata and structure
  - Detailed file-level metadata describing site, year, grid area, and deposition/concentration values (forest, moorland, grid-average) for each metric.
  - Clear unit definitions and conversion guidance (e.g., keq to kg conversions).

## Access, reuse, and practical notes for Data Leaders
- Data sources and access
  - CBED data and supporting information: UK Acidifying and Eutrophying Atmospheric Pollutants (supporting information) and related Defra resources.
  - PCM data: multiple Defra-hosted data portals and UK-air data repositories.
- Practical considerations
  - Data are rolled to 3-year means to smooth inter-annual variability; be mindful of potential biases from annual anomalies.
  - The combination of 5x5 km and 1x1 km layers enables multi-scale analysis and cross-walks between site boundaries and grid cells.
  - Use site-level min/max/avg deposition values and grid-average values to assess worst-case and typical deposition scenarios across protected sites.
- Coordination and community
  - The approach relies on integration of CBED and PCM models with national datasets; alignment with broader air quality data initiatives supports consistent, system-wide data governance.

## References and supporting information
- Includes peer-reviewed references, model evaluation reports, and technical notes related to CBED and PCM methodologies.
- Resource locators provided for UK Eutrophying and Acidifying Pollutants datasets and PCM data portals.