# Historical (1971-2005) and projected (2006-2099) hydrological model (HMF-Malaysia) estimates of monthly mean and annual maximum river flows across Peninsular Malaysia driven by CORDEX-SEA projected climate data

- What the dataset is
  - Ensemble hydrological model estimates of monthly mean river flows and annual maximum river flows (in m3 s-1) on a 0.008333° × 0.008333° grid (~1 km) across Peninsular Malaysia.
  - Covers historical period (1971–2005) and projected future period (2006–2099).
  - Driven by CORDEX-SEA climate data (precipitation, near-surface air temperature, daily max/min temperatures) and two artificial-influence scenarios: current artificial influences (CAI) and planned future artificial influences (FAI).

- Context and purpose
  - Output from the Malaysia Flood Impacts Across Scales (FIAS) project, which aims to identify flood-prone areas and potential damages/disruptions.
  - Designed to support planning for future flood and drought scenarios at state/catchment and national scales in Peninsular Malaysia.

- Hydrological modelling framework
  - Uses the Hydrological Modelling Framework (HMF-Malaysia), a physically-based grid-based model configured to simulate flows across the entire Peninsular Malaysia domain (lat 1.2°–6.8° N, lon 99.5°–104.6° E).
  - Not calibrated to individual catchments; relies on spatial datasets of physical and soil properties to represent local conditions and provide consistent gridded flow estimates, including ungauged locations.
  - Accounts for artificial influences (CAI and FAI) to reflect water transfers, diversions, and planned changes.

- Climate forcing and scenarios
  - Uses daily CORDEX-SEA climate model outputs under RCP2.6, RCP4.5, and RCP8.5 with 6, 7, and 13 ensemble members respectively.
  - Daily climate variables include precipitation and near-surface temperatures; Potential Evaporation (PE) derived from temperature using Oudin et al. (2005) equations.

- Performance and limitations
  - Performance assessed against observed daily river discharge at gauging stations using gridded precipitation (Wong et al., 2016) and PE (GLEAM); however, historical simulations are climate-model realizations rather than direct observations, so results are interpreted statistically.
  - While offering high spatial resolution, the model is not calibrated to individual catchments and may underperform compared with catchment-calibrated models.
  - Spatial resolution (~1 km) means catchments smaller than ~5 km² are not readily resolvable.

- Data format, structure, and access
  - Outputs: monthly mean river flows and annual maximum daily river flows on a 0.008333° grid for 13 historical and 26 future realizations (3 RCPs).
  - File format: NetCDF with dimensions Latitude, Longitude, and Time; metadata-rich headers.
  - Time representation: three possible days-per-year settings (365/366, 365, or 360) depending on the CORDEX-SEA model configuration.
  - File naming conventions illustrate MAE, CAI/FAI, model, driving model, RCP, and period (historical or future).

- How to use the data
  - Do not rely on a single ensemble member as the 'preferred' projection; analyze the full ensemble for current and future periods.
  - Comparisons should be made within the same CORDEX-SEA model and driving data; not directly with observed historical flows.
  - Spatially locate river signals by grid cell; the product is not suitable for very small catchments (<5 km²) due to grid-scale resolution.
  - Data can inform flood risk and drought planning, flood-frequency analysis, and adaptation strategies across states/catchments.
  - For flood-frequency analysis, annual maximum flows can be used with generalized extreme value (GEV) distributions, noting stationarity assumptions.

- Suggested applications
  - Planning for future floods and droughts at the state and catchment scales and for Peninsular Malaysia as a whole.
  - Assessing climate-change impacts on river flows under multiple RCP scenarios.
  - Analyzing flood magnitudes and return periods using AM flow data; constructing flood-frequency curves.

- Data sources and acknowledgments
  - CORDEX-SEA climate variables (precipitation, near-surface temperature) and PE inputs referenced; data accessible via cordex.org.
  - Project acknowledged as part of Malaysia-FIAS with NE/NERC and Malaysian Ministry support; multiple related methodological and data references cited.

- Data products and example usage
  - Examples of file naming: HMF-PM_MMFLOW_CAI_RegCM4-3-ICHEC-EC-EARTH_RCP8.5_200601-209912.nc (monthly mean, CAI) and HMF-PM_MMFLOW_FAI_RegCM4-3-ICHEC-EC-EARTH_RCP8.5_200601-209912.nc (monthly mean, FAI).
  - Example figures illustrate spatial and temporal variability across ensemble members for specific locations (e.g., Kelantan River) and future periods.