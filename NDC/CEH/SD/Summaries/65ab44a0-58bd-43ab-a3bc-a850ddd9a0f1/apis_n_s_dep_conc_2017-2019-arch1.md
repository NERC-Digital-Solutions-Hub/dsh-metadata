# UK Acidifying and Eutrophying Atmospheric Pollutants Supporting information

- Purpose: Describe how CBED and PCM model outputs are spatially mapped to UK protected sites (SAC, SPA, SSSI), how deposition/concentration values are derived at site level, and how data are structured and quality-controlled for analysis and reporting.

## Methodology

- Step 1: Spatial mapping
  - Create a 5x5 km UK grid, clip to UK protected site boundaries (SAC, SPA, SSSI) to produce gridded datasets for all sites.
  - Merge these grids with 3-year averaged CBED output data (2017–2019) to form a UK protected sites CBED dataset.
  - Repeat the process for 1x1 km concentration datasets for NOX and SO2 using the PCM model.
  - Data sources for site boundaries and attributes are downloaded from national websites.
  - Output visual: UK protected site grid overlaid with CBED data (Figure 1).

- Step 2: Generating minimum, maximum, and grid-average values
  - Use SQL queries on the gridded dataset to compute deposition/concentration values for each site.
  - Grid-average deposition per site is calculated as CBEDDepositionValue × (GridArea / TotalSiteArea), with results summed to give the site-level grid average.
  - Outputs encompass minimum, maximum, and area-weighted values to reflect ecosystem-specific deposition.

- CBED Modelling (Concentration Based Estimated Deposition)
  - Produces 5x5 km resolution maps of wet/dry deposition for S, N, and base cations from site measurements.
  - Interpolates site data to generate concentration maps; combines with precipitation to yield wet deposition.
  - Dry deposition computed for five land-cover categories (forest, moorland, grassland, arable, urban) using habitat-specific deposition velocities; applies to moorland/forest depending on non-woodland/woodland habitats.
  - Wet deposition includes precipitation deposition and occult deposition; atmospheric chemistry and transport considered; an orographic enhancement factor accounts for upland precipitation concentration.
  - Inter-annual variability exists; CBED deposition values used to calculate exceedances of critical loads are averaged over three years (rolled mean).
  - Yearly data presented as rolling 3-year means, ecosystem-specific (moorland, forest) and a grid-average option; non-marine Ca+Mg values are provided only for 2019.

- PCM Modelling (Pollution Climate Mapping)
  - Produces background maps and 1x1 km grids of pollutant concentrations (UK-wide) per pollutant (e.g., NOx, NO2, SO2, PM, etc.).
  - Two parts per pollutant: base year model and projection model; outputs include ~9,000 road-side values.
  - Used for scenario assessment, population exposure calculations, policy development, and TEN (Time Extension Notification) applications.

## Outputs and data structure

- Data are delivered as multiple 3-year means (2017–2019) at specific grid resolutions and ecosystem assumptions:
  - 5x5 km grid deposition data for forest and moorland (and grid average), at keq ha-1 year-1.
  - 1x1 km grid concentration data for NOx and SO2, at µg m-3.
  - 3-year means presented for different ecosystem assumptions:
    - Moorland deposition, forest deposition, and grid-average deposition (for nitrogen, sulphur, and Ca+Mg where applicable).
  - Files describe site-level and grid-level deposition/concentration values, including minimum, maximum, and average values for forest or moorland as appropriate.
- Specific file groups and purposes:
  - Files 1–3: Deposition by 5x5 km grid for forest, moorland, and grid-average, respectively; include SITECODE, SITENAME, SITEAREA, CENTROID coordinates, GRIDAREA, YEAR, and deposition components (NH3/NH4, NO2/NO3, SO2/SO4, Ca/Mg NM).
  - File 4: Ammonia concentration by 5x5 km grid (NH3_conc).
  - File 5: NOx concentration by 1x1 km grid (NO2_conc).
  - File 6: SO2 concentration by 1x1 km grid (SO2_conc).
  - File 7: Deposition by forest site—minimum, maximum, and average values for NO2/NO3, NH3/NH4, SO2/SO4, Ca/Mg NM (across forest, moorland, or forest-specific aggregates).
  - File 8: Deposition by moorland site—minimum, maximum, and average values for NO2/NO3, NH3/NH4, SO2/SO4, Ca/Mg NM.
  - File 9: Deposition by grid-average site—minimum, maximum, and average values for NO2/NO3, NH3/NH4, SO2/SO4, Ca/Mg NM.
  - File 10: Ammonia concentration by site—max, min, and average NH3_conc.
  - File 11: NOx concentration by site—max, min, and average NOx_conc.
  - File 12: SO2 concentration by site—max, min, and average SO2_conc.
- All deposition values: keq ha-1 year-1; conversions to kg S ha-1 year-1 or kg N ha-1 year-1 provided (multiply by 16 for S, by 14 for N).
- Concentration values: µg m-3.

## Units, quality control, and data management

- Units:
  - Deposition: keq ha-1 year-1 (convertible to kg S or N ha-1 year-1 as noted).
  - Concentrations: µg m-3.
- Quality control:
  - CBED data and calculations follow QA procedures aligned with Government analytical model standards.
  - Peer-reviewed validation and inter-comparison exercises (e.g., Carslaw 2011) are referenced.
  - Version control, central storage of code, and routine mass-balance checks to ensure numerical consistency.
- Data provenance and discoverability:
  - Data sources are documented, with datasets and methods archived for reproducibility.
  - Data structures delineate site-level and grid-level outputs, with explicit field descriptions (SITECODE, SITENAME, GRIDAREA, YEAR, etc.).

## Practical use and considerations

- Applications:
  - Estimating site-specific and grid-average deposition and ambient concentrations to inform exceedance analyses of critical loads.
  - Supporting policy development, scenario testing, and exposure assessment for protected sites.
- Challenges and caveats (from archetype perspective):
  - Access to updated or higher-resolution data may require navigating multiple data portals and potential updates to sites or designations.
  - Inter-annual variability and landscape-scale deposition dynamics require careful interpretation of 3-year rolling means.
  - Harmonising data across different grid resolutions (5x5 km vs 1x1 km) and ecosystem assumptions may be necessary for integrated analyses.

## References and data sources

- Key methodological references include CBED-related evaluations and foundational studies on deposition modelling and attenuation factors (e.g., Holme Moss studies, Pennines observations, inter-comparison reports, and related atmospheric chemistry literature).
- Resource locators provide access to:
  - UK Acidifying and Eutrophying Atmospheric Pollutants information portal.
  - UK-AIR Defra network information and PCM data portal.
  - PCM model documentation and supporting information.