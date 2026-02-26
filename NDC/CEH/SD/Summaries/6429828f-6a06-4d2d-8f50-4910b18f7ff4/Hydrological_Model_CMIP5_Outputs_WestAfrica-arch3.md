# Historical (1950-2005) and projected (2006-2099) hydrological model (HMF-WA) estimates of monthly mean and annual maximum river flows across West Africa driven by CMIP5 projected climate data

- Overview
  - Provides ensemble estimates of monthly mean river flows and annual maximum daily river flows on a 0.1° × 0.1° grid across West Africa for historical (1950–2005) and projected future (2006–2099) periods.
  - Driven by bias-corrected CMIP5 climate data (precipitation, near-surface air temperature, daily max/min temperatures) to drive the HMF-WA hydrological model.
  - Two future water-use scenarios: (i) water use varying with projected population (FAO, 2016) and (ii) water use remaining at present-day levels (WO).
  - Data cover 3 RCPs (2.6, 4.5, 8.5) with 76 ensemble members (20, 27, and 29 realizations respectively) and provide both historical and future projections.
  - Aims to support planning for floods and droughts and climate-compatible development in the region.

- Data and Modelling Approach
  - Hydrological Modelling Framework West Africa (HMF-WA): grid-based, physically-based model at 0.1° resolution; accounts for anthropogenic water use, wetlands, and endorheic regions to achieve spatially consistent flows.
  - Domain: West Africa and Sahel (3°–26° N, -18°–25° E).
  - Calibration: parameters are not tuned to individual catchments; relies on spatial physical/soil properties. This yields broad spatial consistency but can underperform in some catchments.
  - Performance: assessed against observed daily flows (1981–2010); medians of NSE and NSElog are 0.62 and 0.82, respectively; better performance for high flows, poorer for small/flashy catchments.
  - Climate inputs: bias-corrected CMIP5 outputs (precipitation, near-surface temperature, daily Tmax/Tmin) bias-corrected to 0.5° × 0.5° over Africa; potential evaporation estimated from temperature.
  - Assumptions: future per-person water use remains at present-day levels; river networks, lakes, reservoirs, wetlands not expected to change significantly by 2100.

- Projections and Scenarios
  - Climate projections derived from 76 CMIP5 ensemble members across three RCPs (2.6, 4.5, 8.5).
  - Future flows simulated under two water-use scenarios: population-driven vs present-day water use (WO).
  - Results provide an envelope of possible changes in river flows and water resources across West Africa.

- Data Output and Format
  - Outputs: monthly mean flows (MM) and annual maximum flows (AM) on a 0.1° grid.
  - Format: NetCDF4; dimensions include Latitude, Longitude, and Time; includes metadata in headers.
  - File count: 29 historical realizations and 76 future realizations; no single member is designated as preferred.
  - File naming (examples): 
    - Monthly means with bias correction: HMF-WA_MMFLOW_BC_<model>_HIST_195001-200512.nc; HMF-WA_MMFLOW_BC_<model>_<RCP>_200601-209912.nc; HMF-WA_MMFLOW_BC_WO_<model>_<RCP>_200601-209912.nc
    - Annual maxima: HMF-WA_AMFLOW_BC_<model>_HIST_1950-2005.nc; HMF-WA_AMFLOW_BC_<model>_<RCP>__2006-2099.nc; HMF-WA_AMFLOW_BC_WO_<model>_<RCP>_2006-2099.nc
  - Calendar options: models may use 365/366, 365, or 360 days per year depending on CMIP5 model; up to 30-day months in 360-day setup.
  - Spatial limits: suitable for analyses at ~10 km resolution; not readily applicable to individual rivers or catchments smaller than ~5000 km².

- How to Use the Data
  - Use the full ensemble to assess uncertainty and scenario ranges; no single realization should be treated as most reliable.
  - Suitable for planning floods and droughts at national or regional scales; supports exploration of climate change impacts on river flows under different RCPs and water-use assumptions.
  - For flood frequency analyses, AM flows can be ordered by year and used with plotting positions (e.g., Gringorten) and generalized logistic distributions; note stationarity assumptions.
  - Bias-corrected outputs are commonly used, but users should recognize that bias correction can narrow the apparent uncertainty range.
  - Caution: results are gridded and may not map directly to observed river networks; not designed for precise gauging at the catchment level, especially in smaller or highly variable basins.

- Data Access and Sources
  - Data available from the AMMA-2050 Environmental Information Data Centre (EIDC): https://amma2050.ipsl.upmc.fr/CMIP5_AFRICA/ with usage terms described therein.
  - Required citation: Rameshwaran, P., Bell, V.A., Davies, H.N., & Kay, A.L. (2021). Historical (1950-2005) and projected (2006-2099) hydrological model (HMF-WA) estimates of monthly mean and annual maximum river flows across West Africa driven by CMIP5 projected climate data. NERC EDS Environmental Information Data Centre.
  - Observed river discharge data used for model assessment obtained from the Global Runoff Data Centre (GRDC).
  - Data sources for climate inputs: bias-corrected CMIP5 outputs (AMMA-2050); evaporation estimates from temperature-based formulations (GLEAM/Hargreaves-Samani).

- Limitations and Considerations
  - No catchment-scale calibration; results are optimized for broad spatial consistency rather than perfect fit to observed flows.
  - Historical period is driven by climate model realizations rather than directly observed climate data for that period.
  - Two simplifying assumptions about future hydrology (static per-capita water use and minimal changes in hydrological features) introduce uncertainty into projections.
  - The ensemble approach is essential; individual realizations should not be over-interpreted as definitive forecasts.

- Applications in Monitoring Framework Context
  - Aligns with monitoring framework goals to identify useful environmental health measures, ensure data quality, openness, and governance, and provide outputs for policy scrutiny and decision-making.
  - Explicit data accessibility, metadata, and documentation support governance and transparency; acknowledges data transformation and standardization needs (NetCDF format, grid-based outputs).
  - Highlights challenges relevant to monitoring programs: data coverage, harmonization across datasets, and communicating ensemble-based projections to decision-makers.