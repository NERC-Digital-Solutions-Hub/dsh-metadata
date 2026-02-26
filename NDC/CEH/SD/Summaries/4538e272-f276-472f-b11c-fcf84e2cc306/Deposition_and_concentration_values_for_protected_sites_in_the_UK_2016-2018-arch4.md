# Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

- Purpose: Describe how deposition and concentration data are mapped and aggregated to UK protected sites (SAC, SPA, SSSI) using CBED and PCM modelling outputs.

## Overview of the approach

- Uses two modelling frameworks:
  - CBED (Concentration Based Estimated Deposition) to generate 5x5 km resolution maps of wet and dry deposition for sulfur, oxidised and reduced nitrogen, and base cations.
  - PCM (Pollution Climate Mapping) to produce 1x1 km resolution background concentration maps for multiple pollutants.
- Spatial steps:
  - Create a 5x5 km UK grid.
  - Clip the grid to protected site boundaries and merge with 3-year mean CBED outputs to produce a UK protected sites CBED dataset.
  - Generate corresponding 1x1 km concentration datasets for NOx and SO2 from PCM.
- Temporal context: Outputs are presented as rolling 3-year means to smooth inter-annual variability.

## Methodology

- Step 1: Spatial mapping
  - Build a 5x5 km grid for the UK and clip to SAC, SPA, and SSSI boundaries.
  - Merge gridded CBED deposition data (2016–2018) with protected-site boundaries to produce site-aligned CBED data.
  - Repeat for 1x1 km NOx and SO2 concentration data from PCM.
  - Data boundary and feature lists are sourced from each country’s national websites.
- Step 2: Deriving deposition/concentration statistics per site
  - Use SQL to compute:
    - Grid-average deposition/concentration for each site by weighting grid values by grid-square area within the site boundary.
    - Sum over all grid squares overlapping a site to obtain a site-level value.
  - Deposition calculation example: CBEDDepositionValue × (GridArea / TotalSiteArea).
- CBED modelling details
  - Outputs 5x5 km grid deposition for:
    - Reduced nitrogen (NH3/NH4), oxidised nitrogen (NO2/NO3), and non-marine sulphur (SO2/SO4) to forest, moorland, grassland, arable, and urban habitats.
  - Dry deposition: uses habitat-specific deposition velocities across five land cover categories; applied according to the relative land cover in each 5x5 km grid square.
  - Wet deposition: includes precipitation-driven deposition plus occult deposition to vegetation; separates anthropogenic vs total S and Ca using sea-salt ratios.
  - Orographic enhancement: factor applied in upland regions to account for higher precipitation ion concentrations (based on Great Dun Fell and Holme Moss observations).
  - Inter-annual variability: deposition values are averaged over a 3-year period (rolling mean) to reduce year-to-year noise.
  - Three ecosystem scenarios for site-level results: moorland/short vegetation everywhere; forest everywhere; grid-average across ecosystems.
- PCM modelling details
  - Produces background concentration maps on a 1x1 km grid for the UK, plus around 9,000 road-side values.
  - One model per pollutant; includes base-year and projection models.
  - Provides outputs for scenario assessments and exposure calculations; used to support policy and TEN (Time Extension Notification) applications.

## Data inputs and outputs

- Input data sources:
  - CBED deposition data (3-year mean, 2016–2018) for nitrogen and sulfur compounds.
  - PCM concentration maps for NOx, NO2, SO2, and other pollutants.
  - Land cover information and habitat-specific deposition velocities.
  - Precipitation data and orographic factors for wet deposition.
  - Protected site boundaries and area registrations (SAC, SPA, SSSI/ASSI).
  - National boundary/feature lists for site clipping.
