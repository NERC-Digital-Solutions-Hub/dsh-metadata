# Metadata for the dataset ' Half hourly fluxes of sensible heat, latent energy and carbon, observed by eight eddy covariance towers in the Northern Chihuahuan Desert, 2018-2019 ' by Boschetti and Cunliffe et al .

## Overview
- Half-hourly data from eight eddy covariance towers deployed in the Sevilleta Refuge (New Mexico, USA) collected from 2018-11-01 to 2019-11-01.
- Study aimed to test a new design and investigate spatial variability of fluxes; towers are 6 m tall with core sensors (Gill Windmaster sonic anemometer, Honeywell HIH-4000 RH, Vaisala GMP343 CO2).
- Data were pre-processed and gap-filled; time lags for fluxes derived from covariance analyses; signs of fluxes follow standard conventions (negative NEE = terrestrial carbon sink).

## Data contents
- 1) Data files 1 to 8 (Flux data)
  - 1) SEG_EC1_fluxes
  - 2) SEG_EC2_fluxes
  - 3) SEG_EC3_fluxes
  - 4) SEG_EC4_fluxes
  - 5) SES_EC1_fluxes
  - 6) SES_EC2_fluxes
  - 7) SES_EC3_fluxes
  - 8) SES_EC4_fluxes
  - Contents include half-hourly measurements and derived variables such as air temperature, relative humidity, CO2 concentration, wind components, wind direction, and fluxes (Hc, cLEc, Fcc, NEE), along with metadata like height, path lengths, and sensor-specific parameters.
- 2) Data files 9 to 18 (Footprint data)
  - 9) SEG_EC1_footprint_80
  - 10) SEG_EC2_footprint_80
  - 11) SEG_EC3_footprint_80
  - 12) SEG_EC4_footprint_80
  - 13) SEG_EC0_footprint_80
  - 14) SES_EC1_footprint_80
  - 15) SES_EC2_footprint_80
  - 16) SES_EC3_footprint_80
  - 17) SES_EC4_footprint_80
  - 18) SES_EC0_footprint_80
  - Defines 80% flux footprints for the ten towers (the eight REC systems plus two AmeriFlux towers US-Seg and US-Ses) with coordinates.
- 3) Data files 19 to 20 (Land cover)
  - 19) SEG_Extract_land_cover
  - 20) SES_Extract_land_cover
  - Land cover maps within a 440 m radius around US-SEG and US-SES, with three land cover categories (bare ground, shrubland, herbaceous) at 1 m2 resolution; coding notes indicate 0 = barren, 1 = shrubland, 2 = herbaceous (and a 4 entry noted in text).
- 4) References
  - A set of scholarly and methodological references underpinning the processing steps (eddy covariance methodology, EdiRe software, gap-filling, footprint modelling, NEE partitioning, Tukey-based outlier detection, and density corrections).

## Data processing and quality control
- Pre-processed raw EC data using EdiRe software v1.5.0.32, including spike detection, coordinate rotation, frequency response correction, cross-correlation, and WPL correction.
- Gap-filling performed with code published on GitHub; season-specific u* filtering applied using REddyProc R package v1.2.
- Cospectra analysis conducted with a Hamming window (segment size 512, 30 frequency bins) to derive frequency-specific correlation values.
- Time lags for fluxes derived by covariance analysis between sonic anemometer and RH/CO2 sensors for H, LE, and NEE; delays set to 0, 5.5, and 7 seconds respectively.
- Spikes removed with a Tukey fence-based method (using Q1, Q3, IQR; outliers outside [Q1 - k*IQR, Q3 + k*IQR] with k = 30 to avoid over-filtering).
- Data gaps are represented as blank cells; some columns may contain 0 values (e.g., correlation 0).
- Data are structured with clear variable names, units, and descriptions for reproducibility and governance.

## Temporal scope, location, and structure
- Location: Sevilleta Refuge, New Mexico, USA (towers described as part of REC systems; two AmeriFlux towers included in footprint analyses).
- Time frame: 2018-11-01 to 2019-11-01.
- Data organization: Each flux dataset (fluxes), footprint datasets, and land-cover datasets are provided as separate files with consistent naming conventions to aid discoverability and reuse.

## Data structure and variables (highlights)
- Flux data include:
  - Date_Time (center of half-hour), P (air pressure), mean_vCO2 (CO2 concentration), mean_vT (air temperature), mean_cRH (relative humidity), wind components (mean_gU_pre_rot, mean_gV_pre_rot, mean_gW_pre_rot), mean_gT_virt, mean_cH2O, mean_c_e, Wind_Dir, mean_Wind_Spd, sigma_V, friction_velocity, Height, sonic_path, intake_path, MO_stability, Hc (sensible heat flux after correction), cLEc (latent heat flux after correction), Fcc (NEE after correction).
- Footprint data include:
  - x (Eastings), y (Northings) in UTM 13N NAD83.
- Land-cover data include:
  - Categorical maps: bare ground, shrubland, herbaceous (with specific integer codes).

## Access, interoperability, and governance notes
- Multiple data components (fluxes, footprints, land cover) support reproducible flux footprint analyses and comparability across sites.
- Documentation provides explicit data handling steps, enabling governance by data stewards to ensure standards around metadata, provenance, and update cycles.
- The dataset references widely recognized methods and tools, facilitating interoperability across systems and formats, albeit requiring careful alignment of units, time lags, and coordinate systems when integrating with other datasets.