# Half hourly fluxes of sensible heat, latent energy and carbon, observed by eight eddy covariance towers in the Northern Chihuahuan Desert, 2018-2019

## Overview
- Metadata-supported dataset describing half-hourly flux measurements from eight eddy covariance towers at the Sevilleta Refuge, New Mexico, USA, collected 2018-11-01 to 2019-11-01.
- Purpose: test a new design and investigate spatial variability of fluxes; used to support environmental monitoring and framework development.
- Data include fluxes for sensible heat (H), latent heat (LE), and net ecosystem exchange (NEE), with associated auxiliary variables and quality control.

## Datasets included
- Data files 1–8: SEG_EC1_fluxes, SEG_EC2_fluxes, SEG_EC3_fluxes, SEG_EC4_fluxes, SES_EC1_fluxes, SES_EC2_fluxes, SES_EC3_fluxes, SES_EC4_fluxes (half-hourly flux data from eight towers; 6 m tall; sensors detailed below).
- Data files 9–18: Footprints (SEG_EC1_footprint_80 … SEG_EC4_footprint_80 and SEG_EC0_footprint_80, SES_EC1_footprint_80 … SES_EC4_footprint_80 and SES_EC0_footprint_80) representing 80% flux footprint extents for the ten towers (eight REC systems plus two AmeriFlux towers US-Seg and US-Ses).
- Data files 19–20: LAND COVER extracts (SEG_Extract_land_cover, SES_Extract_land_cover) – land cover maps in a 440 m radius around US-SEG and US-SES with categories: bare ground, shrubland, and herbaceous (codes 0, 1, 2; 4 listed but not explained).

## Data processing and quality control
- Raw EC data pre-processed with EdiRe software (v1.5.0.32) including spike detection, coordinate rotation, frequency response correction, cross-correlation and WPL correction.
- Gap-filling of half-hourly data performed with a GitHub-published code; season-specific u* filtering applied via REddyProc R package (v1.2).
- Cospectra analysis conducted with a Hamming window (segment size 512) yielding 30 frequency bins for frequency-specific correlations.
- Time lags between sonic anemometer and gas sensors determined by covariance analysis at lags of 0, 5.5, and 7 seconds for H, LE, and NEE; CP for water held constant across RH range (5%–90%).
- Spike removal via Tukey’s fence method (IQR-based; outliers outside [Q1 − k·IQR, Q3 + k·IQR] with k = 30).
- Data gaps represented as blank cells; some columns may contain 0 values (e.g., correlation indicators).

## Measurement details
- Location: Sevilleta Refuge, New Mexico, USA (exact tower locations detailed in the associated paper).
- Tower configuration: eight low-frequency (1 Hz) eddy covariance towers; height = 6 m.
- Main sensors:
  - Gill Windmaster sonic anemometer (wind components)
  - Honeywell HIH-4000 relative humidity sensor
  - Vaisala GMP343 CO2 concentration sensor
- Sign convention: flux signs are atmospheric; NEE negative denotes carbon uptake by the ecosystem.

## Data structure and fields (flux dataset)
- Key fields include:
  - Date_Time (center of half-hour): DD/MM/YYYY HH:mm
  - P (air pressure; kPa, ~84 kPa)
  - mean_vCO2 (CO2 concentration; ppmv)
  - mean_vT (air temperature; °C)
  - mean_cRH (relative humidity; %)
  - mean_gU_pre_rot, mean_gV_pre_rot, mean_gW_pre_rot (pre-rotation wind components)
  - mean_gT_virt (sonic temperature; °C)
  - mean_cH2O (water vapor density; g m−3)
  - mean_c_e (water vapor partial pressure; kPa)
  - Wind_Dir, mean_Wind_Spd (wind direction in degrees; wind speed in m s−1)
  - sigma_V (standard deviation of lateral velocity fluctuations)
  - friction_velocity (u*, m s−1)
  - MO_stability (Monin-Obukhov stability: tower height / L)
  - Hc (sensible heat flux after frequency response correction; W m−2)
  - cLEc (latent heat flux after frequency response correction; W m−2)
  - Fcc (Net Ecosystem Exchange after correction; μmol m−2 s−1)
  - Height of tower, sonic_path, intake_path (constant metadata)
- Units and data cleanliness clearly documented; missing values indicated by blanks.

## Spatial footprint data
- 80% footprint extents provided for ten towers (eight REC towers plus US-Seg and US-Ses AmeriFlux towers).
- Structure: x (Easting, UTM 13N, NAD83) and y (Northing, UTM 13N, NAD83).

## Land cover data
- Land cover maps for a 440 m radius around US-SEG and US-SES.
- Categories: bare ground (0), shrubland (1), herbaceous (2); a fourth code (4) is listed but not explained.

## Temporal coverage
- Data span from 2018-11-01 to 2019-11-01, with half-hourly cadence and associated processing steps described.

## Use in monitoring frameworks (implications)
- Demonstrates end-to-end data handling from collection to corrected flux outputs, including:
  - Documentation of data provenance and processing steps (software tools, corrections, time lags).
  - Rigorous quality control, gap filling, and stationarity filtering procedures.
  - Availability of metadata (instrumentation, data structure, units) to support data governance and reproducibility.
  - Provision of footprint and land-cover context to support interpretation of flux measurements and framework embedding.
- Highlights common monitoring-framework barriers and mitigations:
  - Data accessibility and metadata completeness addressed via explicit file-level descriptions and references.
  - Open data compatibility: references to public tools and code for reproducibility.
  - Data governance signals: frequency corrections, data flags, and clear handling of missing data.
  - Spatial coherence ensured by footprint data and land-cover maps, enabling robust interpretation of flux variability across towers.

## References
- Aubinet, Vesala, Papale (2012) Eddy Covariance: A Practical Guide
- Burba (2013) Eddy Covariance Method Field Book
- Burba & Anderson (2010) Practical Guide to Flux Measurements
- Clement (1999) EdiRe Data Software
- Falge et al. (2001) Gap Filling for NEE
- Kljun et al. (2015) Two-Dimensional Footprint Parameterisation
- Reichstein et al. (2005) NEE Partitioning algorithms
- Tukey (1977) Exploratory Data Analysis
- Webb, Pearman, Leuning (1980) Density effects corrections