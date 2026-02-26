# Historical (1950-2014) and projected (2015-2100) hydrological model (HMF-WA) estimates of monthly mean and annual maximum river flows across West Africa driven by CMIP6 projected climate data

## Overview
- Provides ensemble hydrological model estimates of monthly mean river flows (MM) and annual maximum daily flows (AM) on a 0.1° × 0.1° grid across West Africa.
- Historical (1950-2014) and projected future (2015-2100) periods driven by bias-corrected CMIP6 climate data.
- Uses two future water-use scenarios: (i) tied to projected population change and (ii) present-day water use (WO).

## What the data represent
- Grid-based, spatially-consistent river flows across West Africa (including the Sahel) at ~10 km resolution.
- Outputs include:
  - Monthly mean river flows (MM) for each grid cell and month.
  - Annual maximum of daily river flows (AM) for each grid cell and year.
- Ensemble scope:
  - 17 historical CMIP6 realizations.
  - 44 future realizations across three SSP-RCP scenarios: SSP126, SSP245, SSP585.
- Format: NetCDF4 files with metadata in headers; data dimensions: Latitude, Longitude, Time.

## Hydrological model and inputs
- Model: Hydrological Modelling Framework for West Africa (HMF-WA), grid-based and spatially distributed.
- Domain: 3°–26° N, -18° to 25° E (West Africa and Sahel).
- Key characteristics:
  - Not calibrated to individual catchments; relies on spatial datasets of physical/soil properties to configure hydrology.
  - Accounts for anthropogenic water use, wetlands, and endorheic regions.
  - Assumes future water use can vary with population (FAO, 2016) or remain at present-day levels.
- Climate inputs:
  - Daily CMIP6 precipitation and near-surface temperature (daily max/min) bias-corrected to a 0.5° × 0.5° grid over Africa.
  - Potential Evaporation (PE) derived from temperature data using established equations.
- Observations used for validation (1981-2010): GRDC river discharge data; precipitation from CHIRPS; PE from GLEAM.

## Climate scenarios and ensemble details
- SSP-RCPs used: SSP126 (low challenges), SSP245 (mid), SSP585 (high).
- Two water-use scenarios for projections:
  - With population-driven water use (FAO projections).
  - Without population change (WO).
- CMIP6 model ensemble includes 44 realizations across the three SSPs; some models have incomplete coverage for certain SSPs (noted in accompanying tables).

## Data format, naming, and access
- Primary data: monthly mean flows (MMFLOW) and annual maximum flows (AMFLOW).
- File naming convention (examples):
  - Historical MM: HMF-WA_MMFLOW_BC_<model>_HIST_195001-201412.nc
  - Future MM with SSP: HMF-WA_MMFLOW_BC_<model>_<SSP-RCP>_201501-210012.nc
  - Future MM without population change: HMF-WO_MMFLOW_BC_<model>_<SSP-RCP>_201501-210012.nc
  - AM files follow similar patterns: HMF-WA_AMFLOW_BC_...
- BC denotes bias-corrected climate input; WO denotes simulations without population-driven water-use change.
- Temporal and calendar details:
  - Calendar types vary by CMIP6 model (365/366-day Gregorian, 365-day without leap years, or 360-day 12×30-day months).
  - Data provided as monthly values and annual maxima per year.
- Spatial resolution and format:
  - 0.1° × 0.1° grid (~10 km × 10 km).
  - NetCDF4 format; readable with GIS and scientific tools (ArcGIS, QGIS, NCView, cdo, ncdump, Python/Fortran).

## Model performance and caveats
- Validation against 20 GRDC stations (1981-2010) shows:
  - Median Nash-Sutcliffe Efficiency (NSE) around 0.62.
  - Median NSE for logs around 0.82.
  - Better performance for high flows; more challenging for small/upper catchments.
- Important caveats:
  - No per-catchment calibration; potential under- or overestimation for some sites.
  - Gridded output is suitable for broad, regional analysis and ungauged locations, but not precise river reach flows for small catchments (< ~5000 km²).
  - CMIP6 baseline periods are climate-reality-driven realizations, and not direct observed flows; comparisons should be made against the same CMIP6 model runs.

## How to use in GIS
- Suitable for map-based visualization and spatial analysis of future river-flow changes under multiple climate and water-use scenarios.
- Practical applications include:
  - Mapping projected changes in monthly means and annual maximum flows across West Africa.
  - Generating flood frequency curves from annual maxima at grid cells (via Gringorten plotting positions and L-moment fitting).
  - Assessing regional flood/drought risk and planning adaptation measures.
- Limitations to consider in GIS work:
  - Coarse spatial resolution limits catchment- and river-specific analyses.
  - Ensemble should be analyzed as a whole; no single model is preferred.
  - For direct comparison to observed data, use observationally calibrated models or finer-resolution datasets.

## Applications and context
- Designed to support planning for future floods and droughts at country and regional scales.
- Enables exploration of climate-change impacts on river flows under different SSP-RCPs and water-use trajectories.
- Provides a framework to compare CMIP6-driven hydrological projections with CMIP5 outputs (RCP-based) to evaluate differences in magnitude and patterns.

## Data sources and references
- Observed discharge data: Global Runoff Data Centre (GRDC).
- Climate data inputs: CHIRPS (precipitation), GLEAM (potential evaporation).
- Water-use projections: AQUASTAT (FAO) and UN population projections.
- Hydrological framework and validation studies: AMMA-2050 project; Rameshwaran et al. (2021a, 2021b); related methodological references on bias correction and hydrological modeling.

## Acknowledgements
- AMMA-2050 project; NERC/DFID FCFA program; collaborators listed in the associated publications.