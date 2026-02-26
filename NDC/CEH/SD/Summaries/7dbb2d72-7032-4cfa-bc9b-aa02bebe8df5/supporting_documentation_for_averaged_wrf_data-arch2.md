# The energy and mass balance of Peruvian glaciers

## Overview
- Data produced under the Peru GROWS and PEGASUS projects (funded by NERC and CONCYTEC) focusing on glacier energy and mass balance in Peru.
- Associated with the paper: Fyffe et al. (accepted) The energy and mass balance of Peruvian glaciers, Journal of Geophysical Research: Atmospheres.
- WRF model runs and bias correction conducted for two Peruvian catchments: Rio Santa, Cordillera Blanca, and Vilcanota-Urubamba (Cordilleras Vilcabamba, Urubamba, Vilcanota).
- Data intended to support environmental monitoring and policy-relevant analysis of glacier and climate dynamics.

## Data generation and quality control
- WRF model version 3.8.1 run from 1980–2018 with three domains:
  - Outer domain: 12 km resolution over Peru (20°S to 1.9°N; 84.5°W to 64.9°W)
  - Inner domains: 4 km resolution over Rio Santa and Vilcanota-Urubamba catchments.
- Forcing and configuration:
  - Lateral boundary forcing from ERA5 (every 6 hours).
  - One-way nesting with spectral nudging above model level 15.
  - Physical schemes: Morrison double moment microphysics; CAM radiation; Revised MM5 surface layer; Noah-MP land surface; Mellor-Yamada Niino PBL; Kain-Fritsch convection in domain 1.
  - Snow cover, cloud effects, and other surface processes enabled.
  - Spin-up: 1 month per year; each year run separately.
- Bias correction and QA/QC:
  - Temperature adjusted for elevation difference between model and stations using model-derived lapse rates.
  - Precipitation bias corrected first for wet-day frequency, then magnitudes via a constant multiplicative factor.
  - Daily outputs averaged over each catchment or over time; outputs also interpolated to on-glacier weather stations.
- Outputs:
  - Daily maximum/minimum temperatures and total precipitation for 1980–2018.
  - Outputs bias-corrected and averaged for presentation in this dataset.
  - Five on-glacier weather stations used for bias correction: Artesonraju (AG), Cuchillacocha (CG), Shallap (SG), Quelccaya Ice Cap (QIC), Quisoquipina (QQG).

## Data structure and units
- The dataset includes multiple files describing area-averaged, region-specific, and glacier-related climate variables.
- Key file groups and contents:
  - average_annual_total_precip_RS.nc: Average total precipitation per year in Rio Santa Basin (mm).
  - average_annual_total_precip_VUV.nc: Average total precipitation per year in Vilcanota-Urubamba (mm).
  - average_temperature_RS.nc: Average 2 m temperature in Rio Santa Basin (°C).
  - average_temperature_VUV.nc: Average 2 m temperature in Vilcanota-Urubamba (°C).
  - monthly_*_RS.csv / monthly_*_VUV.csv: Monthly cycle data (temperature and precipitation) for each region, including means and standard deviations.
  - seasonal_precipitation_RS.nc / seasonal_precipitation_VUV.nc: Seasonal average precipitation (mm) for each grid point within basin regions.
  - WRF_elevation_RS.nc / WRF_elevation_VUV.nc: Elevation data in the WRF model domain (m a.s.l.).
  - Glacier-specific daily maximum/minimum temperatures and daily precipitation:
    - Artesonraju_glac_maximum_daily_temperature.txt
    - Artesonraju_glac_minimum_daily_temperature.txt
    - Artesonraju_glac_precip.txt
    - Cuchillacocha_glac_maximum_daily_temperature.txt
    - Cuchillacocha_glac_minimum_daily_temperature.txt
    - Cuchillacocha_glac_precip.txt
    - Quelccaya_maximum_daily_temperature.txt
    - Quelccaya_minimum_daily_temperature.txt
    - Quelccaya_precip.txt
    - Quisoquipina_maximum_daily_temperature.txt
    - Quisoquipina_minimum_daily_temperature.txt
    - Quisoquipina_precip.txt
    - Shallap_maximum_daily_temperature.txt
    - Shallap_minimum_daily_temperature.txt
    - Shallap_precip.txt
- Units:
  - Precipitation outputs: mm (monthly totals or annual totals depending on file)
  - Temperature outputs: °C
  - Elevation: m a.s.l.

## Spatial domains and on-glacier data
- Domains:
  - Domain 1: 12 km resolution (outer)
  - Domains 2 and 3: 4 km resolution (inner)
- Study catchments cropped within the blue outlines shown in the project figures.
- On-glacier weather stations used for bias correction:
  - Artesonraju Glacier (AG)
  - Cuchillacocha Glacier (CG)
  - Shallap Glacier (SG)
  - Quelccaya Ice Cap (QIC)
  - Quisoquipina Glacier (QQG)

## Glacier regions and outputs
- Glacier-region outputs include daily, monthly, and seasonal climate metrics for glacierized areas within Rio Santa and Vilcanota-Urubamba basins.
- Outputs provide context for energy and mass balance analyses, enabling comparisons across basins and glacierized regions.

## Use and accessibility
- Data generation supports monitoring of environmental health and glacier-climate interactions, aligning with the Analysts Monitoring the Environment archetype’s aim to provide standardized, QA‑ed data for policy and health assessments.
- Outputs are organized and stored as netCDF and CSV files, with clear naming conventions detailing region, variable, and temporal aggregation.
- Bias-corrected data and the use of established weather stations enhance data reliability for temporal trend analyses and cross-study comparisons.

## References
- Model and data references include key WRF physics and data sources:
  - WRF Version 3.8.1 documentation (Skamarock et al., 2008)
  - ERA5 reanalysis (Hersbach et al., 2020)
  - CAM 3.0 (Collins et al., 2004)
  - Noah-MP land surface model (Niu et al., 2011)
  - Mountain glacier inventories and supporting material (Randolph Glacier Inventory; Pfeffer et al., 2014)
  - Additional model scheme references (Morrison et al., 2005; Nakanishi & Niino, 2004; Jiménez et al., 2012; Ma & Tan, 2009)
- Data and project funding:
  - Peru GROWS and PEGASUS projects; Newton-Paulet Fund; CONCYTEC.