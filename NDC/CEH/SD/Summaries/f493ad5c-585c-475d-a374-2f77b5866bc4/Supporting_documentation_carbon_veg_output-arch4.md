# Supporting documentation

- Purpose and content
  - Presents a dataset of modelled vegetation carbon output from the JULES land surface model, alongside the input temperature and rainfall data.
  - Outputs are monthly with a 1.5 km resolution.
  - Four simulations: two climate projections (from HadRM3-PPE-UK ensemble) under constant present-day CO2 and under a CO2 pathway following the SRES A1B scenario.

- Climate drivers and scenarios
  - Climatology downscaled from a 25 km × 25 km grid to 1.5 km × 1.5 km.
  - Climate sensitivity configurations include 3.5 K (standard) and 7.1 K (highest-sensitivity ensemble member).
  - Present-day CO2 fixed at 386.5 ppm; A1B CO2 pathway applied for the second set of simulations.

- Model and provenance
  - Uses the JULES community land surface model (led by the UK Met Office and Centre for Ecology and Hydrology).
  - Data produced with JULES version vn4.9; model configuration documented in the Rose suite under branch 'transient_25km_drive' (u-ao645).
  - Access to JULES data requires registration on the JULES repository.

- Data structure and access
  - File format: NetCDF (.nc) files.
  - Each file includes: a lat/lon grid, a time series for monthly midpoints, and the respective dataset.
  - Directory structure reflects climatology and CO2 scenario:
    - 35K and 71K directories (two climatologies)
    - Within each, Const_CO2 and CO2 subdirectories
    - Each subdirectory contains 3 NetCDF files (e.g., Temp_35K_Const_CO2.nc for temperature under the 3.5 K, constant CO2 scenario)
  - Outputs provided for temperature, rainfall, and vegetation carbon.

- Quality control and reliability
  - JULES is a community-supported model; access contingent on registration.
  - Documentation and configuration details are linked to the Rose repository and JULES repository; versioning and parameters are specified to support reproducibility.

- Usage considerations and potential data gaps
  - Data are high-resolution gridded climate and vegetation carbon outputs suitable for regional analyses and cross-network comparisons.
  - Access may involve registration barriers; data licensing and discoverability depend on repository policies.
  - Clarity on metadata (units, variable definitions) is provided via NetCDF conventions and accompanying documentation (not fully detailed here).

- References
  - Nakicenovic, N.; Alcamo, J.; Davis, G. et al. (2000). IPCC Special Report on Emission Scenarios (A1B context referenced).