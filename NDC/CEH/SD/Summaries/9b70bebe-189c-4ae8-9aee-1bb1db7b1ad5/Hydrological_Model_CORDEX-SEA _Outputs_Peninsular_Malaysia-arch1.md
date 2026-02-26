# Historical (1971-2005) and projected (2006-2099) hydrological model (HMF-Malaysia) estimates of monthly mean and annual maximum river flows across Peninsular Malaysia driven by CORDEX-SEA projected climate data

- Purpose and scope
  - Provides ensemble grid-based estimates of monthly mean river flows and annual maximum river flows (both in m3 s-1) across Peninsular Malaysia on a 0.008333° × 0.008333° grid (~1 km) for historical (1971–2005) and projected future (2006–2099) periods.
  - Driven by CORDEX-SEA projected climate data (daily precipitation, near-surface air temperature, and daily max/min temps) to assess river-flow responses to climate change.
  - Includes two artificial-influence scenarios for future runs: current artificial influences (CAI) and planned future artificial influences (FAI).

- Model and methodology
  - Hydrological framework: Hydrological Modelling Framework - Malaysia (HMF-Malaysia), a physically-based grid-based model, configured to simulate flows across the Peninsular Malaysia domain (lat 1.2°–6.8° N, lon 99.5°–104.6° E).
  - Characteristics: grid-based and spatially consistent; does not calibrate to individual catchments using observed flows; leverages spatial physical and soil-property datasets to configure hydrology, enabling good estimates in ungauged locations but with possible lower performance than catchment-calibrated models.
  - Climate forcing: CORDEX-SEA ensemble with multiple driving models and RCP scenarios; historical (1971–2005) and future (2006–2099) simulations; RCP2.6, RCP4.5, and RCP8.5 representing different forcing pathways.
  - Artificial influences: CAI simulates present-day water transfers/diversions; FAI represents planned future water management changes.

- Data outputs and structure
  - Outputs include:
    - Monthly mean flows (MM) on a 1 km grid.
    - Annual maximum flows (AM) of daily river flows on a 1 km grid.
  - Temporal and scenario coverage: 13 historical realizations and 26 future realizations across the three RCPs (RCP2.6, RCP4.5, RCP8.5).
  - File formats and naming: NetCDF format with standardized naming conventions for CAI and FAI, historical and future periods (examples provided in the document).
  - Temporal resolution details:
    - Number of days per year in simulations may be 365/366 (Gregorian) or 360 (30-day months), affecting the length of annual maximum time series.

- Data interpretation and usage guidance
  - Do not treat any single CORDEX-SEA member as 'preferred' or 'most reliable'; analyses should consider the full ensemble range to reflect uncertainty.
  - Do not directly compare model-generated flows to observed historical river flows; comparisons should be made within the same CORDEX-SEA model across periods.
  - River identifiers can be linked to grid cells, but the 1 km resolution may not capture flows for catchments smaller than ~5 km².
  - Data are suitable for planning future flood/drought scenarios at state/catchment scales across Peninsular Malaysia.
  - For extreme-flow analysis, annual maxima can be used to fit generalized extreme value (GEV) distributions to derive flood-frequency curves, with caveats about stationarity over the data period.

- Access and technical notes
  - Data are provided as NetCDF files; typical tools for reading include ArcGIS, NCView, Xconv, Fortran, Python. NetCDF headers contain metadata; conversion to ASCII is possible but results in very large files.
  - The broader CORDEX-SEA climate data used to drive the model are available from cordex.org (Region 14 South-East Asia).

- Applications and use cases
  - Support planning for future floods and droughts at the state or catchment level and across Peninsular Malaysia.
  - Analyze how river-flow magnitude and seasonality respond to different climate futures (RCPs) and artificial-influence scenarios.
  - Investigate flood-frequency changes by examining annual maximum series and applying statistical methods (e.g., GEV) to assess return periods.

- Data sources and acknowledgements
  - CORDEX-SEA climate variables sourced from the CORDEX network.
  - Malaysia-FIAS project (Flood Impacts Across Scales) funded by the UK NERC and Malaysia’s Ministry of Higher Education; multiple related references and prior methodological work cited.

- References and context
  - Key methodological and contextual references related to the hydrological framework, calibration/validation approaches, and climate projections underpinning the dataset.