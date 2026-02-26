# Introduction to the project

- Data were created as part of the Peru GROWS and PEGASUS projects, funded by NERC (grants NE/S013296/1 and NE/S013318/1) and CONCYTEC through the Newton-Paulet Fund.
- The Peruvian component was conducted under the Glacier Research Circles call (E031-2018-01-NERC) via FONDECYT; associated with the paper “The energy and mass balance of Peruvian glaciers” (Journal of Geophysical Research: Atmospheres, accepted).
- WRF model runs and bias correction were performed by Emily Potter (BAS, UK) and with involvement from the University of Leeds, as part of the Peru GROWS and PEGASUS projects.
- The dataset provides bias-corrected model outputs to support understanding of glacier energy and mass balance in Peru.

## Data generation and quality control

- Weather Research and Forecasting (WRF) model version 3.8.1 run for 1980–2018 over:
  - Outer domain: 12 km resolution ( Peru extent).
  - Two inner domains: 4 km resolution (Rio Santa catchment, Cordillera Blanca; Vilcanota-Urubamba catchment).
- Forcing and topography:
  - Lateral boundary forcing from ERA5 (every 6 hours).
  - Terrain and land-surface data from USGS and Randolph Glacier Inventory adjustments.
- Bias correction steps:
  - Precipitation: correct wet-day frequency, then apply a multiplicative correction for magnitude.
  - Temperature: adjust 2 m air temperature for model-elevation differences; apply additive corrections (constant for max temp, latitude/longitudinal/height-dependent for min temp).
  - Model outputs interpolated to station locations (nearest-neighbor) and then averaged by catchment or across time.
- Outputs include daily maximum/minimum temperatures and total precipitation, bias-corrected and averaged over the study period.
- On-glacier weather stations (five locations) used for bias correction: Artesonraju (AG), Cuchillacocha (CG), Shallap (SG), Quelccaya Ice Cap (QIC), Quisoquipina (QQG) with specified coordinates and elevations.

## Data structure and units

- Data are organized into multiple files (NetCDF and CSV) covering catchment-wide and glacier-specific statistics:
  - Rio Santa Basin (RS) and Vilcanota-Urubamba (VUV) areas:
    - average_annual_total_precip_RS.nc (mm), average_annual_total_precip_VUV.nc (mm)
    - average_temperature_RS.nc (°C), average_temperature_VUV.nc (°C)
    - seasonal_precipitation_RS.nc (mm), seasonal_precipitation_VUV.nc (mm)
    - WRF_elevation_RS.nc (m a.s.l.), WRF_elevation_VUV.nc (m a.s.l.)
  - Glacier regions (monthly and annual cycles at glacierized regions):
    - monthly_average_temperature_*_RS.csv / VUV.csv (°C)
    - monthly_average_temperature_at_glacier_*_RS.csv / VUV.csv (°C)
    - monthly_total_precipitation_at_glacier_*_RS.csv / VUV.csv (mm)
    - monthly_total_precipitation_at_glacier_std_*_RS.csv / VUV.csv (mm)
    - monthly_total_precipitation_at_glacier_VUV.csv (mm)
    - seasonal_precipitation_RS.nc / VUV.nc (mm)
  - Glacier-specific daily values (for each glacier):
    - Artesonraju, Cuchillacocha, Quelccaya, Quisoquipina, Shallap
      - maximum_daily_temperature.txt (°C)
      - minimum_daily_temperature.txt (°C)
      - precip.txt (mm)
- Five on-glacier weather stations used for bias correction:
  - Artesonraju Glacier (AG, -8.9648°, -77.6357°, 4797 m)
  - Cuchillacocha Glacier (CG, -9.4054°, -77.3521°, 4821 m)
  - Shallap Glacier (SG, -9.4892°, -77.3380°, 4790 m)
  - Quelccaya Ice Cap (QIC, -13.9197°, -70.8165°, 5650 m)
  - Quisoquipina Glacier (QQG, -13.7944°, -70.8852°, 5180 m)

## References

- Collins et al. (CAM 3.0) - NCAR
- Hersbach et al. (ERA5 reanalysis)
- Jarvis et al. (SRTM)
- Jiménez et al. (WRF surface layer)
- Ma & Tan (cumulus parameterization)
- Morrison et al. (double-moment microphysics)
- Nakanishi & Niino (Mellor-Yamada PBL)
- Niu et al. (Noah-MP land surface model)
- Pfeffer et al. (Randolph Glacier Inventory)