# Historical (1950-2005) and projected (2006-2099) hydrological model (HMF-WA) estimates of monthly mean and annual maximum river flows across West Africa driven by CMIP5 projected climate data

## Overview
- Provides ensemble hydrological model estimates of monthly mean river flows and annual maximum river flows on a 0.1° × 0.1° grid across West Africa for historical (1950–2005) and projected future (2006–2099) periods.
- Driven by bias-corrected CMIP5 climate data (daily precipitation, near-surface air temperature, daily max/min temperatures) to drive the HMF-WA model.
- Two future water-use scenarios are included: (i) water use varying with projected population (FAO, 2016) and (ii) water use the same as present day (WO).

## Data coverage and outputs
- Spatial resolution: 0.1° × 0.1° grid (~10 km × 10 km).
- Periods:
  - Historical: 1950–2005
  - Future: 2006–2099
- Ensemble realizations:
  - 29 historical CMIP5 realizations
  - 76 future CMIP5 realizations across RCP2.6, RCP4.5, and RCP8.5
- Outputs provided:
  - Monthly mean river flows (MM) in m3 s-1
  - Annual maximum daily river flows (AM) in m3 s-1

## Modeling framework
- Hydrological Modeling Framework – West Africa (HMF-WA) is a physically-based, grid-based model.
- Configured to simulate flows across West Africa and the Sahel, incorporating anthropogenic water use, wetlands, and local hydrological features.
- Not calibrated to individual catchments; uses spatial physical/soil datasets to configure hydrology for broad, grid-scale consistency, including ungauged locations.
- Assumptions:
  - Future per-capita water use remains at present-day (AQUASTAT) levels; future water use depends only on population for the population-driven scenario.
  - River networks, lakes, reservoirs, and wetlands are assumed not to change significantly between present day and 2100.

## Climate forcing and scenarios
- Climate inputs: bias-corrected CMIP5 data for precipitation, near-surface air temperature, daily max/min temperatures; bias correction applied to a 0.5° × 0.5° Africa-wide grid (Famien et al., 2018).
- Potential evaporation (PE) derived from temperature data (Hargreaves & Samani, 1985).
- CMIP5 ensemble includes 20, 27, and 29 members for RCP2.6, RCP4.5, and RCP8.5, respectively.
- Historical drives use CMIP5 realizations; future periods use the same CMIP5 models under the specified RCPs.

## Data format and access
- Data format: NetCDF4 files with dimensions Latitude, Longitude, and Time.
- File naming (example MM and AM products):
  - With bias correction (BC) and population-driven water use (HIST/FUTURE):
    - Monthly mean: HMF-WA_MMFLOW_BC_<model>_HIST_195001-200512.nc
    - Future: HMF-WA_MMFLOW_BC_<model>_<RCP>_200601-209912.nc
  - Without population change (WO):
    - Monthly mean: HMF-WA_MMFLOW_BC_WO_<model>_<RCP>_200601-209912.nc
  - Annual maximum: HMF-WA_AMFLOW_BC_<model>_HIST_1950-2005.nc
    - Future: HMF-WA_AMFLOW_BC_<model>_<RCP>__2006-2099.nc
    - With WO: HMF-WA_AMFLOW_BC_WO_<model>_<RCP>_2006-2099.nc
- Accessibility: Data available at the provided DOI and associated project pages; citation required for use.

## How to use the data
- Suitable for analyzing future floods and drought scenarios across West Africa and for individual countries or rivers.
- Use AM flows to construct flood-frequency curves (e.g., Gringorten plotting positions, L-moment fits) while noting potential non-stationarity.
- Compare projections by model and by RCP, but avoid direct one-to-one comparisons with observed historical river flows due to model design (not calibrated to individual catchments) and coarsened resolution.
- Data are broad-scale; individual river catchments smaller than ~5000 km2 may not be well-resolved.
- Tools: NetCDF-compatible software (e.g., ArcGIS, NCView, Xconv) or programming languages (Python/Fortran) for data extraction; NetCDF can be converted to ASCII if needed, though resulting files may be large.

## Suggested applications
- Planning for future flood and drought risks under different climate and water-use scenarios.
- Assessing how climate change could affect river flows across West Africa and within specific countries (e.g., applications to Senegal, Burkina Faso, Chad).
- Supporting policy and development planning under climate-sensitive water resources management.

## Data provenance and access details
- Context: Output from AMMA-2050 regional hydrological modelling; part of FCFA initiatives.
- Data sources:
  - CMIP5 bias-corrected climate variables (precipitation, near-surface air temperature, daily max/min temperatures) from 20 CMIP5 models; bias-corrected to Africa-scale grids (Famien et al., 2018).
  - Observed daily river discharge data from GRDC for performance assessment (1981–2010).
- Acknowledgements and references provided in the dataset documentation; data access and terms outlined in the project notes.

## Limitations and considerations
- No catchment-specific calibration; performance varies by region (better for large basins, less so for small, upland, or flashy catchments).
- Assumes minimal change in network features (rivers, lakes, reservoirs, wetlands) to 2100.
- Use the full ensemble to capture uncertainty; individual ensemble members are not designated as preferred or most reliable.
- Bias correction narrows uncertainty, but remaining uncertainty should be considered in impact assessments.