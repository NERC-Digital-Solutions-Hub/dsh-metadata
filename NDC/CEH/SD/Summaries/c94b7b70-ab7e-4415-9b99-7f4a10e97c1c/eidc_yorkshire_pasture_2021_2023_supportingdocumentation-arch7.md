# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a pasture, Yorkshire, UK, 2021-2023

## Overview
- 30-minute observations of land-atmosphere exchange: net ecosystem CO2 exchange (NEE) and sensible (H) and latent heat (LE).
- Span of 1.5 years at an agriculturally-managed pasture in Yorkshire, UK; data collected 01/09/2021–01/01/2023.
- Data collected using micrometeorological eddy covariance (EC) methods, with additional weather and soil measurements.

## Study site
- Location: field at University of Leeds Research Farm (53°51'58.64"N, 1°19'11.08"W).
- Land management: grazed by sheep since 2012; periodic silage cutting; rainfed; no fertiliser applied.
- Climate: temperate oceanic; mean annual temperature ~9.5°C; precip. ~885 mm (1992–2022 averages).
- Soil: loamy, calcareous brown earth; pH ~6.8; bulk density ~1.1 g cm^-3; soil carbon ~27.7 g/kg and nitrogen ~2.3 g/kg (0–30 cm).
- Management during study: silage cut July 2022; periodic grazing.

## Collection methods and fieldwork instrumentation
- Flux measurements: above-canopy closed-path EC system; sensors at 2 m height.
- Instruments: LI-7200RS CO2/H2O analyser; Gill Windmaster 3D sonic anemometer.
- Data rate: 10 Hz, aggregated to 30-minute means; primary data logged by CR1000X; supplemented by Smartflux 2.
- Ancillary measurements: SN-500 net radiometer (Rnet, SWin, SWout, LWin, LWout); HMP155 (Tair, RH); TEROS 11 (Tsoil, soil moisture) at 5 cm depth; all 30-minute means.

## Data processing
- Processing workflow follows Morrison et al. (2019).
- Flux computation: 30-minute NEE, LE, H using EddyPro 7; includes data conditioning, angle-of-attack correction, time lag adjustments, and co-spectral attenuation corrections.
- Random uncertainty estimated per referenced methods.

## Quality control
- Software: R (v4.1.3).
- Criteria for data retention: removal of statistical outliers; LI-COR signal anomalies (>10% above baseline); footprint model indicating data outside site boundaries (>20%); unrealistic flux thresholds (H, LE, NEE); friction velocity (u*) thresholds (<0.14 m s^-1).

## Gap-filling and flux partitioning
- Gap-filling and partitioning of NEE performed with REddyProc (R v4.1.3).
- Gap strategies: marginal distribution sampling; uncertainty estimated as the standard deviation of data used to fill gaps.

## Data structure and content
- File: Yorkshire_Pasture_2021_2023.csv (Date in dd/mm/yyyy; GMT; Time in HH:MM:SS; all in GMT).
- Key flux variables (before gap-filling): NEE, LE, H, and their uncertainties; momentum flux (Tau) and its uncertainty; CO2 storage terms; storage terms for LE and H; barometric pressure; air temperature (Tair); relative humidity (RH); vapor pressure deficit (VPD); radiation terms (SWin, SWout, LWin, LWout, Rnet, PAR); soil and moisture terms (Tsoil, VWC); wind metrics (windspeed, winddir, Ustar); turbulence metrics (TKE, Tstar, L, (z-d)/L).
- Gap-filled/partitioned quantities: NEE_f (gap-filled NEE), NEE_f_sd (uncertainty), Reco (ecosystem respiration), GPP (gross primary productivity).
- Note: NA denotes missing data.

## Acknowledgements
- Funded by the Leeds-York-Hull Natural Environmental Research Council (NERC) DTP Panorama (grant NE/S007458/1).
- Acknowledges University of Leeds Research Farm and Rob Yardley for farm-management information.

## References (key instruments and methods)
- EddyPro, REddyProc, standard micrometeorology references, and instrument models (LI-7200RS, SN-500, HMP155, TEROS 11), among others.