# Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

- Objective
  - Map deposition and pollutant concentrations onto UK protected sites (SAC, SPA, SSSI) by combining CBED deposition maps with PCM concentration data to support assessment of ecosystem exposure and potential exceedances.

- Modelling frameworks
  - CBED (Concentration Based Estimated Deposition)
    - Generates 5x5 km resolution maps of wet and dry deposition for sulphur, oxidised/reduced nitrogen, and base cations from gas/particle concentrations and precipitation data.
    - Wet deposition uses precipitation concentrations plus an annual precipitation map; includes occult deposition and orographic enhancement for uplands.
    - Dry deposition uses gas/PM concentrations, habitat-specific deposition velocities, and land-cover fractions (forest, moorland, grassland, arable, urban).
    - Three ecosystem assumptions for deposition to sites: moorland, forest, and a grid-average mixture.
    - Averaged to 3-year means due to inter-annual weather variability.
  - PCM (Pollution Climate Mapping)
    - Produces 1x1 km grid background concentrations for UK pollutants; supports scenario assessment and population exposure calculations; used for TEN applications for PM10/NOx.

- Data inputs and sources
  - UKEAP (UK Eutrophying and Acidifying Pollutants) network site measurements (for CBED concentrations and deposition).
  - UK Met Office precipitation data (for wet deposition calculations).
  - Orographic enhancement factors sourced from historical studies (e.g., Great Dun Fell, Holme Moss) to adjust precipitation concentration in uplands.
  - PCM data (Defra/Ricardo Energy & Environment) for background concentrations and road-side values; multiple pollutants tracked (NOx, NO2, SO2, PM, etc.).

- Spatial processing and workflow (Step 1)
  - Create a UK-wide 5x5 km grid and clip to SAC/SPA/SSSI boundaries to produce gridded datasets for protected sites.
  - Merge gridded CBED deposition values with site boundaries using FME.
  - Step 2 (depositional values per site): Use SQL to compute minimum, maximum, and grid-average deposition/concentration per protected site.
    - Grid-average value per grid cell is CBED value times (Grid Area / Site Area); sum across grid cells overlapping the site.

- Step 2: Generating deposition/concentration values
  - For each protected site, compute:
    - Minimum deposition/concentration across grid cells within the site.
    - Maximum deposition/concentration across grid cells within the site.
    - Grid-average deposition/concentration (weighted by grid-square overlap with the site).
  - Equations and weighting reflect spatial overlap to produce site-level metrics.

- Outputs and data structure
  - Step 2 outputs include site-level metrics for 3-year rolling means (2016-2018) with:
    - 5x5 km grid deposition data by site (moorland, forest, or grid-average).
    - 1x1 km NOx and NO2 concentrations by site.
  - Detailed data structure includes multiple datasets (see dataset descriptions) reporting:
    - Site metadata (SITECODE, SITENAME, SITEAREA, CENTROID_X/Y, COUNTRY, DESIGNATION, GRIDAREA).
    - 3-year mean deposition by ecosystem type (NH3/NH4, NO2/NO3, SO2/SO4) at 5x5 km resolution (forest, moorland) and grid-average values.
    - 3-year mean concentrations for NOx, NH3, SO2 (in corresponding grid resolutions).

- Datasets and content (3-year means, 2016-2018)
  - Dataset 1-3: Deposition by grid or ecosystem
    - 5x5 km grid, forest or moorland deposition (NH3/NH4, NO2/NO3, SO2/SO4), plus grid-average values.
  - Dataset 4-6: Concentrations by grid
    - NH3, NOx, SO2 concentrations on 1x1 km grids.
  - Dataset 7-9: Site-level minimum/maximum/average deposition (forest/moorland)
  - Dataset 10-11: Grid-average site deposition and NH3/NOx concentrations by site
  - Dataset 12: NOx concentrations by site
  - Units
    - Deposition: keq ha-1 year-1 (convertible to kg S ha-1 yr-1 or kg N ha-1 yr-1 by multiplying by 16 or 14, respectively).
    - Concentrations: µg m-3.

- Quality control and validation
  - Methods aligned with government QA of analytical models; extensive peer review and inter-comparison (e.g., Carslaw 2011).
  - Version control, documentation, and central code storage.
  - Mass-balance checks and comparisons to previous years to ensure numerical consistency.
  - Extensive published methodological documentation and supporting information.

- Data interpretation and usage
  - Outputs enable assessment of critical load exceedance by site and ecosystem type.
  - Provide ecosystem-specific deposition scenarios (moorland vs forest) and a grid-average for general site exposure.
  - Supporting information for policy development, modelling validation, and impact assessment.

- References and resources
  - Beswick et al., Dore et al., Fowler et al., Stedman et al., RoTAP, Carslaw 2011, etc.
  - Supporting information and model data:
    - UK Acidifying and Eutrophying Atmospheric Pollutants (ukeap) site
    - PCM data portal (uk-air Defra)
    - PCM data for road-side values and background concentrations

- Resource locators
  - http://www.pollutantdeposition.ceh.ac.uk/ukeap
  - https://uk-air.defra.gov.uk/networks/network-info?view=ukeap
  - https://uk-air.defra.gov.uk/data/pcm-data
  - Additional referenced supporting information and model documentation links

- Additional notes
  - The CBED methodology detailed here includes both anthropogenic and non-marine deposition components, separation of total/non-marine sums via sea-salt corrections, and a three-year rolling average to mitigate inter-annual variability.
  - Wet deposition accounts for cloud interception (occult deposition) and is enhanced in upland regions; dry deposition accounts for across-land cover types and habitat-specific deposition velocities.