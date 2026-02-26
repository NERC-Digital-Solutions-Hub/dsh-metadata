# The energy and mass balance of Peruvian glaciers

## Overview
- Data accompany the Peru GROWS and PEGASUS projects, funded by NERC (grants NE/S013296/1 and NE/S013318/1) and CONCYTEC via the Newton-Paulet Fund.
- Peruvian component conducted under the call E031-2018-01-NERC "Glacier Research Circles" (FONDECYT Contract N° 08-2019FONDECYT).
- Associated with the paper “The energy and mass balance of Peruvian glaciers” (Fyffe et al., accepted in Journal of Geophysical Research: Atmospheres); WRF model runs and bias correction performed by Emily Potter (British Antarctic Survey) and collaborators, linked to the Peru GROWS and PEGASUS projects.
- Data are bias-corrected WRF outputs (1980–2018) at two glacier-relevant catchments in Peru, produced to support analysis of glacier energy and mass balance.

## Data generation and quality control
- Model setup
  - WRF version 3.8.1; run 1980–2018.
  - Outer domain: 12 km resolution over Peru; two inner domains at 4 km resolution covering Rio Santa (Cordillera Blanca) and Vilcanota-Urubamba catchments.
  - Physics: established schemes including Morrison double-moment microphysics, CAM radiation, Noah-MP land surface, Mellor-Yamada–Niino PBL, and Kain–Fritsch convection (domain 1 only; domains 2–3 not convective).
  - Forcing: ERA5 lateral boundary data (every 6 hours).
- Bias correction and data processing
  - Precipitation bias-corrected first for the number of wet days, then globally scaled (multiplicative correction).
  - Temperature bias-corrected: daily max corrected additively with a constant amount; daily min corrected additively with a latitude/longitude/elevation-dependent amount.
  - Elevation adjustments performed to align model and station elevations.
  - Outputs are averaged across time or across catchments; the averaged data are the dataset contents presented.
  - Model outputs interpolated to station locations using nearest-neighbour interpolation.
- Observations for bias correction
  - Precipitation and temperature observations used from in-situ stations in the study regions.
  - Five on-glacier weather stations used for extraction of outputs (see station list below).
- Coverage and scope
  - Outputs include basin-wide averages (1980–2018) and glacier-region-focused statistics (monthly and seasonal cycles).

## Data structure, contents, and units
- Time span and scope
  - 1980–2018, bias-corrected WRF outputs, averaged per catchment or across time as specified.
- Spatial and temporal structure
  - Two study catchments: Rio Santa Basin (RS) and Vilcanota-Urubamba (VUV).
  - Daily variables; aggregated as annual, monthly, and seasonal statistics.
- Key data files (examples)
  - average_annual_total_precip_RS.nc and average_annual_total_precip_VUV.nc (annual average precipitation per grid point in mm).
  - average_temperature_RS.nc and average_temperature_VUV.nc (average 2 m air temperature per grid point in °C).
  - monthly_*.csv and monthly_*_std_*.csv files (monthly cycles and standard deviations for glacierized regions and basins; units in °C for temperature, mm for precipitation).
  - seasonal_precipitation_RS.nc and seasonal_precipitation_VUV.nc (seasonal precipitation in mm).
  - WRF_elevation_RS.nc and WRF_elevation_VUV.nc (elevation in meters a.s.l.) for the respective basins.
  - Glacier-specific daily files (temperature max/min and daily precip) for Artesonraju, Cuchillacocha, Quelccaya, Quisoquipina, and Shallap glaciers (units: °C for temperature, mm for precipitation).
- Station locations (examples)
  - Artesonraju Glacier (AG), -8.9648°, -77.6357°, elevation 4797 m a.s.l.
  - Cuchillacocha Glacier (CG), -9.4054°, -77.3521°, elevation 4821 m a.s.l.
  - Shallap Glacier (SG), -9.4892°, -77.3380°, elevation 4790 m a.s.l.
  - Quelccaya Ice Cap (QIC), -13.9197°, -70.8165°, elevation 5650 m a.s.l.
  - Quisoquipina Glacier (QQG), -13.7944°, -70.8852°, elevation 5180 m a.s.l.
- Data provenance and references
  - Data and methods align with CAM 3.0 (Collins et al. 2004), ERA5 reanalysis (Hersbach et al. 2020), SRTM (Jarvis et al. 2008), and Noah-MP land surface model (Niu et al. 2011).
  - Supporting methodology for WRF and related parameterizations described in cited literature (e.g., Jiménez et al. 2012; Ma & Tan 2009; Morrison et al. 2005; Nakanishi & Niino 2004).

## Potential uses for analysts
- Analyze spatial-temporal patterns of precipitation and temperature in glacierized regions to identify drivers of energy and mass balance.
- Develop or validate predictive models of glacier response under historical climate forcing (1980–2018).
- Compare bias-corrected model outputs with in-situ observations to assess model performance at local scales.
- Use glacier-region monthly and seasonal statistics to examine seasonal cycles and variability in energy fluxes.
- Integrate with other datasets or models to study glacier hydrology, runoff, and regional climate impacts in Peru.

## References
- Collins, W.D. et al. (2004). Description of the NCAR Community Atmosphere Model (CAM 3.0).
- Hersbach, H. et al. (2020). The ERA5 global reanalysis.
- Jarvis, A. et al. (2008). Hole-filled SRTM for the globe.
- Jiménez, P.A. et al. (2012). Revised WRF surface layer formulation.
- Ma, L.-M., & Tan, Z.-M. (2009). Cumulus parameterization improvements.
- Morrison, H.C.J.A. et al. (2005). Double-moment microphysics parameterization.
- Nakanishi, M., & Niino, H. (2004). Improved Mellor-Yamada boundary layer model.
- Niu, G.-Y. et al. (2011). The Noah-MP land surface model.
- Pfeffer, W.T. et al. (2014). The Randolph Glacier Inventory.