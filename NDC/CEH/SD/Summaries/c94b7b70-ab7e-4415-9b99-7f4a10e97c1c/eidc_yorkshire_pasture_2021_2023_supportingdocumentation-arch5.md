# Eddy covariance measurements of carbon dioxide, energy and water fluxes at a pasture, Yorkshire, UK, 2021-2023

## Overview
- 30-minute observations of net ecosystem CO2 exchange (NEE) and sensible (H) and latent heat (LE) fluxes over 1.5 years on an agriculturally managed pasture in Yorkshire, UK.
- Measurements collected using the micrometeorological eddy covariance (EC) method from 01/09/2021 to 01/01/2023.
- Dataset also includes weather and soil physics measurements.

## Study site
- Location: field at the University of Leeds Research Farm (53°51'58.64"N, 1°19'11.08"W).
- Land management: grazing by sheep since 2012; occasional silage cutting; rainfed; no fertiliser applied.
- Climate: temperate oceanic; mean annual temperature ~9.5°C and precipitation ~885 mm (1992–2022).
- Soil: loamy, calcareous brown earth; pH ~6.8; bulk density ~1.1 g/cm³; 0–30 cm carbon ~27.7 g/kg and nitrogen ~2.3 g/kg.
- Management during study: periodic grazing; silage cut in July 2022.

## Collection methods and fieldwork instrumentation
- Automated measurements of CO2 fluxes, weather, and soil parameters from 01/09/2021 to 01/01/2023.
- Flux instrumentation: EC system with sensors mounted 2 m above the canopy; LI-7200RS CO2/H2O analyser and Gill Windmaster 3D anemometer; data at 10 Hz, summarized to 30-minute means; processed by CR1000X and Smartflux 2.
- Ancillary measurements: net radiation (Rnet), short- and long-wave radiation (SWin, SWout, LWin, LWout), air temperature (Tair), relative humidity (RH), soil temperature (Tsoil) and soil moisture (VWC) at 5 cm; all as 30-minute means.

## Data processing
- Processing workflow based on Morrison et al. (2019).
- 30-minute fluxes (H, LE, NEE) computed with EddyPro 7; includes data conditioning, angle of attack correction, time-lag correction, and correction for high/low-frequency co-spectral attenuation.
- Random uncertainty estimated following Finkelstein & Sims (2001).

## Quality control
- Performed in R (v4.1.3) to ensure high-quality data.
- Data removal criteria include: statistical outliers, LI-COR signal strength anomalies (>10% above baseline), nonrepresentative footprints (>20% data outside site boundaries), unrealistic flux thresholds (H: 200–450 W m⁻²; LE: -50 to 400 W m⁻²; NEE: -60 to 30 μmol m⁻² s⁻¹), and friction velocity (u*) < 0.14 m s⁻¹.

## Gap-filling
- Gap filling and NEE partitioning performed with REddyProc (R) following Reichstein et al. (2016).
- Missing periods gap-filled using marginal distribution sampling; uncertainty from the standard deviation of filled observations.

## Details of data structure
- File: Yorkshire_Pasture_2021_2023.csv with 30-minute records.
- Key variables (examples): NEE, NEE_unc, LE, LE_unc, H, H_unc, Tau (momentum flux), Tau_unc, CO2_strg, LE_strg, H_strg, Pa, Tair, RH, VPD, SWin, SWout, LWin, LWout, Rnet, PAR, G, GPP, Reco, NEE_f, NEE_f_sd.
- Timestamps in GMT (Date: dd/mm/yyyy; Time: HH:MM:SS).
- Additional fields include soil and meteorological parameters (Tsoil, VWC, windspeed, winddir, Ustar, TKE, L, (z-d)/L, etc.).
- NA denotes missing data.

## Acknowledgements
- Funded by Leeds-York-Hull NERC DTP Panorama (grant NE/S007458/1).
- Thanks to University of Leeds Research Farm and Rob Yardley for farm management information.

## References
- Includes referenced instruments, processing tools, and methodological papers (e.g., EddyPro, REddyProc, Moncrieff et al., Reichstein et al., Papale et al., Morrison et al., etc.).