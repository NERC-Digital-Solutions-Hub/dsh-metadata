# Metadata pertaining to EIDC submission: 'Carbon dioxide and methane fluxes and associated environmental observations from paired burned/unburned peatland undergoing restoration'

## Overview
- Time series of land surface–atmosphere exchanges including net ecosystem CO2 exchange (NEE), methane (CH4), sensible heat (H), and latent heat (LE), plus meteorological observations.
- Two blanket bog sites at Forsinard RSPB Reserve, Flow Country, Caithness and Sutherland, Scotland.
- Context: former forestry plantation felled in 2017 as part of peatland restoration; large wildfire occurred May 2019.
- Sites: UK-DKF (burned area within wildfire footprint) and UK-DKE-RESTORED (protected from fire; instrumentation located nearby; swapped meters from original location).
- Period covered: 25/09/2019–20/05/2021 (with substantial data gaps; monitoring until 16/10/2020 affected by sonic anemometer and power supply issues; some data after 2021 with gaps due to power/logger faults and COVID-19 travel restrictions).

## Experimental design and sampling regime
- Paired site design to compare burned vs. restored/ungrazed peatland under restoration.
- Fluxes and micrometeorology sampled with eddy covariance (EC) systems at multiple heights; data processed to 30-minute intervals.
- Meteorological observations aggregated to 30-minute intervals; additional micrometeorological variables collected near EC mast.

## Measurements and data coverage
- Fluxes: 30-minute densities for CO2 (NEE), CH4, LE, and H derived from 20 Hz raw data.
- Meteorology: 30-minute intervals for air temperature (Ta), relative humidity (RH), precipitation, radiation components, soil variables, and water table depth.
- Key time window: 25/09/2019–20/05/2021; data capture until 16/10/2020 impacted by sonic anemometer/power issues; post-2020 data further affected by power supply and data logger faults.

## Collection methods and instrumentation
- EC system: enclosed-path setup for LE and H; open-path CH4 measurements.
- Sonic anemometers: Windmaster Pro at 2.3 m (RESTORED) and 2.55 m (FIRE) above surface; measurements of turbulent components (u, v, w) and sonic temperature.
- Gas analyzers: LI-7200 for water vapor and CO2; Li-7700 for CH4.
- Additional measurements: air temperature (Ta) and relative humidity (RH) at 2 m; net radiation (Rn), incoming shortwave radiation (Rg), photosynthetically active radiation (PPFD); soil heat flux (G), soil temperature (Tsoil), soil volumetric water content (VWC); precipitation; water table depth (WTD).
- Sensor deployment: fetch along SW wind direction ~300 m; canopy height ~0.25 m at RESTORED; vegetation semi-evergreen with deer grazing in the area.

## Data processing and quality assurance
- Flux calculations: using EddyPRO software (v7.0.6) with 30-minute blocks.
- Data screening and corrections: outlier screening; 2D rotation of sonic data; correction for imperfect cosine response, time lags, cospectral attenuation, humidity influence, and density effects; CO2 storage considered negligible; NEE assumed equal to turbulent CO2 flux.
- Sign convention: positive fluxes from ecosystem to atmosphere; negative fluxes opposite.

## Calibration and data quality flags
- Instrument calibration: gas analyzers calibrated per manufacturers' instructions; spans and zero checks not possible on-site during data capture due to remoteness; June 2021 zero/span check performed with no significant drift.
- Quality control: dataset submitted without full screening due to patchy data capture; quality flags included for future users.
- Flags: detailed flag scheme with 000 (raw), 001 (primary), 002 (calibrated), 003 (no data), 004 (removed faulty data), interpolation/fill flags (01#, 02#, 03#, 04#), and Mauder & Foken 2004 flag coding (2##, 3##). Maximum interpolation gap: 1 hour.

## Data structure and contents
- Single CSV file with extensive columns including:
  - DateTime; soil moisture content (SWC_1_1_1, SWC_2_1_1, SWC_3_1_1) and flags
  - Soil temperatures (Ts_1_1_1, Ts_2_1_1, Ts_3_1_1) and flags
  - Air temperature (Ta_1_1_1) and flag
  - Relative humidity (RH_1_1_1) and flag
  - Photosynthetic photon flux density (PPFD_1_1_1) and flag
  - Net radiation (Rn_1_1_1) and flag
  - Incoming shortwave radiation (Rg_1_1_1) and flag
  - Precipitation (P_rain_1_1_1) and flag
  - Water table depth (WTD) and flag
  - Soil heat flux (G) and flag
  - Sensible heat flux (H) and flag
  - Latent heat flux (LE) and flag
  - Net ecosystem CO2 exchange (co2_flux) and flag
  - Water vapor flux (h2o_flux) and flag
  - Methane flux (ch4_flux) and flag
  - CO2, H2O, CH4 mixing ratios (co2_mixing_ratio, h2o_mixing_ratio, ch4_mixing_ratio) and flags
  - Gas-related variables (u*, L, wind_speed, wind_dir, (z-d)/L) and flags
- Column-level descriptions and units provided in the metadata; the dataset aims to be as complete as possible given field conditions.

## Data availability and accessibility
- Raw data, mixing ratio data, and processed fluxes supplied to maximize usability.
- Metadata and detailed instrument and processing references provided to enable reproducibility and cross-study comparability.

## Notable limitations and considerations
- Substantial data gaps due to equipment power issues, weather, site management, and COVID-19 travel restrictions.
- Post-16/10/2020 gaps and ongoing power/logger faults reduced continuous data coverage.
- Calibration limitations due to remote site constraints; on-site span/zero checks were not feasible during most of the recording period.

## References
- Mauder, M. et al. (2013) A strategy for quality and uncertainty assessment of long-term eddy-covariance measurements.
- Vickers, D. & Mahrt, L. (1997) Quality Control and flux sampling problems for tower and aircraft data.
- Wilczak, J. M. et al. (2001) Sonic anemometer tilt correction algorithms.
- Nakai, T. et al. (2006) Correction of sonic anemometer angle of attack errors.
- Moncrieff, J. B. et al. (1997) A system to measure surface fluxes of momentum, sensible heat, water vapour and carbon dioxide.
- Moncrieff, J. B. et al. (2004) Averaging, detrending and filtering of eddy covariance time series.
- Schotanus, P. et al. (1983) Temperature measurement with a sonic anemometer.
- Webb, E. K. et al. (1980) Correction of flux measurements for density effects due to heat and water vapour transfer.