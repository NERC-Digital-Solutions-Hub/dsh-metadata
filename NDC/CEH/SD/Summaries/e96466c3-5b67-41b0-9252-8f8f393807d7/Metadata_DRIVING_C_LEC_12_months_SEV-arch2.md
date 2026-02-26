Half hourly fluxes of sensible heat, latent energy and carbon, observed by eight eddy covariance towers in the Northern Chihuahuan Desert, 2018-2019

## Overview
- Metadata for a dataset of half-hourly fluxes (sensible heat, latent energy, and carbon) measured by eight eddy covariance towers in the Sevilleta Refuge, New Mexico, USA, from 2018-11-01 to 2019-11-01.
- Aims to test design, assess spatial variability of fluxes, and provide standardized environmental monitoring outputs.
- Data are organized into multiple file groups: raw/processed fluxes, footprint areas, and land cover within a defined radius.

## Data files

- Data files 1 to 8 (SEG_EC1_fluxes, SEG_EC2_fluxes, SEG_EC3_fluxes, SEG_EC4_fluxes, SES_EC1_fluxes, SES_EC2_fluxes, SES_EC3_fluxes, SES_EC4_fluxes)
  - Half-hourly data from eight towers (six meters tall) deployed at Sevilleta Refuge.
  - Main sensors: Gill Windmaster sonic anemometer, Honeywell HIH-4000 RH sensor, Vaisala GMP343 CO2 sensor.
  - Pre-processing: using EdiRe v1.5.0.32 including spike detection, coordinate rotation, frequency response correction, cross-correlation, and WPL correction.
  - Gap filling: via code from GitHub; season-specific u* filtering with REddyProc v1.2.
  - Cospectra: computed with Hamming windows (512 segment size, 30 bins) to derive frequency-specific correlations.
  - Time lags: determined for H, LE, and NEE (0, 5.5, and 7 s for gas sensors; water lag constant across RH 5–90%).
  - Spike removal: Tukey’s fence method (k = 30) to avoid over-filtering.
  - Data fields cover time, meteorological and flux variables (e.g., Date_Time, P, mean_vCO2, mean_vT, mean_cRH, Wind_Spd, Hc, cLEc, Fcc, etc.) with units and descriptions.
  - Flags and notes: missing values are represented as blanks; some fields may contain zeros (e.g., correlation measures).

- Data files 9 to 18 (SEG_EC1_footprint_80, SEG_EC2_footprint_80, SEG_EC3_footprint_80, SEG_EC4_footprint_80, SEG_EC0_footprint_80, SES_EC1_footprint_80, SES_EC2_footprint_80, SES_EC3_footprint_80, SES_EC4_footprint_80, SES_EC0_footprint_80)
  - 80% flux footprint coordinates for ten towers (eight REC towers plus US-Seg and US-Ses AmeriFlux towers).
  - Data format: x (Easting, m, NAD83 UTM 13N), y (Northing, m, NAD83 UTM 13N).

- Data files 19 to 20 (SEG_Extract_land_cover, SES_Extract_land_cover)
  - Land cover maps within 440 m radius centered on US-SEG and US-SES towers.
  - Categories: bare ground, shrubland, and herbaceous. 1 m2 cells.
  - Codes listed: 0 = barren, 1 = shrubland, 2 = herbaceous (note potential typographical discrepancy with code 4 appearing in text).

## Temporal and spatial scope
- Time period: 2018-11-01 to 2019-11-01.
- Location: Sevilleta Refuge, New Mexico, USA.
- Towers: eight eddy covariance towers (SEG and SES series) plus two AmeriFlux towers for footprint integration.

## Data processing and quality control
- Pre-processing with EdiRe software (v1.5.0.32) including spike detection, coordinate rotation, frequency response correction, WPL correction, and cross-correlation adjustments.
- Gap filling performed with an established GitHub-based method; u* filtering applied seasonally using REddyProc (v1.2).
- Time lags between gas/vapor sensors and sonic measurements estimated via covariance analysis at specified delays.
- Spike filtering uses Tukey’s fences to minimize over-filtering.
- Cospectral analysis informs frequency-domain interpretation of fluxes.
- Flux signs: positive or negative conventions follow standard eddy covariance practice (e.g., negative NEE indicates a carbon sink).

## Data structure and key fields
- Flux data fields include: Date_Time (center of half-hour), pressure (P), mean CO2 concentration (mean_vCO2), air temperature (mean_vT), relative humidity (mean_cRH), pre-rotation wind components (mean_gU_pre_rot, mean_gV_pre_rot, mean_gW_pre_rot), post-rotation wind (mean_Wind_Spd), friction velocity (friction_velocity), Monin-Obukhov stability (MO_stability), corrected fluxes (Hc, cLEc, Fcc).
- Spatial fields include tower height, instrument paths, and footprint data.
- Land cover fields provide 1 m2 resolution land cover categories for 440 m neighborhoods around US-SEG and US-SES towers.

## Spatial context and references
- Footprint and land-cover data enable interpretation of flux footprints and local land-cover influences on flux magnitudes.
- References cited include foundational manuals and methodological papers for Eddy Covariance methods, data processing (EdiRe, REddyProc), flux footprint modeling, gap-filling strategies, and statistical outlier detection (e.g., Tukey, Webb et al. 1980).

## Practical implications for analysis
- Provides standardized, QA/QC’d half-hour flux data with accompanying footprint and land-cover context for inter-site comparison and temporal trend analyses.
- Suitable for examining spatial variability of fluxes and assessing how local land cover and footprint effects influence ecosystem gas exchange and energy fluxes.
- Data and processing details (time lags, gap-filling, u* filtering, and cospectra) enable reproducibility and robust cross-site analyses.