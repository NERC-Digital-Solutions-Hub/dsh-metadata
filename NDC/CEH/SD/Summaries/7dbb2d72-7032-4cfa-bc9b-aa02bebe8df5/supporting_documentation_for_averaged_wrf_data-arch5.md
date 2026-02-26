# The energy and mass balance of Peruvian glaciers

- This dataset compiles WRF model outputs used in the Peru GROWS and PEGASUS projects (funded by NERC and CONCYTEC) to investigate energy and mass balance of Peruvian glaciers.
- Timeframe and scope: 1980–2018, covering three domains with nested grids (outer 12 km, two inner 4 km domains) over Peru, focusing on two study catchments:
  - Rio Santa Basin (Cordillera Blanca)
  - Vilcanota-Urubamba catchment (Cordilleras Vilcabamba, Urubamba, Vilcanota)
- Data provenance: WRF model runs (version 3.8.1) driven by ERA5 forcing, bias-corrected against in-situ observations, and spatially interpolated to station locations before correction.

## Data generation and quality control

- Model setup
  - WRF v3.8.1 with three domains: outer 12 km, inner two domains at 4 km resolution.
  - Physics: Morrison double-moment microphysics, CAM radiation, Noah-MP land surface, Mellor-Yamada/Nakanishi and Niino PBL, Kain–Fritsch cumulus in domain 1.
  - Forcing: ERA5 every 6 hours; one-way nesting; spectral nudging above model level 15; topography and land surfaces from USGS/SRTM and Randolph Glacier Inventory adjustments.
  - Spin-up: yearly runs with a one-month spin-up.
- Data bias correction and processing
  - Precipitation bias-corrected for number of wet days and magnitude (multiplicative correction post-wet-day adjustment).
  - Temperature bias corrections applied to 2 m air temperature to align with station elevations (elevation adjustments using model-derived gradients; daily min/max temperature corrections with domain-constant for max and latitude/longitude/height dependence for min).
  - Model outputs averaged over time or by catchment; glacierized regions extracted for annual/seasonal/monthly statistics.
  - Outputs bias-corrected and interpolated to five on-glacier weather stations in Peru for validation.
- Outputs and data products
  - Daily and aggregated metrics derived from 1980–2018 simulations.
  - Key variables: precipitation and temperature (average over grids per basin; annual totals; monthly cycles; seasonal averages).
  - Glacier-specific data (daily max/min temperatures and daily precipitation) across multiple glaciers.
- Data quality notes
  - Bias correction relies on cleaned in-situ observations; interpolation to station locations introduces uncertainty in areas with sparse station coverage.
  - Model physics choices and domain configuration influence biases; results are presented as averaged outputs, suitable for downstream energy and mass balance studies.

## Data structure, contents, and units

- Basins and grid-averaged products
  - average_annual_total_precip_RS.nc: average total precipitation per year in Rio Santa Basin (mm)
  - average_annual_total_precip_VUV.nc: average total precipitation per year in Vilcanota-Urubamba Basin (mm)
  - average_temperature_RS.nc: average 2 m temperature in Rio Santa Basin (°C)
  - average_temperature_VUV.nc: average 2 m temperature in Vilcanota-Urubamba (°C)
- Glacier-region monthly and annual series
  - monthly_average_temperature_at_glacier_RS.csv / monthly_average_temperature_at_glacier_VUV.csv
  - monthly_average_temperature_at_glacier_std_RS.csv / monthly_average_temperature_at_glacier_std_VUV.csv
  - monthly_average_temperature_RS.csv / monthly_average_temperature_VUV.csv
  - monthly_total_precipitation_at_glacier_RS.csv / monthly_total_precipitation_at_glacier_VUV.csv
  - monthly_total_precipitation_at_glacier_std_RS.csv / monthly_total_precipitation_at_glacier_std_VUV.csv / monthly_total_precipitation_VUV.csv
- Glacier region annual/seasonal statistics
  - seasonal_precipitation_RS.nc / seasonal_precipitation_VUV.nc (seasonal totals, mm, basin-cropped)
  - WRF_elevation_RS.nc / WRF_elevation_VUV.nc (elevation in the WRF model, m a.s.l.)
- Glacier-specific daily metrics (per glacier, region)
  - Artesonraju_glac_maximum_daily_temperature.txt (°C)
  - Artesonraju_glac_minimum_daily_temperature.txt (°C)
  - Artesonraju_glac_precip.txt (mm)
  - Cuchillacocha_glac_maximum_daily_temperature.txt (°C)
  - Cuchillacocha_glac_minimum_daily_temperature.txt (°C)
  - Cuchillacocha_glac_precip.txt (mm)
  - Quelccaya_maximum_daily_temperature.txt (°C)
  - Quelccaya_minimum_daily_temperature.txt (°C)
  - Quelccaya_precip.txt (mm)
  - Quisoquipina_maximum_daily_temperature.txt (°C)
  - Quisoquipina_minimum_daily_temperature.txt (°C)
  - Quisoquipina_precip.txt (mm)
  - Shallap_maximum_daily_temperature.txt (°C)
  - Shallap_minimum_daily_temperature.txt (°C)
  - Shallap_precip.txt (mm)
- File formats
  - NetCDF (.nc) for gridded, basin-wide products
  - CSV and TXT files for glacier-specific monthly/ daily statistics
- Metadata and coordinates
  - Locations and elevations for on-glacier stations (five stations with precise lat/long/elevations)
  - Basin outlines and domain boundaries depicted in project figures
  - Clear naming conventions tying outputs to basin (RS: Rio Santa; VUV: Vilcanota-Urubamba) and glacier regions

## Provenance, funding, and references

- Projects and funding: Peru GROWS and PEGASUS (NERC grants NE/S013296/1 and NE/S013318/1; CONCYTEC Newton-Paulet Fund), with Peruvian component under E031-2018-01-NERC Glacier Research Circles.
- Publication context: Data are associated with Fyffe et al. (accepted) The energy and mass balance of Peruvian glaciers, Journal of Geophysical Research: Atmospheres.
- Data creators and roles: WRF runs and bias correction performed by researchers at the British Antarctic Survey and University of Leeds; coordination under the Peru GROWS and PEGASUS projects, with PI leadership from Francesca Pellicciotti and Duncan Quincey.

## Relevance for data stewardship

- Data governance and usability
  - Clear provenance, processing steps, and bias-correction methodology enable reproducibility and reuse for energy/mass balance analyses and glacier modeling.
  - Documented data structure, file naming, and units facilitate automated ingestion and metadata curation.
- Metadata and interoperability considerations
  - Explicit information on model version, domain configuration, forcing data, and bias-correction steps supports traceability and cross-study comparison.
  - Glacier- and basin-specific outputs, plus station coordinates used for validation, support integration with other glacier datasets.
- Potential limitations to consider
  - Dependence on ERA5 forcing and WRF physics choices may introduce domain- and model-structure biases; results are averaged over catchments and require careful interpretation for fine-scale analyses.
  - Bias-correction relies on available in-situ observations; gaps in station data may affect correction quality in parts of the basins.