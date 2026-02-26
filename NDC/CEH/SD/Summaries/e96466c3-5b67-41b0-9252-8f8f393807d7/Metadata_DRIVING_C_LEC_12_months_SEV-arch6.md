# Half hourly fluxes of sensible heat, latent energy and carbon, observed by eight eddy covariance towers in the Northern Chihuahuan Desert, 2018-2019

## Overview
- Metadata for a dataset collected from eight eddy covariance towers at Sevilleta Refuge, New Mexico, USA.
- Timeframe: 2018-11-01 to 2019-11-01.
- Purpose: test design quality and examine spatial variability of fluxes across towers.
- Towers: eight REC systems plus two AmeriFlux towers (US-Seg and US-Ses); towers are 6 m tall.
- Main sensors per tower: Gill Windmaster sonic anemometer, Honeywell HIH-4000 RH sensor, Vaisala GMP343 CO2 sensor.
- Data products aimed at enabling self-serve analysis (fluxes, footprints, land cover) with guidance on use.

## Data files

- 1) to 8) Flux data for EC1–EC4 and SES EC1–EC4
  - Half-hourly data with fields such as Date_Time (center of half-hour, DD/MM/YYYY HH:mm), pressure (P ~ 84 kPa), mean_vCO2 (ppmv), mean_vT (C), mean_cRH (%), wind components and speeds, temperature, humidity, and fluxes.
  - Variables include: cLEc (latent heat flux, post frequency response correction), Hc (sensible heat flux, post correction), Fcc (net ecosystem exchange post correction), friction_velocity, MO_stability, and footprint-related indicators.
  - Flux signs: NEE negative indicates a terrestrial carbon sink.
  - Data quality: tiny gaps due to maintenance; spikes removed with Tukey-based filtering (k = 30).
  - Time lags for gases and heat: H, LE, NEE time lags (0, 5.5, 7 seconds respectively) determined via covariance analysis; water lag constant across RH 5–90%.
  - Data format notes: some fields may contain 0 (e.g., certain correlation metrics); missing values represented as blanks.
- 9) to 12) Footprint 80% for SEG EC1–EC4
- 13) to 18) Footprint 80% for SEG/SES EC0 and SES EC1–EC4
  - Footprint coordinates in x (Easting) and y (Northing) in UTM 13N, NAD83.
  - Coverage corresponds to the 80% flux footprint area incorporating the ten towers (eight REC plus US-Seg and US-Ses).

- 19) to 20) Land cover extracts
  - Land cover maps within a 440 m radius centered on US-SEG and US-SES.
  - Categories: 0 = barren, 1 = shrubland, 2 = herbaceous, 4 = (noted, likely a category in data).

## Data collection and processing

- Field setup: eight REC towers and two AmeriFlux towers; sensors and tower details described above.
- Data processing workflow:
  - Raw EC data pre-processed with EdiRe v1.5.0.32, including spike detection, coordinate rotation, frequency response correction, cross-covariance adjustments, and WPL corrections.
  - Gap-filling of half-hourly data performed using REddyProc (R v1.2) with season-specific u* filtering.
  - Cospectral analysis conducted with a Hamming window, segment size 512, and 30 frequency bins to derive frequency-specific correlations.

## Data structure and units

- Date_Time: Center of half-hour interval (DD/MM/YYYY HH:mm).
- P: Air pressure (kPa) ~ constant 84 kPa.
- mean_vCO2: CO2 concentration from Vaisala (ppmv).
- mean_vT: Air temperature (C).
- mean_cRH: Relative humidity (%).
- mean_gU_pre_rot, mean_gV_pre_rot, mean_gW_pre_rot: Pre-rotation wind components (m/s).
- mean_gT_virt, mean_cH2O, mean_c_e: Temperature and moisture-related variables (C, g/m^3, kPa).
- Wind_Dir, mean_Wind_Spd: Wind direction (degrees) and speed (m/s).
- sigma_V, friction_velocity: Turbulence statistics (m/s, m/s).
- Height, sonic_path, intake_path: Tower height and sensor path constants.
- MO_stability: Monin-Obukhov stability parameter (dimensionless).
- Hc, cLEc, Fcc: Sensible heat flux, latent heat flux, and net ecosystem exchange after corrections (W/m^2, W/m^2, umol CO2 m^-2 s^-1).
- Footprint data: x, y coordinates in meters (UTM NAD83).
- Land cover data: categorical raster at 1 m^2 resolution with 0, 1, 2, 4 categories.

## Methodological notes and references

- Flux signs: NEE negative = terrestrial carbon sink.
- Time lag determination for gas sampling and sensor alignment described in references, with particular citations to Burba et al. and related methodology.
- References include methodological guides for eddy covariance, gap filling, footprint prediction, and data quality practices (Aubinet et al. 2012; Burba 2010; Clement 1999; Falge et al. 2001; Kljun et al. 2015; Reichstein et al. 2005; Tukey 1977; Webb et al. 1980).

## Practical relevance for data use

- Provides ready-to-analyze half-hour fluxes (H, LE, NEE) with post-processing corrections and quality treatments suitable for cross-site comparison.
- Includes footprint information to contextualize flux measurements and land-cover context around each tower.
- Land-cover maps enable habitat characterization and zonal analyses around measurement sites.
- Clear documentation of data structure, units, time references, and post-processing steps supports reproducibility and self-serve data exploration.