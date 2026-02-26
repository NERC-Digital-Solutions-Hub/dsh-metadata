# Energy and carbon dioxide fluxes, meteorology and soil physics observed at INCOMPASS Land Surface Stations in India, 2016 to 2017

## Overview
- Three CSV files corresponding to INCOMPASS Land Surface Stations in India: Berambadi (Southern Karnataka), Dharwad (Dharwad, Karnataka), and Kanpur (Uttar Pradesh).
- Time series of surface-atmosphere exchanges: sensible heat (H), latent heat (LE), momentum (τ), and net ecosystem CO2 exchange (NEE).
- Ancillary meteorology, soil physics observations, atmospheric turbulence variables, and observation quality indicators.
- Data collected under the INCOMPASS project from 2016-01-01 00:30 to 2018-01-01 00:00; open-path eddy covariance (EC) measurements with standardized processing and QC.

## Sites and site context
- Berambadi, Southern Karnataka
  - Location: agricultural land on Deccan Plateau; ~2 km from Western Ghats foothills; semi-arid monsoon climate (Aw); mean temperature ~24.4°C; ~600 mm rainfall.
  - Soils: Alfisols; dominant crops include maize, turmeric, sunflower, marigold, sorghum, vegetables.
  - Characteristics noted in Table 1 (location, altitude, land use, climate, soil order, major soil properties).
- Dharwad, Southern Karnataka
  - Location: on campus of University of Agricultural Sciences, Dharwad; climate Aw; mean temperature ~24.3°C; ~885 mm rainfall.
  - Soils: Vertisols; agricultural field with multi-crop schedule (maize, horse gram, soybean intercropping, pigeon pea).
- Kanpur, Uttar Pradesh
  - Location: semi-natural grassland at IIT Kanpur; humid subtropical climate (Csa); mean temperature ~25.6°C; ~820 mm rainfall.
  - Soils: Fluvisols; vegetation a Phragmites-Saccharum-Imperata grassland; periodic flooding and occasional standing water.

## Sampling regime and instrumentation
- Automated, tower-based flux, meteorology, and soil physics measurements from 2016-01-01 00:30 to 2018-01-01 00:00.
- Flux data collection
  - Open-path eddy covariance (EC) systems at all sites; 10 m tall masts; three velocity components and sonic temperature measured by Windmaster sonic anemometers; CO2 and water vapor by LI-7500A; data logged at 20 Hz.
  - Fluxes computed on 30-minute intervals; sign convention: positive from surface to atmosphere.
  - Processing with EddyPRO v6.1; includes corrections for angle of attack, coordinate rotation, spectral corrections, density effects, and storage terms; QC flags applied.
- Meteorological observations
  - 10 m masts; sensors for barometric pressure, air temperature, relative humidity, net radiation (and components), wind speed/direction, precipitation.
- Soil physics observations
  - Duplicated soil measurements at two depths; soil heat flux, soil temperature, and soil volumetric water content at depths 0.03–0.15 m; sensor details provided; data logged and aggregated to 30-minute resolution.

## Data processing and quality control
- Flux data
  - EddyPRO processing included standard micrometeorological corrections; 30-minute averaging; random uncertainties calculated via covariance-based approach.
  - QC procedures: outlier removal using median absolute deviation; tests for Stationarity and Integral Turbulence; data flagged; thresholds include acceptable quality, with higher rejection if QC flags exceed a threshold; instrument signal checks (LI-7500A > 80%), site-specific ranges, and nighttime NEE checks.
  - Footprint analysis (Kormann & Meixner model via ART Footprint Tool) to assess spatial representativeness.
  - Weekly visual inspection for any clearly erroneous values; supplementary QC for ancillary data.
- Ancillary data
  - Basic range checks, spike/dropout visual checks; cross-checks among soil depth observations; rainfall verification against soil moisture changes and flooding events.

## Data structure and content
- Time series delivered as separate CSV files for each station; records span 2016-01-01 00:30 to 2018-01-01 00:00.
- Missing data represented by -9999.
- Timestamps are end-of-30-minute-intervals; DateTime is in Indian Standard Time (UTC+5:30).
- Main variables
  - Fluxes: H (sensible heat), LE (latent heat), τ (momentum), NEE (net ecosystem CO2 exchange) with associated uncertainties and storage terms.
  - Meteorology: pressure (Pa), air temperature (Ta), relative humidity (RH), short- and long-wave radiation components (SWin, SWout, LWin, LWout), net radiation (Rnet), wind speed (WS) and direction (WD) at surface and 10 m, precipitation.
  - Soil physics: soil heat flux (G) at two depths/locations, soil temperature (Tsoil) at 0.05 and 0.15 m, soil volumetric water content (VWC) at 0.05 and 0.15 m, with multiple depth/location entries.
  - Derived/auxiliary EC metrics: Ustar (friction velocity), TKE, T*, Obukhov length (L), stability parameter (z/L), x_peak and x_10/30/50/70/90% footprints.
  - Data quality and processing flags, and uncertainty terms for primary variables.
- Documentation references in Table 3 enumerate the exact meaning and units for each column.

## Data governance, usage notes, and acknowledgments
- Data are produced under the INCOMPASS project and acknowledge funding from NERC, MoES, and associated program grants; collaborators across Indian institutions and UK partners.
- Data provenance and site permissions are documented; datasets rely on standardized processing protocols to ensure comparability across sites.
- References provided for processing methods, QC criteria, and footprint modeling underpin dataset quality and reproducibility.

## Practical implications for data stewards
- The dataset provides a harmonized, quality-controlled time series of surface energy, CO2 fluxes, meteorology, and soil physics across three Indian sites, suitable for cross-site comparative analyses and flux-network studies.
- Rigorous QC, footprint assessment, and detailed metadata enhance discoverability and reusability; missing data are clearly encoded (-9999) and time stamps are standardized to 30-minute intervals.
- Documentation of site characteristics, instrumentation configurations, and data processing steps supports governance, data sharing, and long-term maintenance.