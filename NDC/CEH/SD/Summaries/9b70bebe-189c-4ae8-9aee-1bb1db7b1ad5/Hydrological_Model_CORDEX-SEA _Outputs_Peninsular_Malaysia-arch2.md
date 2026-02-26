# Historical (1971-2005) and projected (2006-2099) hydrological model (HMF-Malaysia) estimates of monthly mean and annual maximum river flows across Peninsular Malaysia driven by CORDEX-SEA projected climate data

- Overview
  - Ensemble hydrological model estimates of monthly mean and annual maximum river flows (m3 s-1) on a ~1 km grid across Peninsular Malaysia.
  - Historical period: 1971–2005; projected period: 2006–2099.
  - Driven by CORDEX-SEA climate data; accounts for artificial influences via two scenarios: current artificial influences (CAI) and planned future artificial influences (FAI).

- Data and Methodology
  - Hydrological Model: Hydrological Modelling Framework–Malaysia (HMF-Malaysia), grid-based and physically-based; domain covers Peninsular Malaysia (lat 1.2°–6.8° N, lon 99.5°–104.6° E).
  - Driving Climate Data: CORDEX-SEA daily climate model outputs for precipitation and near-surface air temperature (daily max/min); daily Potential Evaporation (PE) estimated from temperature data (Oudin et al., 2005).
  - Climate Scenarios: RCP2.6, RCP4.5, RCP8.5 with ensemble members (6, 7, and 13 members respectively).
  - Model Realizations: 13 historical realizations for baseline; 26 future realizations for projections (across CAI/FAI and RCPs).
  - Artificial Influences: CAI (current transfers/diversions) and FAI (planned future influences) incorporated into simulations.
  - Note on Calibration: Model typically not calibrated to individual catchments using observed flows; emphasizes spatial consistency across the national domain, including ungauged locations.

- Format and Content
  - Outputs: grid-based monthly mean flows (MM) and annual maximum daily flows (AM) at 0.008333° × 0.008333° (~1 km) resolution.
  - File Format: NetCDF; three dimensions—Latitude, Longitude, Time.
  - Ensemble and Period Coverage:
    - Historical: 1971–2005 (driven by climate model realizations, not observed climate).
    - Future: 2006–2099 (two artificial influence scenarios across multiple RCPs).
  - File Naming Convention (examples):
    - Monthly means under CAI, historical: HMF-PM_MMFLOW_CAI_<model>_HIST_197101-200512.nc
    - Monthly means under CAI, future: HMF-PM_MMFLOW_CAI_<model>_<RCP>_200601-209912.nc
    - Monthly means under FAI, future: HMF-PM_MMFLOW_FAI_<model>_<RCP>_200601-209912.nc
    - Annual maxima under CAI, historical: HMF-PM_AMFLOW_CAI_<model>_HIST_1971-2005.nc
    - Annual maxima under CAI, future: HMF-PM_AMFLOW_CAI_<model>_<RCP>_2006-2099.nc
    - Annual maxima under FAI, future: HMF-PM_AMFLOW_FAI_<model>_<RCP>_2006-2099.nc
  - Model and Realization Details: Table 1 lists CORDEX-SEA models, driving models, calendars, and which periods/realizations are used per combination; total counts: 13 historical, 26 future realizations.

- How to Use the Data
  - Use MM and AM grids for planning future floods and drought scenarios at state/catchment scales and across Peninsular Malaysia.
  - Analyze climate-change impacts on river flows for various periods and RCPs.
  - Flood frequency analysis: fit generalized extreme value (GEV) distributions to annual maxima to derive flood-return period curves, with caveats about stationarity.

- Limitations and Considerations
  - Ensemble Ensemble: No single ensemble member is preferred; analyses should consider the full range of model outputs.
  - Observations vs. Model Realizations: Historical data derive from climate model realizations, not observed climate; direct comparison to observed flows is not appropriate.
  - Spatial Resolution: 1 km grid cannot resolve catchments smaller than ~5 km².
  - Calibration: Lack of catchment-specific calibration may affect performance relative to calibrated hydrological models.
  - Data Size: The full CORDEX-SEA ensemble is large; use provided aggregated MM and AM grids rather than attempting to download all ensemble members simultaneously.

- Performance and Validation
  - Validation performed using observed daily river discharge data at gauges across Peninsular Malaysia, with driving data from Wong et al. (2016) for precipitation and GLEAM for PE.
  - Baseline (historical) flows are climate-model realizations rather than observed climate; spatial performance assessed prior to applying climate-change scenarios.

- Data Sources and Access
  - CORDEX-SEA climate variables can be downloaded from cordex.org (Region 14: Southeast Asia-SE Asia).
  - Project context: Malaysia-Flood Impacts Across Scales (FIAS) project; UK NERC and Malaysian Ministry of Higher Education support.
  - Related references include works by Bell, Rameshwaran, Crooks, Jenkinson, Martens, Oudin, van Vuuren, Wong, and others.

- Practical Guidance for Analysts
  - For analyses, work with the MM and AM NetCDF files to capture the ensemble range rather than selecting a single member.
  - When integrating with other datasets, account for the 1 km grid scale and the fact that small catchments (<5 km²) are not resolved.
  - Use AM data for flood-frequency assessments and CC-driven changes in peak flows; use MM data to evaluate typical monthly flow changes.