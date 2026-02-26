# Ozone flux, dynamic global vegetation, and carbon storage modelled data of tropical forests using the Joint UK Land Environment Simulator (JULES), 1900-2015

- GIS-ready, spatially explicit dataset modelling ozone (O3) impacts on tropical forests using JULES v5.6 at a 1.25° latitude × 1.875° longitude grid.
- Covers extant, current-secondary, and potential-secondary forest extents, with preindustrial (1900–1910) and recent (2005–2014) O3 concentrations; provides both input conditions and model outputs related to NPP and carbon pools.

## What is included

- Gridded data (19 files) at 1.25° × 1.875° resolution:
  - Forest cover types: Current forest, Secondary forest, Potential forest; includes fractional cover and grid-cell area.
  - Ozone concentrations: O3_PI (1900–1909), O3_PD (2005–2014), and O3_change (1900–2014).
  - O3 exposure summaries for forest types: SSP_2050.csv (present-day and 2050 O3 for current, secondary, and potential forest types under different SSPs).
- Model outputs and summaries:
  - JULES_susceptibility.csv: three calibrated O3 susceptibility levels (Low, Moderate, High) with relative NPP decline and POD1 values.
  - NPP decline grids: Low_NPP.nc, Mod_NPP.nc, High_NPP.nc and corresponding percentage declines (Low_NPP_per.nc, Mod_NPP_per.nc, High_NPP_per.nc).
  - Delta_carbon.csv: yearly changes in vegetation and soils carbon (Pg-C) for high, moderate, and low O3 susceptibility.
  - Forest_types_NPP_Low.csv, Forest_types_NPP_Mod.csv, Forest_types_NPP_High.csv: per-forest-type (Current, Secondary, Potential) NPP declines by Julian day with area weighting.
- Calibrated and supporting data:
  - Calibration figures and parameters for BET-Tr tropical broadleaf evergreen PFT (alpha values for low, moderate, high susceptibility).
  - Data and metadata on model inputs (CO2, land-use change, CRU-JRA v2.3 meteorology) and spin-up (1900–1920).

## Spatial, temporal, and methodological scope

- Spatial: Global tropical forests modeled on a 1.25° × 1.875° grid; grid-cell area and fractional forest covers provided for current, secondary, and potential forests.
- Temporal: Pan-tropical simulations from 1900 to 2014 (with a 1000-year spin-up); focused comparisons between fixed preindustrial O3 and transient O3 forcing over 1900–2014.
- Model and inputs:
  - JULES v5.6, with an ozone damage scheme affecting net photosynthesis and stomatal conductance via a damage factor F (based on a sensitivity parameter α and a flux threshold y).
  - Calibration of α for tropical BET-Tr PFT to reproduce observed O3 susceptibilities; α values differ by susceptibility level.
  - Forcing: CO2 trajectories and land-use changes from Global Carbon Budget 2020; meteorology from CRU-JRA v2.3; O3 fluxes derived from UKESM1 CMIP6 historical data.
  - Top-canopy O3 flux used for calibration alignment with DO3 SE measurements.

## Data structure and accessibility for GIS

- Data are provided as gridded NetCDF files for each variable and CSVs for summaries and calibration.
- Outputs enable map-based analyses of:
  - Spatial distribution of forest types and their O3 exposure.
  - Relative and absolute declines in NPP by forest type and susceptibility level.
  - Changes in terrestrial carbon pools (vegetation and soils) across the 1900–2014 period.
  - Potential impacts on nature-based climate solutions via secondary and regenerated forests.

## How the data were produced and validated

- JULES simulations: fixed vs transient O3 scenarios; homogeneous O3 susceptibility levels across tropical trees; canopy-layer O3 flux considered for calibration consistency.
- Validation and quality control:
  - Model outputs examined against prior JULES applications and CMIP6 contexts.
  - Regridding and area-weighted aggregation used to align binary forest maps with the JULES grid.
- Data provenance:
  - Regridding and geospatial alignment performed with Google Earth Engine.
  - Geography aligned to Natural Earth features for regional delineation and mapping.

## Potential GIS and policy applications

- Map-based assessment of how O3 exposure could reduce tropical forest productivity and carbon storage over the 20th century and into the 2050s under different SSP scenarios.
- Evaluation of nature-based solutions and forest restoration planning under ozone pressure (areas of secondary and potential forests).
- Spatial decision-support for climate policy, forest management, and air-quality solutions linking O3 exposure to carbon cycle impacts.

## References and data access

- Data and model descriptions are linked to key literature on JULES, ozone impacts, and CMIP6 forcing.
- Primary data deposit includes gridded outputs and summary CSVs (19 gridded files plus multiple CSV/NPP files), plus documentation on calibration and methodology.