- Data outputs (datasets described in accompanying tables):
  - Datasets 1–3: Deposition by grid (5x5 km) for forest, moorland, and grid-average across 2016–2018.
  - Dataset 4: NH3 concentrations by grid (µg/m3) for 2016–2018.
  - Dataset 5: NOx concentrations by grid (µg/m3) for 2016–2018.
  - Dataset 6: SO2 concentrations by grid (µg/m3) for 2016–2018.
  - Datasets 7–9: Site-level deposition values (minimum, maximum, average) for forest, moorland, and grid-average across 2016–2018.
  - Dataset 10: Site-level grid-average concentrations (NO2, NH3, NOx, SO2, etc.) for 2016–2018.
  - Dataset 11: Site-level NH3 concentrations (min, max, avg) for 2016–2018.
  - Dataset 12: Site-level NOx concentrations (min, max, avg) for 2016–2018.
- Dataset structure notes (examples)
  - APIS_n_acid_dep_forest_bygrid_2016_2018.csv, APIS_n_acid_dep_moorland_bygrid_2016_2018.csv, APIS_n_acid_dep_gridavg_bygrid_2016_2018.csv: include SITECODE, SITENAME, SITEAREA, CENTROID_X/Y, COUNTRY, DESIGNATION, GRIDAREA, YEAR, and deposition components (NH3/NH4, NO2/NO3, SO2/SO4) with units keq ha-1 year-1.
  - APIS_nh3_conc_bygrid_2016_2018.csv, APIS_nox_conc_bygrid_2016_2018.csv, APIS_so2_conc_bygrid_2016_2018.csv: include site metadata plus grid-level concentrations (NH3, NOx, SO2) on 1x1 km grids.
  - APIS_n_acid_dep_forest_site_2016_2018.csv, APIS_n_acid_dep_moorland_site_2016_2018.csv, APIS_n_acid_dep_gridavg_site_2016_2018.csv: site-level min, max, and average deposition values for forest/moorland/grid-average across 2016–2018.
  - APIS_nh3_conc_site_2016_2018.csv, APIS_nox_conc_site_2016_2018.csv, APIS_so2_conc_site_2016_2018.csv: site-level concentration statistics (min, max, avg) for 2016–2018.

## Data units, interpretation, and quality control

- Units:
  - Deposition: kilo-equivalents per hectare per year (keq ha-1 year-1); conversion to kg equivalents provided (e.g., S deposition multiply by 16; N deposition multiply by 14).
  - Concentrations: micrograms per cubic metre (µg m-3).
- Data quality and validation
  - CBED methods peer-reviewed and part of Defra inter-comparison exercises.
  - Documented method development, version control, and centralized code storage.
  - Mass-balance checks and comparisons with prior-year data for consistency.
- Data structure and documentation
  - Detailed dataset descriptions, field names, units, and descriptions are provided for each dataset (1–12) and for the associated APIS files.
  - Datasets are arranged by grid (5x5 km) or by site, with 3-year rolling means and ecosystem-specific variants.

## Practical implications for data leadership

- Data discoverability and interoperability:
  - Multiple, well-structured datasets with consistent naming and clear field definitions facilitate integration with other data systems.
  - Distinct grid-resolution datasets (5x5 km deposition; 1x1 km concentrations) support both broad-scale and fine-scale analyses.
- Governance, updates, and transparency:
  - Rolling 3-year means provide stable benchmarks while allowing periodic updates as new years become available.
  - Clear QA/validation practices and external references support trust and reproducibility.
- Potential challenges to consider:
  - Managing data across different grids, ecosystems, and site boundaries requires careful metadata and lineage tracking.
  - Access to underlying boundary data and model inputs may require coordination with national bodies or Defra networks.
  - Ensuring alignment with evolving data standards and any sector-wide coordination to avoid duplicated efforts.

## References and resources

- UK Acidifying and Eutrophying Atmospheric Pollutants (UKEAP) information and supporting data:
  - http://www.pollutantdeposition.ceh.ac.uk/ukeap
  - https://uk-air.defra.gov.uk/networks/network-info?view=ukeap
  - https://uk-air.defra.gov.uk/data/pcm-data
- Related methodological and validation literature (Examples):
  - Beswick et al., 2003; Fowler et al., 1988; Dore et al., 2001, 2007; Carslaw 2011; RoTAP 2012; other Defra and peer-reviewed sources listed in the document.