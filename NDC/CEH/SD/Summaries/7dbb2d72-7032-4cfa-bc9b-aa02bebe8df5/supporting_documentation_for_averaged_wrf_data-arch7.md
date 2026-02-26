# 1 Introduction to the project

- Data were created as part of the Peru GROWS and PEGASUS projects, funded by NERC (grants NE/S013296/1 and NE/S013318/1) and CONCYTEC through the Newton-Paulet Fund.
- Peruvian component aligned with the call “Glacier Research Circles” via FONDECYT.
- Associated with the paper on the energy and mass balance of Peruvian glaciers (accepted in Journal of Geophysical Research: Atmospheres).
- WRF model runs and bias correction conducted by researchers at BAS (UK) and University of Leeds, as part of Peru GROWS and PEGASUS projects.

## 2 Data generation and quality control

- WRF model version 3.8.1 run for 1980–2018 over:
  - Outer domain: 12 km resolution covering Peru.
  - Inner domains: 4 km resolution over two study catchments — Rio Santa, Cordillera Blanca; and Vilcanota-Urubamba catchment.
- Precipitation and temperature bias-corrected against cleaned in-situ observations; outputs interpolated to station locations using nearest-neighbour.
- Pre-bias-correction step: adjust model 2 m air temperature for elevation differences using a gradient from model output.
- Bias-correction specifics:
  - Precipitation: correct number of wet days, then apply a constant multiplicative correction for magnitude.
  - Temperatures: minimum and maximum corrected additively; maximum correction is domain-wide constant, minimum correction varies with latitude, longitude, and height.
- Outputs are averaged (by catchment or time) and presented as the dataset.
- Daily max/min air temperature and total precipitation (1980–2018) extracted at five on-glacier weather stations (see Table 2 for locations).

## 3 Data structure and units

- File types and contents:
  - average_annual_total_precip_RS.nc — average annual precipitation per grid point in Rio Santa Basin, 1980–2018; units: mm.
  - average_annual_total_precip_VUV.nc — same for Vilcanota-Urubamba; units: mm.
  - average_temperature_RS.nc — average 2 m temperature per grid point in Rio Santa; units: °C.
  - average_temperature_VUV.nc — same for Vilcanota-Urubamba; units: °C.
  - monthly_average_temperature_at_glacier_RS.csv — annual cycle of temperature for glacierised Rio Santa; units: °C.
  - monthly_average_temperature_at_glacier_VUV.csv — annual cycle for glacierised Vilcanota-Urubamba; units: °C.
  - monthly_total_precipitation_at_glacier_RS.csv / monthly_total_precipitation_at_glacier_VUV.csv — monthly totals over glacierised regions; units: mm.
  - monthly_total_precipitation_RS.csv / monthly_total_precipitation_VUV.csv — monthly totals for catchments; units: mm.
  - seasonal_precipitation_RS.nc / seasonal_precipitation_VUV.nc — seasonal average total precipitation cropped to basin boundaries; units: mm.
  - WRF_elevation_RS.nc / WRF_elevation_VUV.nc — elevation in the WRF model; units: m a.s.l.
  - Artesonraju_glac_maximum_daily_temperature.txt / Artesonraju_glac_minimum_daily_temperature.txt / Artesonraju_glac_precip.txt — glacier-specific daily metrics (AG); units: °C or mm.
  - Similarly named files for Cuchillacocha (CG), Quelccaya (QIC), Quisoquipina (QQG), Shallap (SG) glaciers with maximum/minimum daily temperatures and daily precipitation; units: °C or mm.
- Glacier and region identifiers:
  - Artesonraju (AG), Cuchillacocha (CG), Shallap (SG), Quelccaya (QIC), Quisoquipina (QQG).
- Boundaries and coverage:
  - Data cropped to catchment boundaries; designed for GIS-friendly integration (rasters and tabular outputs).

## 4 References

- Key model and data sources underpinning the work, including:
  - CAM 3.0 atmospheric model description.
  - ERA5 global reanalysis.
  - SRTM elevation data (USGS).
  - Noah-MP land surface model.
  - Randolph Glacier Inventory (RGI) for glacier data.
  - WRF model components and schemes (microphysics, radiation, surface layer, land surface, PBL, convection, etc.).