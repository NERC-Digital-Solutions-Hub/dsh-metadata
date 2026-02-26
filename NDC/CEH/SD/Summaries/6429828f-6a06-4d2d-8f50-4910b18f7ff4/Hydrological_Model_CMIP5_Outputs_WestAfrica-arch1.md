# Historical (1950-2005) and projected (2006-2099) hydrological model (HMF-WA) estimates of monthly mean and annual maximum river flows across West Africa driven by CMIP5 projected climate data

## Overview
- Provides ensemble hydrological model estimates of monthly mean river flows and annual maximum daily river flows on a 0.1° × 0.1° grid across West Africa.
- Covers historical (1950–2005) and projected future (2006–2099) periods using bias-corrected CMIP5 climate forcing data.
- Two future water-use scenarios are included: (i) water use tied to projected population growth, and (ii) water use equal to present day.

## Hydrological modelling framework (HMF-WA)
- Physically-based, grid-based, spatially distributed model configured for West Africa and the Sahel.
- Incorporates anthropogenic water use, wetland inundation, and endorheic regions for spatial consistency.
- Runs at 0.1° × 0.1° resolution over latitudes 3°–26° N and longitudes -18°–25° E.
- Not calibrated to individual catchments; uses physical and soil property datasets to configure hydrology, aiming for broad spatial consistency and ungauged-site applicability.
- Provides an uncertainty envelope through multiple CMIP5 climate realizations and water-use scenarios.

## Climate projections and driving data
- Uses bias-corrected CMIP5 outputs (precipitation, near-surface air temperature, daily max/min temperature) to drive HMF-WA.
- Climate scenarios: RCP2.6, RCP4.5, and RCP8.5 with multiple ensemble members (76 future realizations total; 29 historical realizations used for baseline).
- Daily potential evaporation (PE) data sourced from model temperature; PE not available directly from CMIP5 and is estimated accordingly.
- Two future water-use scenarios:
  - BC_WO: future projections with no population-driven changes in water use.
  - BC_<model>_<RCP> with population-driven water use (based on FAO AQUASTAT 2016 and UN population projections).

## Data products and file formats
- Outputs: monthly mean flows (MM) and annual maximum flows (AM) in m3 s-1.
- Format: NetCDF4 with dimensions Latitude, Longitude, Time.
- Spatial grid: 0.1° × 0.1° (~10 km × 10 km).
- Periods and ensembles:
  - Historical: 1950–2005 (29 CMIP5 realizations).
  - Future: 2006–2099 across 3 RCPs (76 realizations in total; two water-use scenarios).
- File naming conventions (examples):
  - Monthly mean with bias correction and population-driven water use: HMF-WA_MMFLOW_BC_<model>_HIST_195001-200512.nc
  - Monthly mean under future RCP: HMF-WA_MMFLOW_BC_<model>_<RCP>_200601-209912.nc
  - Future with no population change (WO): HMF-WA_MMFLOW_BC_WO_<model>_<RCP>_200601-209912.nc
  - Annual maximum with bias correction and population-driven water use: HMF-WA_AMFLOW_BC_<model>_HIST_1950-2005.nc
  - Future annual maximum: HMF-WA_AMFLOW_BC_<model>_<RCP>__2006-2099.nc
  - Future annual maximum with no population change (WO): HMF-WA_AMFLOW_BC_WO_<model>_<RCP>_2006-2099.nc

## Domain, resolution, and data characteristics
- Domain: West Africa and Sahel; lat 3°–26° N, lon -18°–25° E.
- Resolution: 0.1° × 0.1° (approx. 10 km × 10 km).
- Data characteristics:
  - Outputs do not correspond to observed river flows at specific gauged catchments; designed for spatially continuous, gridded river-flow representations.
  - No single CMIP5 model is preferred; users should analyze the full ensemble to assess uncertainty.
  - Individual river-specific interpretations should consider the coarse grid (~5,000 km² minimum catchment representation per cell).

## Model performance and limitations
- Validation (1981–2010) against GRDC observed daily flows shows:
  - Medians of NSE = 0.62 and NSElog = 0.82, indicating reasonable performance for high flows and variable performance for some sites.
  - Better performance for large, low-flux catchments; smaller, upland, or flashy catchments show poorer performance.
- Limitations:
  - No catchment-scale calibration; potential biases in regions where calibration would improve accuracy.
  - Assumptions include: future per-person water use remains at present-day levels, and river networks, lakes, reservoirs, and wetlands do not change significantly by 2100.
  - Requires bias-corrected climate inputs; acknowledges debate about bias correction reducing uncertainty but supports current practice for impact studies.

## Access, usage, and interpretation guidance
- Data access: https://doi.org/10.5285/6429828f-6a06-4d2d-8f50-4910b18f7ff4
- Data can be downloaded through the AMMA-2050/FCFA data portal; dataset requires proper citation.
- Key usage notes:
  - Do not compare CMIP5 ensemble members directly to observed historical river flows; compare ensemble members to projected future flows within the same model.
  - Ensemble spread should be used to assess uncertainty and range of potential outcomes.
  - Spatial resolution limits applicability to catchments smaller than roughly 5,000 km².
  - NetCDF format supports programmatic access (Python, Fortran, etc.) and can be converted to other formats if needed.

## Suggested applications
- Planning for future floods and droughts in West Africa and individual countries.
- Analyzing climate-change impacts on river flows under different RCPs and population-growth scenarios.
- Flood-frequency analysis using annual maximum (AM) series: ordering AMs, fitting distributions (e.g., generalized logistic) with L-moments, and deriving return-period plots.
- Use of the full ensemble to characterize uncertainty ranges rather than relying on a single realization.

## Data sources and acknowledgments
- CMIP5 bias-corrected climate inputs: AMMA-2050 project resources; bias correction methodology by Famien et al. (2018).
- Observed river discharge data: GRDC.
- Population and water-use projections: FAO AQUASTAT (2016) and UN population projections (2017).
- AMMA-2050 and FCFA program support by NERC/DFID; data preparation and submission acknowledgments included.

## References and related materials
- AMMA-2050 project context and CMIP5 dataset references.
- Model framework and performance evaluation papers (Rameshwaran et al.; Crooks et al.; Ehret et al.; Ramírez-Villegas et al.; Maraun, etc.).
- Data usage notes on bias correction and uncertainty (Ehret et al.; Maraun; Gohar et al.; Ramirez-Villegas et al.).
- Supporting figures and example outputs illustrating spatial and temporal flow patterns (e.g., Niger River examples).