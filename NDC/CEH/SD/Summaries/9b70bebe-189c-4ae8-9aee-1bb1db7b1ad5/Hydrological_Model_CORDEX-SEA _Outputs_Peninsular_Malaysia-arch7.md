# Historical (1971-2005) and projected (2006-2099) hydrological model (HMF-Malaysia) estimates of monthly mean and annual maximum river flows across Peninsular Malaysia driven by CORDEX-SEA projected climate data

## Overview
- High-resolution grid-based hydrological dataset for Peninsular Malaysia, providing monthly mean river flows and annual maximum daily flows.
- Spatial resolution: 0.008333° × 0.008333° grid (~1 km × 1 km).
- Time coverage: historical (1971–2005) and future projections (2006–2099).
- Driven by CORDEX-SEA ensemble climate data (precipitation and near-surface temperature) to generate flows.

## Model and driving data
- Hydrological Modeling Framework: HMF-Malaysia (physically-based, grid-based, regional scale).
- Domain: Peninsular Malaysia (lat 1.2°–6.8° N, lon 99.5°–104.6° E).
- Artificial influences: two scenarios for future flows
  - CAI: current artificial influences (e.g., water transfers/diversions)
  - FAI: planned future artificial influences
- Calibration: model is not calibrated to individual catchments; uses physical/soil properties to configure hydrology for spatial consistency and ungauged locations.
- Climate projections: CORDEX-SEA multi-model ensemble with 6 RCP2.6, 7 RCP4.5, and 13 RCP8.5 realizations (total realizations listed in Table 1 of the source).
- Observational context: performance assessed against observed daily flows at Malaysian gauging stations using gridded precipitation and PE estimates, but historical runs are climate-model realizations rather than direct observations.

## Data formats and contents
- Outputs: monthly mean river flows (MM) and annual maximum daily river flows (AM) on a 1 km grid.
- Realizations: 13 historical and 26 future climate realizations (across 3 RCPs).
- File format: NetCDF with dimensions Latitude, Longitude, Time; metadata header included.
- File naming conventions illustrate combinations of era (HIST or future), CAI/FAI, CORDEX-SEA model, driving model, RCP, and period (e.g., HMF-PM_MMFLOW_CAI_<model>_<RCP>_200601-209912.nc).
- Time granularity: months for MM; annual for AM (yearly maximum of daily flows); time steps may reflect 365/366 or 360-day calendars depending on the driving climate model.
- Domain coverage and coordinate details: data available only for the Peninsular Malaysia domain; not suitable for catchments smaller than ~5 km² due to grid scale.

## How to use the data in GIS
- Suitable for map-based analyses of future flood and drought scenarios at state/catchment scales across Peninsular Malaysia.
- Ensemble approach: no single member is preferred; analyses should consider the full ensemble range for both historical and future periods.
- Comparability: individual CORDEX-SEA ensemble member can be compared to future outputs from the same member, but not directly to observed historical flows.
- River identification: rivers can be located from the georeferenced grid, but the 1 km resolution limits detailed catchment-scale drainage features below ~5 km².
- Software compatibility: NetCDF is widely supported (ArcGIS, NCView, Xarray/xconv in Python, etc.); NetCDF can be converted to ASCII if needed (resulting in very large files).
- Data access: CORDEX-SEA climate inputs available from cordex.org; projected flows provided as described above.

## Suggested applications
- Planning for future flood and drought scenarios at the state, catchment, or regional scale across Peninsular Malaysia.
- Analyzing climate-change impacts on river flows under RCP2.6, RCP4.5, and RCP8.5 scenarios.
- Investigating flood-frequency characteristics by deriving annual maximum (AM) flows and fitting generalized extreme value (GEV) distributions to return-period plots (with stationarity assumptions noted).

## Data sources and acknowledgements
- CORDEX-SEA climate inputs (precipitation and near-surface air temperature) and related data sources.
- Related datasets and methods referenced include GLEAM evaporative data, Wong et al. (2016) high-resolution rainfall dataset, and the broader Malaysia-FIAS project (funded by NERC and Malaysia’s MOHE).

## Notes and caveats
- The historical runs are model realizations rather than direct observations and should be treated statistically rather than as exact historical records.
- Spatial resolution limits applicability to small catchments; interpretation should be at relatively coarse spatial units (≥ ~5 km²).
- The dataset supports ensemble-based risk assessment but requires careful handling of calendar (365/366 vs 360-day) differences across driving models.