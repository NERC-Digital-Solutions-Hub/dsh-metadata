# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a conservation managed fen, Wicken Sedge Fen, Cambridgeshire, UK, 2009 to 2010

## Overview
- Time series of land surface–atmosphere exchanges for net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) at Wicken Sedge Fen (EF-LN) in Cambridgeshire, UK.
- Measurements collected with an open-path eddy covariance system during 2009-03-20 to 2009-12-31 and 2010-04-09 to 2011-01-16/17.
- Dataset includes ancillary weather and soil physics observations and atmosphere turbulence descriptors.

## Study site
- Wicken Sedge Fen flux observation site: 52° 18' 34.86" N, 0° 16' 47.01" E, 2 m above mean sea level.
- Climate: temperate maritime; mean annual air temperature ~10.7°C and precipitation ~563 mm yr⁻¹ (1981–2010).
- Peat depth: 2–4 m; hydrologically isolated from surrounding arable land.
- Primary water source: Monks Lode; soil pH ~7.5, C content ~32%, C:N ~15.

## Sampling regime
- Automated flux, meteorological, and soil physics measurements conducted in two periods: 2009-03-20 14:30 to 2009-12-31 08:30 and 2010-04-09 12:30 to 2011-01-17 00:00.

## Flux data acquisition
- Eddy covariance measurements above grassland canopy at 3.95 m height.
- Instrumentation: Solent R3 ultrasonic anemometer thermometer + LI-7500 infrared gas analyser.
- Raw data: three velocity components, sonic temperature, water vapour density, and CO2 density; sampled at 20 Hz and logged with a CR3000 data logger.

## Ancillary data acquisition
- Additional meteorological and soil observations co-located with the flux tower.
- Measurements include: air temperature (Ta) and relative humidity (RH) at 2 m; net radiation (Rnet) and components; soil heat flux (G) at two locations; soil temperature in the upper 0.1 m.

## Data processing
- Turbulent fluxes calculated with EddyPRO software (v7.0.6) and 30-minute averaging.
- Processing steps include: QC of 20 Hz data, angle-of-attack corrections, 2D coordinate rotation, corrections for spectral attenuation, humidity effects on H, density corrections for LE and CO2.
- Derived variables: wind speed/direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter (z/L).
- Random uncertainty for each 30-minute flux estimate calculated; outputs include both original and derived metrics.

## Quality control
- Outliers removed using median absolute deviation; flux bounds applied (H: -200 to 550 W m⁻²; LE: -60 to 600 W m⁻²; NEE: -50 to 30 μmol CO2 m⁻² s⁻¹).
- NEE quality checks: nighttime NEE removal when negative, friction velocity threshold (u* > 0.18 m s⁻¹), footprint criterion (≥80% from target ecosystem).
- Visual inspection step: weekly plots to identify additional erroneous values for manual removal.

## Data gap-filling and flux partitioning
- Gaps in EC data filled with Marginal Distribution Sampling (MDS).
- NEE partitioned into GEP and TER using Ta-driven algorithm (no soil temperature measurements at site) per Reichstein et al. (2005).
- Gap-filling and partitioning performed with REddyProc (R) and where possible, meteorological data gaps filled using onsite weather station data.

## Details of data structure
- Data provided as a single CSV file with columns as described (DateTime, NEE, NEE_sd, LE, LE_sd, H, H_sd, Tau, Tau_sd, CO2_strg, Pa, Ta, RH, VPD, SWin, SWout, LWin, LWout, Rnet, G1, G2, WS, WD, Ustar, TKE, L, zL, Xpeak, x70, x90, NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP, etc.).
- Time coverage: complete time series from 2009-01-01 00:30 to 2011-01-17 00:00, with actual flux measurements active on 2009-03-20 14:30 to 2009-12-31 08:30 and 2010-04-09 12:30 to 2011-01-17 00:00.
- Missing records denoted by -9999.
- Units and variable descriptions follow LI-COR conventions and Reichstein et al. (2016).

## Nature and units of recorded values
- Fluxes: NEE (μmol CO2 m⁻² s⁻¹), LE (W m⁻²), H (W m⁻²), τ (kg m⁻¹ s⁻²).
- Ancillary meteorology: Ta (°C), RH (%), VPD (hPa), SWin/SWout (W m⁻²), LWin/LWout (W m⁻²), Rnet (W m⁻²), G1/G2 (W m⁻²).
- Turbulence and canopy metrics: WS (m s⁻¹), WD (degrees), Ustar (m s⁻¹), TKE (m⁻² s⁻²), L (m), zL (dimensionless).
- Gap-filled variables: NEE_filled, NEE_filled_sd, LE_filled, LE_filled_sd, H_filled, H_filled_sd, TER, GEP, etc.

## Acknowledgments
- Funded by Natural Environment Research Council (NE/R016429/1) as part of UK-SCAPE; thanks to National Trust and Wicken Fen staff; individual acknowledgments to JK, RM.