# Concentration-Based Estimation of Deposition (CBED) methodology

- Purpose: Provides 5x5 km gridded estimates of deposition flux for nitrogen, sulphur, and base cations in the UK, by integrating gas/particulate concentrations, precipitation chemistry, and land-cover–specific deposition velocities.
- Core idea: Combine observations (air and precipitation) with models to estimate wet and dry deposition across five land-cover categories (forest, moorland, grassland, arable, urban), then aggregate to grid cells.

## Data sources and deposition calculation

- Dry deposition: Derived from gas and particulate concentration maps, land-cover–specific deposition velocities, and grid-cell land-cover composition.
  - Gases: SO2, HNO3, NO2, NH3.
  - Particulates: sulfate, nitrate, ammonium, calcium, magnesium.
- Wet deposition: Based on precipitation deposition plus direct deposition of cloud droplets (occult deposition), for sulphate, ammonium, nitrate, calcium, magnesium, and hydrogen (acidity). Anthropogenic vs total sulphur and calcium separated using sea-water ion ratios.
- Key input datasets:
  - NO2: PCM model (rural interpolation plus point/line sources).
  - NH3: FRAME model plus UKEAP measurements.
  - SO2: Rural measurements with urban enhancement factor.
  - Wet deposition: precipitation data with orographic enhancement for uplands.

## Temporal coverage and uncertainty

- Averaging: Individual-year estimates are uncertain; results are averaged over three-year periods to smooth variability due to weather and sparse measurements.
- Early years: Dry deposition components in earlier years were retrospectively estimated due to limited aerosol measurements, increasing uncertainty (pre-1996).

## Implementation and data products

- Implementation: Originally in Genstat; re-implemented in R. Differences with Genstat arise from spatial interpolation (kriging) and use of long-term means/orographic enhancement factors.
- Output data structure: Exported from raster to comma-separated values (CSV) in xyz format as 3-year means (current year and two preceding years).
- Land-cover weighting: Deposition in each grid cell is the weighted mean across five land-cover categories.

## Data files and field descriptions

- rCBED_Fdep_gm2y_1986-2012_gridavg.csv
  - Deposition flux per grid cell, 3-year mean, weighted by land-cover fractions.
- rCBED_Fdep_gm2y_1986-2012_forest.csv
  - Deposition to forest assuming complete forest cover in each grid cell.
- rCBED_Fdep_gm2y_1986-2012_moor.csv
  - Deposition to moorland assuming complete moorland cover in each grid cell.
- Common file format fields (example):
  - year: end-year of the 3-year period (e.g., 2012 for 2010-2012).
  - easting, northing: grid center coordinates (OS Great Britain grid).
  - H: hydrogen ion deposition (g H m^-2 year^-1).
  - NOx: oxidised nitrogen deposition (g N m^-2 year^-1).
  - NHx: reduced nitrogen deposition (g N m^-2 year^-1).
  - Ntot: total nitrogen deposition (g N m^-2 year^-1).
  - SOx: sulphur deposition (g S m^-2 year^-1).
  - xSOx: non-marine sulphur deposition (g S m^-2 year^-1).
  - Ca, Mg, CaMg: calcium, magnesium, and combined calcium+magnesium deposition (g M m^-2 year^-1).
  - Cl: chloride deposition (g Cl m^-2 year^-1).

Units: all deposition values expressed as grammes (g) per square metre per year (g m^-2 year^-1).

## Quality control and documentation

- Quality controls align with government analytical model QA standards; includes mass-balance checks and consistency with previous years.
- Peer-reviewed development and participation in Defra model inter-comparison exercises.
- Documentation practices: versioning, central code storage, and extensive publication of CBED results in peer-reviewed literature.

## Access and supporting information

- Data are linked to UK Acidifying and Eutrophying Atmospheric Pollutants and the UKEAP network.
  - UK-EUP networks: UKEAP and UK-Air DEFRA network information pages.
- References include foundational CBED methodology papers and related deposition modelling work.

## Summary for data use

- CBED provides a robust, three-year-averaged dataset of nitrogen, sulphur, and base-cation deposition at 5x5 km resolution for Great Britain, including both wet and dry components and land-cover-specific adjustments.
- Suitable for policy assessment, trend analysis, and public data exploration; caveats include greater uncertainty in earlier years and reliance on multiple models and interpolations to generate deposition fields.
- Data products are designed to support self-serve analysis and visualization, with clear formats and unit definitions to facilitate integration into broader datasets.