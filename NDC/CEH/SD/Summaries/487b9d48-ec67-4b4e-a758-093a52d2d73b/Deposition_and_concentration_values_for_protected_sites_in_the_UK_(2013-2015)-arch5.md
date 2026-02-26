# CBED Modelling and PCM Modelling for UK Protected Sites: Spatial Mapping and 3-Year Means (2013-2015)

## Overview
- Documents the process and datasets for mapping deposition and pollutant concentrations to UK protected sites (SAC, SPA, SSSI) using CBED and PCM models.
- Outputs include 3-year means (2013–2015) at 5x5 km grid resolution for site-level deposition and 1x1 km grid resolution for NOx and SO2 concentrations.
- Data are sourced from national and NGO data repositories (e.g., JNCC, UK national websites) and used to assess ecosystem-specific deposition and potential exceedances.

## Step 1: Spatial Mapping to Protected Sites
- Use Feature Manipulation Engine (FME) to create a UK-wide 5x5 km grid.
- Clip grid to boundaries of SAC, SPA, and SSSI to produce gridded site datasets.
- Merge gridded site data with 3-year CBED output (2013–2015) to create a UK protected sites CBED dataset.
- Repeat the process for 1x1 km NOx and SO2 concentration datasets based on the PCM model.
- Data boundaries and feature lists for protected sites downloaded from JNCC and national websites.

## Step 2: Deriving Minimum, Maximum, and Grid-Average Values
- Compute minimum, maximum, and grid-average deposition/concentration values for each protected site using SQL on the gridded dataset.
- Grid-average calculation: GridArea / TotalSiteArea multiplied by the site CBED deposition value, summed across grids (Formula provided: CBEDDepositionValue × (GridArea / TotalSiteArea)).
- Outputs include site-level deposition and concentration metrics, with 3-year means.

## CBED Modelling (Concentration-Based Estimated Deposition)
- CBED generates 5x5 km resolution maps of wet and dry deposition for S, N, and base cations from air concentrations and precipitation data.
- Data sources: UKEAP network measurements; interpolated site concentrations; precipitation-derived wet deposition; dry deposition via land-cover-specific deposition velocities for five land-cover categories (forest, moorland, grassland, arable, urban).
- Wet deposition includes occult deposition (cloud droplets) and accounts for an orographic enhancement factor in upland regions.
- Dry deposition covers gases (SO2, HNO3, NO2, NH3) and PM components (sulfate, nitrate, ammonium, Ca, Mg).
- Critical-load exceedances apply moorland to non-woodland and forest to woodland habitats.
- Inter-annual variability exists; deposition values averaged over three years to smooth fluctuations.
- Outputs are annual values presented as rolling 3-year means across ecosystems:
  - Three ecosystem-specific scenarios: moorland/short vegetation, forest, and a grid-average across ecosystems.

## PCM Modelling (Pollution Climate Mapping)
- PCM produces background maps and 1x1 km grids of pollutant concentrations (NOx, NO2, PM10, PM2.5, SO2, etc.) for the UK.
- Purpose: fulfill EU Directive 2008/50/EC reporting requirements; used for scenario assessment, population exposure calculations, and TEN (Time Extension Notification) applications.
- Runs per pollutant with a base year and projection model; includes around 9,000 representative roadside values.

## Data Values, Units, and Conversions
- Deposition values: expressed as keq ha^-1 year^-1; can be converted to kg S ha^-1 year^-1 (multiply by 16) or kg N ha^-1 year^-1 (multiply by 14).
- Concentration values: expressed as µg m^-3.
- The dataset includes conversions and notes on total nitrogen deposition (NO2/NO3 + NH3/NH4).

## Quality Control and Validation
- Methods aligned with government QA for analytical models; CBED data subject to extensive peer review and model inter-comparison (e.g., Carslaw 2011).
- Documentation practices include versioning, central code storage, and extensive peer-reviewed publications.
- Mass-balance checks and comparisons to previous years conducted to ensure numerical consistency.

## Data Structure and Datasets
- Dataset 4: 3-year mean concentrations of ammonia at SAC/SPA/SSSI grid squares (5x5 km).
- Datasets 1–3: 3-year mean ecosystem-specific deposition (NM-NH3/NH4, NO2/NO3, SO2/SO4 NM) for moorland or forest/woodland at 5x5 km grid resolution.
- Dataset 5: 3-year mean NOx concentrations at 1x1 km grids.
- Datasets 6: 3-year mean SO2 concentrations at 1x1 km grids.
- Datasets 7–9: 3-year mean deposition values (min, max, average) for NM-NH3/NH4, NO2/NO3, SO2/SO4 NM at 5x5 km resolution.
- Dataset 10: 3-year mean ammonia concentrations (min, max, average) at 5x5 km.
- Dataset 11: 3-year mean NOx concentrations (min, max, average) at 1x1 km.
- Dataset 12: 3-year mean SO2 concentrations (min, max, average) at 1x1 km.
- The files APIS_srcl_... and related CSVs include per-site attributes (SITECODE, SITENAME, SITEAREA, GRIDAREA, YEAR), geometry coordinates, designation (SAC/SPA/SSSI), and depositing/concentration metrics across forest/moorland/grid-average contexts.

- Example dataset fields include:
  - SITECODE, SITENAME, SITEAREA (hectares), CENTROID_X, CENTROID_Y, COUNTRY, DESIGNATION (SAC/SPA/SSSI), GRIDAREA (overlap area), YEAR (mid-year of the rolling average).
  - Depositional values by habitat type (forest: NH3/NH4, NO2/NO3, SO2/SO4 NM), and grid-average values.
  - Concentration metrics: NH3_CONC, NO2_CONC, SO2_CONC (µg m^-3) with min/max/avg statistics.

## Data Availability and References
- Resource locators include:
  - UK EAP/ukeap-related information and datasets
  - UK Air DEFRA PCM data portal
- Key references cited for model development and validation (e.g., Beswick et al., Dore et al., Fowler et al., Stedman et al., RoTAP).

## Governance Considerations for Data Stewards
- Ensure timely access to 3-year mean datasets (2013–2015) at both 5x5 km and 1x1 km resolutions.
- Maintain metadata standards: site designations, grid overlap, YEAR, GRIDAREA, and per-habitat deposition/concentration fields.
- Document data lineage: CBED-derived deposition values, PCM concentration data, and how min/max/average values are produced (Step 2 methodology).
- Track data updates and versioning; preserve historical versions and record any methodological changes.
- Manage data sharing constraints: note embargoes or proprietary limitations, especially for source data from national bodies.
- Preserve accessibility via provided resource links and ensure data quality control procedures are transparent and reproducible.
- Be prepared to respond to user needs mapping (e.g., data users requiring ecosystem-specific deposition vs. grid-average values, or vice versa).