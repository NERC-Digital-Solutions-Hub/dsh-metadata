# Metadata for the dataset ' Half hourly fluxes of sensible heat, latent energy and carbon, observed by eight eddy covariance towers in the Northern Chihuahuan Desert, 2018-2019 ' by Boschetti and Cunliffe et al .

## Overview
- Provides half-hourly flux and footprint data from eight eddy covariance towers at Sevilleta Refuge, New Mexico, USA, collected 2018-11-01 to 2019-11-01.
- Purpose: test a new design and investigate spatial variability of fluxes across towers; towers are 6 m tall and instrumented with sonic anemometers, relative humidity sensors, and CO2 sensors.
- Data collection and processing led by Tim Hill, Robert Clement, Fabio Boschetti, and Andrew Cunliffe (University of Exeter).
- Data products include flux measurements (SEG_EC1–SEG_EC4 and SES_EC1–SES_EC4), 80% footprint maps, and land-cover maps around two AmeriFlux towers (US-Seg, US-Ses).

## Data content and structure
- 1) Data files 1 to 8: Flux data
  - Segments: SEG_EC1_fluxes, SEG_EC2_fluxes, SEG_EC3_fluxes, SEG_EC4_fluxes, SES_EC1_fluxes, SES_EC2_fluxes, SES_EC3_fluxes, SES_EC4_fluxes.
  - Variables include Date_Time (center of half-hour), atmospheric pressure (P), CO2 concentration, air temperature, relative humidity, wind components (pre-rotation), Wind_Dir, Wind_Spd, friction velocity, Monin-Obukhov stability, and fluxes (Hc, cLEc, Fcc, NEE).
  - Time lags for gases: 0, 5.5, and 7 seconds to account for closed-path sampling delays.
  - Data processing: gap-filled, with season-specific u* filtering via REddyProc; spike detection via Tukey-based method; cospectral analysis performed with specified parameters.
  - Sign convention: flux signs relative to atmosphere, with negative NEE indicating a terrestrial carbon sink.
  - Data formatting notes: missing values as blanks; some fields hold constant values (e.g., air pressure, sampling path details).
- 2) Data files 9 to 18: Footprint data
  - SEG_EC1_footprint_80, SEG_EC2_footprint_80, SEG_EC3_footprint_80, SEG_EC4_footprint_80, SEG_EC0_footprint_80, SES_EC1_footprint_80, SES_EC2_footprint_80, SES_EC3_footprint_80, SES_EC4_footprint_80, SES_EC0_footprint_80.
  - 80% footprint coordinates for ten towers (the eight REC systems plus two AmeriFlux towers US-Seg and US-Ses).
  - Structure: x (easting, NAD83 UTM 13N), y (northing, NAD83 UTM 13N).
- 3) Data files 19 to 20: Land-cover data
  - SEG_Extract_land_cover, SES_Extract_land_cover.
  - Land-cover maps within a 440 m radius around US-SEG and US-SES; categories: 0 = barren, 1 = shrubland, 2 = herbaceous; resolution 1 m2 cells.
- 4) References
  - Key methodological and software references for Eddy Covariance techniques, data processing, gap filling, footprint analysis, and statistical handling (Aubinet et al. 2012; Burba 2013; Burba & Anderson 2010; Clement 1999; Falge et al. 2001; Kljun et al. 2015; Reichstein et al. 2005; Tukey 1977; Webb et al. 1980).

## Data processing and methodology
- Pre-processing
  - Raw data from EC1–EC4 processed with EdiRe software v1.5.0.32 (spike detection, coordinate rotation, frequency response correction, cross-correlation, WPL correction).
- Gap filling and filtering
  - Gap-filling using code from GitHub; season-specific u* filtering via REddyProc R package (v1.2).
- Flux and spectra analyses
  - Cospectra analysis using Hamming window; specific data segment size and frequency bins to derive frequency-specific correlations.
  - Time-lag determination for H, LE, and NEE based on covariance analyses between sonic anemometer and RH/CO2 sensors (lags set to 0, 5.5, 7 s; water lag constant across 5–90% RH).
- Data quality and consistency
  - Outliers removed using a Tukey fence approach; k parameter set to 30 to avoid over-filtering.
  - Blank cells indicate missing values; notes on constant fields (e.g., air pressure, tower height).
- Coordinate and reference frame
  - Footprint coordinates tied to UTM 13N NAD83; land-cover maps referenced to towers US-SEG and US-SES.

## Data provenance and usage considerations
- Provenance
  - Data collected from eight REC towers plus two AmeriFlux towers (US-Seg, US-Ses), with instrumentation and maintenance led by named researchers.
- Usage considerations for data leaders
  - Rich, multi-tower flux dataset suitable for cross-site comparisons, method validation, and cross-network integration.
  - Metadata includes processing steps, time lags, and quality-control methods enabling rigorous data governance.
  - Land-cover context supports spatial analyses and footprint interpretation around flux towers.
  - Open references and software links (REddyProcWeb; GitHub gap-filling code) aid reproducibility and potential reprocessing.

## Access and usage notes
- Online tools and software references provided for processing and reproducibility:
  - REddyProc web services: https://www.bgc-jena.mpg.de/bgi/index.php/Services/REddyProcWeb
  - Gap-filling code availability via GitHub
- Data are documented with detailed field definitions, units, and processing steps to support integration into broader data ecosystems and community data standards.