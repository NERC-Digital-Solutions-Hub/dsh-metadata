# Historical (1950-2014) and projected (2015-2100) hydrological model (HMF-WA) estimates of monthly mean and annual maximum river flows across West Africa driven by CMIP6 projected climate data

## Overview
- Provides ensemble hydrological model estimates of monthly mean and annual maximum river flows (m3 s-1) on a 0.1° × 0.1° grid across West Africa for historical (1950–2014) and projected future (2015–2100) periods.
- Driven by bias-corrected CMIP6 climate outputs; explores two future water-use scenarios to envelope potential impacts.
- Part of the AMMA-2050 project aimed at understanding monsoon change and informing climate-compatible development.

## Data and modelling approach
- Hydrological Model: Hydrological Modelling Framework for West Africa (HMF-WA), a physically-based, grid-based distributed model; accounts for anthropogenic water use, wetland inundation, and regional hydrological features.
- Domain and resolution: West Africa and Sahel, 3°–26° N, -18°–25° E, 0.1° × 0.1° grid (~10 km × 10 km).
- Calibration: Parameters are not calibrated to individual catchments; relies on spatial physical/soil datasets to configure hydrology, enabling estimates at ungauged locations but with varied catchment performance.
- Data products: 17 historical and 44 future climate realizations (CMIP6) driving the model; outputs include monthly mean flows and annual maximum daily flows.
- Bias correction: Climate inputs bias-corrected; potential evaporation derived from temperature data using standard methods.

## Climate projections and scenarios
- Ensemble: 44 CMIP6 members across three SSP-RCPs (SSP126, SSP245, SSP585).
- Historical baseline: 1950–2014; Future period: 2015–2100.
- Water-use scenarios for future projections:
  - With population-driven water use (based on FAO AQUASTAT and population growth).
  - With water use the same as present day (WO).
- Purpose: provide an envelope of possible river-flow futures to reflect uncertainty in climate and water-use trajectories.

## Data format, access, and file naming
- File format: NetCDF4; provides data on Latitude, Longitude, and Time dimensions.
- Spatial resolution: 0.1° × 0.1° (approx. 10 km × 10 km).
- Available outputs:
  - Monthly mean flows (MM) for historical and future periods.
  - Annual maximum (AM) flows for historical and future periods.
- File naming conventions illustrate bias-corrected data (BC) and water-use scenario (WO) options, e.g.:
  - HMF-WA_MMFLOW_BC_<model>_HIST_195001-201412.nc
  - HMF-WA_MMFLOW_BC_<model>_<SSP-RCP>_201501-210012.nc
  - HMF-WA_AMFLOW_BC_WO_<model>_<SSP-RCP>_201501-210012.nc
- Calendar variants: 365/366-day, 365-day, or 360-day years, depending on the CMIP6 model used.

## Performance and validation
- Validation against observed daily river discharge (GRDC) for 1981–2010.
- Overall performance: high flows captured well; low flows less well.
- Median Nash-Sutcliffe Efficiency (NSE) across West Africa ~0.62; NSE-log ~0.82.
- Some catchments with poorer performance are typically small, upland, or flashy; no catchment-level calibration reduces overfitting but affects local accuracy.

## Applications and use cases
- Support planning for future floods and droughts at national and regional scales.
- Analyze climate-change impacts on river flows for countries or rivers under multiple SSP-RCP scenarios.
- Utilize AM-flow outputs for flood-frequency analyses (e.g., Gringorten plotting positions, L-moments) to derive return-period curves.
- Researchers should consider the full ensemble range (not treat any single member as preferred) and acknowledge nonstationarity in hydrological planning.

## Data limitations and uncertainties
- Not calibrated to individual catchments; may reduce accuracy in localized areas but ensures spatial consistency across ungauged sites.
- Assumes limited change in river networks, lakes, reservoirs, and wetlands between present day and 2100; future water use linked primarily to population changes.
- Coarse resolution (~10 km) limits applicability to small catchments (<~5000 km²).
- Historical runs use climate model realizations, not direct observations; comparisons to observed flows are appropriate in a statistical sense only.
- Bias-corrected climate data reduce uncertainty but do not remove all model uncertainty.

## Data management, provenance, and context
- Related to AMMA-2050, FCFA program; provides an accessible grid-based hydrological dataset for West Africa.
- Data sources include GRDC for observed river discharge; CMIP5 and CMIP6 climate projections underpin the simulations.
- Encouraged to store and reference the full ensemble of simulations to capture uncertainty; datasets are designed for integration with other environmental monitoring data and policy evaluations.

## Acronyms and references
- Key acronyms include AM, AQUASTAT, CMIP5/CMIP6, EartH2Observe, GLEAM, NSE, PE, RCP, SSP, WAS, and more.
- Documentation references include Rameshwaran et al. (2021a, 2021b), and related methodological papers on bias correction and hydrological modelling.