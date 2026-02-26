# Supporting documentation

- Purpose
  - Provides modelled vegetation carbon output from the JULES land surface model, with accompanying monthly temperature and rainfall data at 1.5 km resolution.
  - Four simulations: two climate projections × constant present-day CO2 vs SRES A1B CO2 pathway.

- Simulation design and climate drivers
  - Climatology downscaled from HadRM3-PPE-UK ensemble (Hadley Centre, 2008) from 25 km to 1.5 km grid.
  - Climate sensitivities used: standard configuration at 3.5 K and an ensemble member with a higher sensitivity of 7.1 K.
  - CO2 scenarios: present-day value of 386.5 ppm and the SRES A1B CO2 pathway (Nakicenovic et al. 2000).

- Model and data provenance
  - Data produced with JULES version vn4.9.
  - JULES is a community-developed land surface model led by the UK Met Office and Centre for Ecology and Hydrology.
  - Reproducible via the Rose software suite (u-ao645), in the branch transient_25km_drive (registration required).

- Data structure and access
  - Data stored as NetCDF files containing:
    - latitude-longitude grids
    - monthly time midpoints
    - the variable data (e.g., temperature, rainfall, vegetation carbon)
  - Directory structure:
    - 35K and 71K directories correspond to different climatologies.
    - Each contains Const_CO2 and CO2 subdirectories.
    - Each subdirectory includes 3 NetCDF (.nc) files.
  - File naming example: Temp_35K_Const_CO2.nc (temperature for the 3.5K, constant CO2 simulation).

- Practical notes for analysts
  - Enables high-resolution assessment of vegetation carbon response to climate change under different CO2 pathways and climate sensitivities.
  - Useful for cross-scenario comparisons and regional impact analyses at 1.5 km resolution.

- References
  - Nakicenovic, N.; Alcamo, J.; Davis, G. (2000). IPCC Special Report on Emission Scenarios. Cambridge.