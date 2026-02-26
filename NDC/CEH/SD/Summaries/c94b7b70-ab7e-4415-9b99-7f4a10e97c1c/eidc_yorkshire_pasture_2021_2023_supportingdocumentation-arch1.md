# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a pasture, Yorkshire, UK, 2021-2023

## Overview of the dataset
- 30-minute observations of land-atmosphere exchange: net ecosystem CO2 exchange (NEE), sensible heat (H), and latent heat (LE).
- Collected over ~1.5 years at an agriculturally-managed pasture in Yorkshire, UK.
- Measurements used the eddy covariance (EC) method from 01/09/2021 to 01/01/2023.
- Includes weather and soil physics measurements.

## Study site
- Field located at the University of Leeds Research Farm (coordinates provided).
- Grazed by sheep since 2012; occasional silage cutting.
- Temperate oceanic climate: mean annual temperature ~9.5°C and rainfall ~885 mm.
- Soil: loamy, calcareous brown earth; pH ~6.8; bulk density ~1.1 g cm^-3.
- Soil carbon and nitrogen at 0–30 cm: 27.7 g kg^-1 and 2.3 g kg^-1.
- Rainfed site with no irrigation or fertiliser; silage cut July 2022; periodic grazing during the measurement period.

## Collection methods and fieldwork instrumentation

### Flux instrumentation
- Automated measurements of CO2 fluxes, weather, and soil measurements.
- Eddy covariance with a closed-path system, sensors 2 m above canopy.
- LI-7200RS CO2/H2O analyser and Gill Windmaster 3D sonic anemometer.
- Measurements: NEE (μmol CO2 m^-2 s^-1), H (W m^-2), LE (W m^-2), turbulence (u, v, w; m s^-1), sonic temperature (Tsonic; °C).
- Data sampled at 10 Hz and aggregated to 30-minute means.
- Logging: CR1000X datalogger and Smartflux 2 processing computer.

### Ancillary measurements
- Energy fluxes: net radiation (Rnet), short-wave incoming (SWin) and outgoing (SWout), long-wave incoming (LWin) and outgoing (LWout).
- Air temperature (Tair) and relative humidity (RH); soil temperature (Tsoil) and soil moisture (VWC%) at 5 cm depth.
- All ancillary measurements logged as 30-minute means.

## Data processing
- Processing workflow follows Morrison et al. (2019).
- 30-minute fluxes (H, LE, NEE) computed with EddyPro 7 (V7.0.6).
- Steps: data conditioning, angle-of-attack correction for the Gill anemometers, cross-correlation for time lags, correction for co-spectral attenuation (high/low frequency).
- Random uncertainty estimated per Finkelstein & Sims (2001).

## Quality control
- Performed in R (v4.1.3) to ensure high-quality flux data.
- Data removed for: statistical outliers; LI-COR signal strength anomalies (> baseline); nonrepresentative footprints (>20% outside site boundaries); unrealistic flux thresholds (H, LE, NEE); friction velocity u* < 0.14 m s^-1.

## Gap-filling
- Gaps and flux partitioning of NEE done with REddyProc (R package).
- Gap-filling method: marginal distribution sampling.
- Uncertainty of filled data estimated from the standard deviation of observations used for gap filling.

## Details of data structure
- File: Yorkshire_Pasture_2021_2023.csv
- Columns include:
  - Temporal: Date (dd/mm/yyyy, GMT), Time (HH:MM:SS, GMT)
  - Fluxes and uncertainties: NEE, NEE_unc, LE, LE_unc, H, H_unc, Tau, Tau_unc
  - Storage terms: CO2_strg, LE_strg, H_strg
  - Meteorology: Pa (barometric), Tair, RH, VPD, SWin, SWout, LWin, LWout, Rnet, PAR, G, GPP
  - Soil and environment: Tsoil, Tsoil_unc, VWC, windspeed, winddir, Ustar, TKE, Tstar, L, (z-d)/L
  - Processed names: NEE_f, NEE_f_sd, Reco, GPP
- Note: NA indicates missing data.
- The table includes a comprehensive set of pre- and post-gap-filled variables, including flux partitioning results.

## Acknowledgements
- Data collection funded by the Leeds-York-Hull Natural Environmental Research Council (NERC) Doctoral Training Partnership (DTP) Panorama (grant NE/S007458/1).
- Acknowledges the University of Leeds Research Farm and Rob Yardley for farm management information.

## References
- Cited sources for instruments, processing, and methods (e.g., LI-COR EddyPro, Moncrieff et al. on Eddy covariance processing, Reichstein et al. on REddyProc, Morrison et al. 2019 workflow, various instrument datasheets and calibration references).