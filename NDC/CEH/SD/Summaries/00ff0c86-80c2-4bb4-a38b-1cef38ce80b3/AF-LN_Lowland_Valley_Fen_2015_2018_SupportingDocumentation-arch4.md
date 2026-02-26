# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a lowland valley fen, Anglesey, UK, 2015 to 2018

## Overview
- Time-series dataset (2015-01-01 00:30 to 2018-10-11 00:00) of land surface-atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured via eddy covariance at AF-LN site on Anglesey, UK.
- Includes ancillary meteorological and soil-physics observations, plus variables describing atmospheric turbulence.
- Flux data processed with standard eddy-covariance procedures; gap-filled and partitions of NEE into GEP and TER provided where possible.
- Data provided as a single CSV (AF-LN_Lowland_Valley_Fen_2015_2018.csv) with detailed metadata and units.

## Study site
- Location: AF-LN flux observation site, Cors Erddreiniog National Nature Reserve, Anglesey, North Wales (53° 18' 37.18'' N, 4° 17' 28.06'' W), elevation ~63 m amsl.
- Habitat: High-quality valley-head fen with low-intensity pony grazing; managed as a conservation site.
- Climate and soil context: temperate maritime climate (mean 1981-2010 temp ~10.4 ± 3.9°C; precipitation ~841 ± 41 mm y⁻¹); deep fen peat with low bulk density and high carbon content; water levels near peat surface year-round.

## Sampling regime
- Automated measurements of flux, meteorology, and soil-physics from 2015-01-01 00:30 to 2018-10-11 00:00.
- Flux observations above grass canopy at 2.0 m height.

## Flux data acquisition
- Eddy covariance system: open-path configuration using CSAT3 ultrasonic anemometer (three velocity components; sonic temperature) and LI-7500 CO2/H2O infrared gas analyzer.
- Data were sampled at 20 Hz and logged with a CR3000 data logger.
- Fluxes recorded: NEE (μmol CO2 m⁻² s⁻¹), H (W m⁻²), LE (W m⁻²), and τ (kg m⁻¹ s⁻²); ancillary turbulence metrics (e.g., wind speed, direction, u*, TKE, Obukhov length).

## Ancillary data acquisition
- Meteorological: air temperature (Ta, 2 m), relative humidity (RH), net radiation (Rnet), incoming shortwave radiation (SWin), soil heat flux (G1, G2), soil temperatures (Tsoil1), precipitation (0.5 h and total).
- All ancillary data logged as 30-minute means or sums where applicable.

## Data processing
- Fluxes computed from raw 20 Hz data using EddyPRO software (Version 6.1) with standard processing:
  - QC steps: quality control of 20 Hz data, after-tilt and rotation corrections, high/low-frequency attenuation corrections, density corrections, etc.
  - Derived metrics: wind speed/direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter z/L, and flux footprint estimates.
- Random uncertainties for fluxes calculated; data processed to produce consistent time series.

## Quality control
- Outlier removal using median absolute deviation; non-stationary turbulence periods removed.
- Flux ranges filters: H (-200 to 500 W m⁻²), LE (-60 to 500 W m⁻²), NEE (-50 to 30 μmol CO₂ m⁻² s⁻¹).
- Night-time NEE removed or flagged when appropriate; friction velocity threshold applied (u* > 0.18 m s⁻¹).
- Weekly visual checks of flux and ancillary data to manually remove clearly erroneous values.

## Data gap-filling and flux partitioning
- Gap-filling for EC data (NEE, LE, H) using Marginal Distribution Sampling (Reichstein et al., 2005).
- Partitioning NEE into GEP and TER using a Ta-driven approach following Reichstein et al. (2005).
- Gap-filling and partitioning implemented via REddyProc (R package; Reichstein et al., 2016).
- Whenever possible, missing meteorological data filled using observations from a nearby second eddy covariance station (<1 km away).

## Details of data structure
- Data provided as a single CSV file with columns described in Table 1 (DateTime in dd-mm-yyyy HH:MM GMT, NEE, NEE_sd, LE, LE_sd, H, H_sd, Tau, Tau_sd, CO2_strg, LE_strg, H_strg, Pa, Ta, RH, VPD, SWin, Rnet, G1, G2, Tsoil1, Precipitation, WS, WD, Ustar, TKE, L, zL, x_peak, x_70, x_90, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP, etc.).
- Gap-filled and partitioned variables included: NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP.
- -9999 used to denote missing records due to system failures or QC removals.

## Nature and units of recorded values
- DateTime: dd-mm-yyyy HH:MM (UTC)
- NEE: μmol CO₂ m⁻² s⁻¹
- LE: W m⁻²
- H: W m⁻²
- Tau: kg m⁻¹ s⁻²
- Pa: kPa
- Ta: °C
- RH: %
- VPD: hPa
- SWin: W m⁻²
- Rnet: W m⁻²
- G1, G2: W m⁻²
- Tsoil1: °C
- Precipitation: mm per 0.5 h, total precipitation
- WS, WD: m s⁻¹ and degrees
- Ustar: m s⁻¹
- TKE: m² s⁻²
- L: m
- zL: dimensionless
- x_peak, x_70, x_90: m (upwind distance metrics for flux footprint)
- NEE_filled, LE_filled, H_filled, TER, GEP: same units as respective raw fluxes or derived terms; associated_sd fields provide uncertainties for filled values.

## Acknowledgments and references
- Dataset produced under UK-SCAPE programme and Defra project SP1210; acknowledges permission from Natural Resources Wales for site access.
- References include foundational methods and software for eddy-covariance processing and gap-filling (e.g., Reichstein et al., EddyPRO, REddyProc, Moncrieff et al., etc.).