# Introduction to the project

- The data were created as part of the Peru GROWS and PEGASUS projects, funded by NERC (grants NE/S013296/1 and NE/S013318/1) and CONCYTEC through the Newton-Paulet Fund.
- The Peruvian component aligns with the call E031-2018-01-NERC "Glacier Research Circles" via FONDECYT (Contract 08-2019FONDECYT).
- Associated publication: a paper on the energy and mass balance of Peruvian glaciers (accepted for Journal of Geophysical Research: Atmospheres); WRF model runs and bias correction were conducted by named personnel across institutions in the UK.

## Data provenance and scope

- WRF model outputs are produced for Peru, with bias-corrected meteorological fields used for glacier/relevant catchments.
- The work is interconnected with the Peru GROWS and PEGASUS projects and relies on published model configurations and forcing data.

## Data generation and quality control

- Model: WRF version 3.8.1, run from 1980 to 2018.
- Domains and resolution:
  - Outer domain: 12 km horizontal resolution covering Peru (20°S to 1.9°N, 84.5°W to 64.9°W).
  - Inner domains: two 4 km resolutions covering Rio Santa, Cordillera Blanca (Rio Santa catchment) and Vilcanota-Urubamba catchment (Cordilleras Vilcabamba, Urubamba, Vilcanota).
- Forcing and physics:
  - Lateral forcing from ERA5 every 6 hours.
  - One-way nesting, spectral nudging above model level 15.
  - A set of specific physics schemes (including Morrison microphysics, CAM radiation, Noah-MP land surface, etc.) as detailed in the data documentation.
- Bias correction and data preparation:
  - Pre-correction: model output bias-corrected against cleaned in-situ precipitation and air temperature observations for both study regions.
  - Precipitation: corrected for the number of wet days (to address overestimation) followed by a constant multiplicative correction to adjust magnitude.
  - Temperature: minimum and maximum daily temperatures corrected additively; maximum corrected with a constant value across the domain; minimum corrected variably with latitude, longitude, and height.
  - Elevation adjustments: model air temperature at 2 m adjusted to account for elevation differences between model and station elevations.
  - Post-correction: outputs averaged over each catchment or over time, as described in section 3 of the dataset documentation.
- Data products and validation:
  - Outputs are presented as averaged datasets and include values at five on-glacier weather stations (locations listed in the documentation).
  - Table 1 describes the WRF setup; Table 2 provides the station locations and elevations.

## Data structure, content, and units

- The dataset comprises both gridded and glacier-specific time series/files, including:
  - Average annual precipitation per year at each grid point, for:
    - Rio Santa Basin (RS) — average per year (mm).
    - Vilcanota-Urubamba (VUV) — average per year (mm).
  - Average temperature at 2 m, per grid point, for RS and VUV (°C).
  - Monthly annual cycles of temperature (and standard deviations) over glacierised regions in RS and VUV (°C).
  - Monthly total precipitation over glacierised regions in RS and VUV (mm) and corresponding standard deviations.
  - Seasonal precipitation averages for RS and VUV (mm).
  - WRF-derived elevation datasets for RS and VUV (m a.s.l.).
  - Glacier-specific daily temperature maxima/minima and daily precipitation for each glacier site:
    - Artesonraju (AG) – maxima/minima daily temp (°C) and daily precip (mm).
    - Cuchillacocha (CG) – maxima/minima daily temp (°C) and daily precip (mm).
    - Shallap (SG) – maxima/minima daily temp (°C) and daily precip (mm).
    - Quelccaya Ice Cap (QIC) – maxima/minima daily temp (°C) and daily precip (mm).
    - Quisoquipina (QQG) – maxima/minima daily temp (°C) and daily precip (mm).
- File naming and content:
  - Example gridded annual data: average_annual_total_precip_RS.nc, average_temperature_VUV.nc.
  - Glacier-specific time series: Artesonraju_glac_maximum_daily_temperature.txt, Cuchillacocha_glac_precip.txt, Quelccaya_precip.txt, etc.
  - Temporal aggregation: data are presented as annual averages, monthly cycles, and seasonal aggregates, with clear units (mm for precipitation, °C for temperature, m a.s.l. for elevations).

## Data governance and accessibility (for data leadership)

- Clear documentation of data generation methods, bias correction steps, domain configurations, and file-level metadata supports reproducibility and auditability.
- Data are organized by catchment (RS, VUV), with both gridded and glacier-specific outputs, enabling end-to-end analysis from regional to site-level scales.
- The dataset includes multiple file formats (NetCDF .nc, CSV .csv, and text .txt) to support diverse analysis workflows.
- The documentation provides explicit references to model configuration, forcing data, and relevant literature, aiding traceability and future methodological updates.

## References

- Collins et al. (2004) CAM 3.0 description.
- Hersbach et al. (2020) ERA5 reanalysis.
- Jarvis et al. (2008) SRTM data.
- Jiménez et al. (2012) WRF surface layer scheme.
- Ma & Tan (2009) Convection parameterization.
- Morrison et al. (2005) Double-moment microphysics.
- Nakanishi & Niino (2004) Mellor-Yamada level-3 model.
- Niu et al. (2011) Noah-MP land surface model.
- Pfeffer et al. (2014) Randolph Glacier Inventory.